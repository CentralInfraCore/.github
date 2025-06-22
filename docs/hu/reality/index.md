# A valóság réteg – Áttekintés

Ez a dokumentum a CentralInfraCore (CIC) rendszer **valóság rétegét** mutatja be. Ez a réteg írja le, hogyan kapcsolódik a rendszer az infrastruktúra tényleges állapotához, és hogyan hajt végre állapotalapú műveleteket sémavezérelt logikával.

---

## 🧩 Alapvető komponensek

### 1. [Relay – Végrehajtás és továbbítás](relay.md)

A relék sémavezérelt csomópontok, amelyek érvényesítik, alkalmazzák és továbbítják az állapotváltozásokat. Irányított adatfolyamokat határoznak meg.

### 2. [State – Deklaratív állapotmodell](state.md)

Az állapot három szintből áll: deklarált, származtatott és megfigyelt. Ez a modell lehetővé teszi az eltérésfelismerést és deklaratív javítást.

### 3. [Schema – Strukturális és szemantikai szerződések](schema.md)

A sémák határozzák meg az objektumok kötelező mezőit, öröklési szabályait és validációs logikáját. Lehetővé teszik a moduláris és tesztelhető rendszerműködést.

### 4. [Hibakezelés – Relay visszacsatolás és helyreállítás](error.md)

A CIC-ben a hibák strukturáltak, visszacsatolhatók, és az AI-folyamatok részeként is felhasználhatók. Nem lefagyasztanak, hanem taníthatók.

---

## 🎯 Miért fontos?

A valóság réteg biztosítja a rendszer **technikai és szemantikai alapját**:

* az állapotok pontos lekérdezéséhez és ellenőrzéséhez
* sémavezérelt, újrajátszható végrehajtási logikához
* biztonságos, kontextus-alapú reléfolyamatokhoz
* AI-alapú visszajelzéshez és korrekcióhoz

---

## 📚 Kapcsolódó fájlok

* AI-navigáció belépőpont: [`_ai_prompt_index.yaml`](../../../_ai_prompt_index.yaml)
* A teljes rendszer logikai összefoglalója: [`meta/cic.yaml`](../../../meta/cic.yaml)

---

*Készült mesterséges intelligenciával együttműködve. Embernek olvasható, gépnek értelmezhető.*
