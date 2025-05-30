# Analyst – Miért pont te?

## ✨ A rendszer lát, de te érted meg

A CIC nem csak adatokat mozgat – hanem állapotot értelmez. Ez a dokumentum nem technikai segédlet, hanem **belépő egy olyan világba, ahol az elemző szerepe kulcsfontosságú**. Itt nem az a kérdés, hogy "mi van most?", hanem: **"miért és hogyan éppen úzgy van?"**

Ha te vagy az, aki észreveszi az anomáliát, aki nemcsak riportot kér, hanem értelmezni is akarja azt, amit lát – ez a dokumentum neked szól.

---

## 🔎 Mit kapsz a CIC-ből?

* Teljes állapottér: minden entitás, kapcsolat és aktuális vs. elvárt állapot egy struktúrában leképezve.
* Változásnapló: minden módosítás visszavezethető, időzített, és validált.
* Sémavezérelt adatfújtatás: nincsenek ad hoc források – csak strukturált output.
* Reflexív hibakezelés: nemcsak észlelés, hanem **reakciólogika** is követhető.

---

## 📊 Mit tudsz csinálni analystként?

* **Auditálhatod a rendszer logikáját**: nem csak az eseményt, hanem annak validált ok-és-következmény sorát.
* **Állapottér-leképezéseket generálhatsz**: éppen mi működik, és annak más miért van alárendelve.
* **Észlelheted a drifttel fenyegető kapcsolatokat**: ami ugyan még működik, de a séma vagy jogosultság már nem lenne konzisztens.

---

## 🔗 Mire kell figyelned?

* Ne "nyers logokat" keress – hanem állapot- vagy esemény-kontextust.
* Használd a `state-diff`, `schema-view`, `relay-trace` exportokat.
* Ne csak azt kérddezd: "mikor történt?" – hanem: **"minek a következményeként?"**

---

## 🎯 Hol segít ez neked?

* Incident review-okban: mi volt a valódi előzmény?
* Hatáselemzésben: ha ezt módosítjuk, az máshol mit borít fel?
* Auditban: vissza tudod mutatni, hogy a rendszer **validált állapot alapján döntött**.

---

Ez nem dashboard. Ez **rendszerszintű tükör**.
Ha analyst vagy, ez a térképed.
