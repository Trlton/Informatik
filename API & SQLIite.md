# API og SQLite 
Dette tager udgangspunkt i projektet:

https://github.com/hojgfd/DATA-API-projekt.git


Dette projekt bruger flask** til at lave en APIog SQLite som datalag

---

## 1. API laget 

API'en fungerer som mellemlaget og definerer endpoints til systemet.

### Data modtagelse (POST Request)

```python
@app.route('/data', methods=['POST')
def receive_data():
    content = request.get_json(force=True) # Forventer JSON
    # ... lagring i DB...
    return jsonify({"status": "ok", "received": content}), 200 # Returnerer JSON-svar
```

### Logic
* f.eks. sortering eller tjek om værdier er under en bestemt værdi (regler ift luftkvalitet)

Eksempel: Ruten /anbefalinger tjekker, om den målte CO₂ og temperatur bryder indeklima retningslinjer (CO₂ > 1000, Temp < 20 osv)

```python
# Tjekker mod forretningsregler
if l["co2"] > 1000:
    problemer.append("For højt CO₂")
if l["temperatur"] < 20:
    problemer.append("For koldt")
```
---
## 2. Data laget (SQLite)
SQLite bruges til kontinuerlig lagring af sensordata

### Database oprettelse
* init_db(): Kaldes ved start (if __name__ == "__main__": init_db()) for at sikre, at databasen og tabellen (sensor_data) eksisterer, og laver dem hvis de ikke gør.

``` python
conn = sqlite3.connect("items.db")
c = conn.cursor()
c.execute("""
    CREATE TABLE IF NOT EXISTS sensor_data (
        # ... Kolonner defineret her
    )
""")
conn.commit()
```

### lagring af data
* Data der modtages via POST til /data, indsættes i databasen

```python
c.execute("""
    INSERT INTO sensor_data (klasse, co2, temperatur, luftfugtighed)
    VALUES (?, ?, ?, ?)
""", ("D2321", co2, temperature, humidity))
conn.commit()
```

### Selection og aggregation (dannelse af view)
* API'en henter data fra SQLite til at lave et bestemt "view" for brugeren. (f.eks. historik).

  
Eksempel: (/historik): Data grupperes og bliver aggregated ved brug af SQL for at vise gennemsnit pr. minut, hvilket reducerer mængden af data, der skal trækkes ud.
```python

SELECT strftime('%Y-%m-%d %H:%M:00', tidspunkt) as minut,
       AVG(co2), # Aggregering
       AVG(temperatur),
       AVG(luftfugtighed)
FROM sensor_data
GROUP BY minut  # Gruppering
ORDER BY minut DESC
```


