# 🧠 CIC Dokumentáció – Rendszeráttekintés

Üdvözlünk a **Central Infrastructure Controller (CIC)** dokumentációjában!
Ez a rendszer egy alapjaiban más szemléletű megközelítést vezet be az infrastruktúra-kezelésben:
📌 deklaratív, állapotalapú, validált és szerepkörvezérelt.

A dokumentumok nyelv és cél szerint vannak strukturálva. Nyelvek: `hu/` (magyar) és `en/` (angol).

---

## 📁 Könyvtárstruktúra és cél

| Könyvtár       | Funkció                                 | Kulcsszavak                |
| -------------- | --------------------------------------- | -------------------------- |
| `concept/`     | Miért létezik a CIC?                    | filozófia, világlátás      |
| `reality/`     | Hogyan gondolkodik és működik belülről? | állapotlogika, séma, relay |
| `interaction/` | Kik használják és hogyan?               | szerepek, belépési pontok  |
| `usage/`       | Hogyan néz ki a gyakorlatban?           | folyamatok, példák         |
| `deployment/`  | A rendszer bevezetése és integrációja   | init, bootstrap, runtime   |

---

## 🔍 Könyvtárak részletesen

### `concept/` – 🌐 A rendszer filozófiája

Az alapvető gondolatok, amelyek a CIC működését meghatározzák.
Nem a működést írják le, hanem a **célt és gondolkodásmódot**.

* `cic_gondolkodasmod.md`: A modell alapgondolata
* `cic_brain.md`: A logikai mag leírása
* `alapelvek.md`: Alapelvek – az állapot nem vágy, hanem igazság

### `reality/` – 🧬 A rendszer belső világa

Leírja, hogyan látja önmagát a CIC: struktúráját, döntéseit, működését.

* `schema.md`: Strukturális szabályok és típusok
* `state_model.md`: Az aktuális és elvárt állapot összevetése
* `relay_flow.md`: A CIC irányítási és továbbítási logikája
* `error_logic.md`: Hibaészlelés és propagáció

### `interaction/` – 🧍 Emberi nézőpont

Szerepkörönkénti belépők. Minden szereplő saját szemszögéből ismerheti meg a CIC világát.

* `*_intro.md` fájlok (DevOps, Fejlesztő, QA, Vezető stb.)
* Cél: a **rendszergondolkodás emberi kontextusba helyezése**

### `usage/` – 🛠️ Gyakorlati alkalmazás

Konkrét leírások, újrahasználható példák, munkafolyamatok.

* `node_lifecycle.md`: Egy node életútja a rendszeren belül
* `deploy_with_validation.md`: Deploy validáción keresztül
* `rollback_flow.md`: Hogyan kezeljük a visszavonást
* `schema_upgrade.md`: A szabályrendszer biztonságos evolúciója

### `deployment/` – 🚀 Telepítés és környezetek

A CIC rendszer bevezetésének technikai és folyamati oldalai:

* `bootstrap.md`: Előkészítés, első környezet
* `env_profiles.md`: Környezetspecifikus séma- és jogosultsági különbségek
* `init_matrix.md`: Modulok és sémák indítási mátrixa
* `integration_bridge.md`: Külső rendszerekhez való illesztés

---

## 🎯 A dokumentáció célja

Nemcsak azt szeretnénk bemutatni, **hogyan működik a CIC** –
hanem azt is, hogy **miért változtat meg mindent, ha CIC-módon gondolkodunk**.

> Gondolkodj állapotban. Validáld a szándékot. Csak azt engedd be, ami igaz.