# Modularitás a CIC rendszerben

A CentralInfraCore (CIC) rendszer modularitása nem csupán kódújrafelhasználhatóságot jelent — hanem **séma-alapú funkcionalitás-elhatárolást** és **gráf-szintű újrakomponálhatóságot**.

---

## 🧱 Modul fogalma a CIC-ben

Egy modul:

* egyértelmű `kind` és `version` alapján azonosítható
* rendelkezik saját sémával (input, state, relay-viselkedés)
* lehet relézhető komponens vagy önálló feldolgozó

Modul lehet például:

* `cert/selfsigned`
* `vault/secret`
* `node/basic`

---

## 🧩 Modularitási elvek

### 1. **Sémaalapú elhatárolás**

Minden modul saját sémával és öröklési fával rendelkezik.

### 2. **Gráfba illeszthetőség**

A modulok relézhető csomópontként illeszthetők a végrehajtási gráfba.

### 3. **AI-navigálhatóság**

A modulokhoz prompt vagy relé-logika alapján automatikusan elérhető súgó, validátor és szülő-séma.

### 4. **Izolálhatóság**

A modul saját állapotkezelést és relé-választást végezhet, más komponensektől függetlenül.

---

## 🔗 Modulkapcsolatok

A modulok között lehet:

* **öröklési viszony** (pl. `node/basic` ← `node/k8s`)
* **relay-útvonal kapcsolat** (pl. `cert/selfsigned` → `vault/secret`)
* **szerepalapú szűrés** (pl. csak bizonyos user inputra aktiválható)

---

## 📌 Példa modulstruktúra

```yaml
kind: cert/selfsigned
version: v0.1
schema:
  required: [cn, duration]
relay:
  triggers: [vault/secret]
```

---

## 🎯 Miért fontos?

* A moduláris struktúra teszi lehetővé a **PoC-k bővítését** éles rendszerré
* Későbbiekben támogatja a **szerepalapú vezérlést és validációt**
* Az AI számára **értelmezhető egységeket** jelent, amiket menüből is elérhet

---

*Készült mesterséges intelligencia támogatásával. Minden modul egy irányított cél.*
