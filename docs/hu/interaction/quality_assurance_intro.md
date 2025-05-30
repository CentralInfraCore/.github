# Quality Assurance – Ha a rendszerbe hiba jut, te nem voltál ott

## ✅ Nem a tesztelés a QA. A keretrendszer biztosítása.

A CIC nem helyetted dönt. Nem fogja megakadályozni, hogy valaki rossz kódot írjon. De **nem engedi be azt, ami nem konzisztens** – és ebben te vagy a kulcs.

Ha QA-s vagy, a célod nem az, hogy "átment a teszten", hanem hogy **be sem kerülhetett, ami nem volt szabályos**.

---

## 🔍 Mit ad neked a CIC QA-ként?

* **Sémaalapú belépési pont**: minden entitásnak definiált szerkezete van, amit a rendszer validál.
* **Verziózott állapotnaplózás**: nem csak mit, hanem *mikor, miért és ki validált*.
* **Minőségi kapuk (quality gates)**: explicit validációs szabályokkal és következményekkel.
* **Szabály-alapú kizárás**: ami nem teljesíti az elvárt struktúrát, az nem kerül be.

---

## 🧪 Mire használhatod?

* **Automatizált elfogadási kritériumokra**: nem kell utólag „megnézni”, mert ha hibás, be sem ment.
* **Release gating**: a build nem pipeline-szintű, hanem *rendszerszintű minőséghez kötött*.
* **Elvárt viselkedés megfogalmazására**: nem „reméljük, hogy működik” – hanem deklaráljuk.

---

## 🚦 Mire figyelj QA-ként?

* A séma = specifikáció. Ha ott nincs benne, akkor a rendszerben sincs.
* A validáció = kapu. Nem megkerülhető.
* A rollback = szabályos viselkedés, ha megsérült a minőség.

---

## 🎯 Miért fontos ez neked?

* Mert nem te vagy az utolsó védvonal – *hanem az első struktúraőr*.
* Mert nem neked kell felfedezni, mi volt a hiba – hanem biztosítani, hogy el sem juthatott odáig.
* Mert a CIC lehetővé teszi, hogy a **minőséget ne a folyamatban mérjük, hanem a rendszer létezésében**.

---

Ez nem pipeline step.
Ez **minőségi keretrendszer**, ahol a szabály nem ajánlás, hanem belépési követelmény.
Ha QA vagy, a CIC nem akadályod – **hanem a legerősebb érvényesítési felületed**.
