# Mi az a CentralInfraCore (CIC)?

A CentralInfraCore (CIC) egy új szemléletű infrastruktúra-leíró rendszer, amely **állapotalapú gondolkodást**, **séma-alapú végrehajtást**, és **AI által támogatott értelmezést** kombinál. Nem egy eszköz, hanem egy működő gondolkodási modell — relékkel, gráfokkal és tudással vezérelve.

---

## 🎯 Mit old meg a CIC?

* Leíró fájlok helyett **tudásvezérelt állapotdefiníciót** nyújt
* Nem szkripteket futtat, hanem **sémavezérelt relé-logikát** alkalmaz
* Nem csak gép által olvasható, hanem **AI-értelmezhető és navigálható**
* Minden állapot **verziózott, visszakövethető és validált**

---

## 🧱 Fő építőkövei

### Állapotmodell

Három szint: deklarált, származtatott, megfigyelt — minden döntés ezen alapul.

### Séma

Nem csak formátum, hanem értelmezési szabályrendszer. Minden objektum és prompt mögött séma áll.

### Relay-végrehajtás

Minden állapotváltozás reléken keresztül történik — gráfszerűen irányítva, nem lineárisan.

### Modularitás

A rendszer minden komponense verziózott és újrakomponálható. Semmi sincs „beleégetve”.

### AI-támogatás

A rendszer promptokkal értelmezhető — az AI segít elérni a megfelelő sémát, relét, vagy hibakezelést.

---

## 🧪 PoC jelenlegi határai

* **Selfsigned** tanúsítvány workflow relay-alapon
* **Basic state–schema–relay** lánc működése
* **Verziózott sémák**, validálás
* **AI-indexek** (pl. `_ai_prompt_index.yaml`, `.explained.md`)

### Amit még rejtünk (jövő)

* Multi-relé orchestration
* Szerepalapú prompt-navigáció
* Teljes rollout lifecycle vezérlés
* Self-healing logika és rollback workflow

---

## 👥 Kinek szól?

* Platform mérnököknek, akik nem akarnak kézzel YAML-t generálni
* Architekteknek, akik struktúrált, verifikálható rendszert keresnek
* AI-vezérelt dokumentációs vagy oktatási célra
* Mindenkinek, aki a DevOps következő szintjét keresi

---

## 🌱 Zárógondolat

A CIC nem „eszköz”, hanem egy **irányított rendszer** — amelyben az állapot szándékot fejez ki, a séma értelmez, a relé dönt, és az AI tanul.

Ez még csak a kezdet.

---

*Készült mesterséges intelligencia együttműködésével. Tudásvezérelt PoC.*
