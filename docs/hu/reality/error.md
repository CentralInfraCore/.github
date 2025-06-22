# Hibakezelési logika a CIC-ben

A CentralInfraCore (CIC) rendszerben a hibakezelés nem egy utólagos szempont, hanem szerves része a relé-alapú végrehajtási logikának. A cél nem pusztán a hiba megjelenítése, hanem annak **értelmezett visszacsatolása és következményalapú kezelése**.

---

## 🎯 Célok

* **Értelmes hibák**: A hiba nem csak egy üzenet, hanem struktúrált objektum
* **Relé-visszacsatolás**: A hiba relé-visszairányban továbbítható
* **AI-közvetíthetőség**: A hiba lehet része az AI-navigációs logikának (pl. új promptot indít)

---

## 🧱 Hibatípusok

### 1. **Sémahibák**

* Hiányzó vagy hibás mezők a deklarációban
* Inkompatibilis típus vagy szemantikai kizárás

### 2. **Állapothibák**

* A megfigyelt állapot eltér a deklarálttól, de nem módosítható
* Állapot-származtatás sikertelen

### 3. **Relézési hibák**

* Nem létező útvonal vagy relay-pont
* Nem teljesített kötelező reléfejléc (pl. verzió hiánya)

### 4. **Végrehajtási hibák**

* Modul vagy renderer nem elérhető
* Külső rendszer nem válaszol, vagy állapot összeomlik

---

## 🔁 Hibák útvonala

```plaintext
hiba keletkezik → relé visszacsatolás → eredeti állapotcél módosítása vagy figyelmeztetés generálása
```

A hibák **nem fojtják le a rendszert**, hanem visszairányított, értelmezhető eseményekké válnak.

---

## 🧠 AI és hibakezelés

* A struktúrált hiba **promptot indíthat** („Miért nem sikerült a relay X?”)
* A hibákból **tudásgráf** vagy AI-útvonal tanulható
* A hibákhoz **kontextus-alapú súgó vagy workflow** társítható

---

## Összefoglalás

A CIC hibakezelési modellje **nem logol, hanem értelmez**, és ezt a szemléletet adja tovább a reléken, AI-n és dokumentumokon keresztül.

---

*Készült mesterséges intelligenciával együttműködve. Hibával szemben nem fut, hanem tanul.*
