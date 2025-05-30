# Alapelvek

Ez a dokumentum összefoglalja a Central Infrastructure Controller (CIC) működésének alapvető elveit. Ezek az elvek nem megkerülhetők, nem opcionálisak, hanem a rendszer természetes következményei.

## 1. Az aktuális állapot nem azonos az elvárt állapottal

A rendszer különbséget tesz a *valóság* (amit érzékel) és a *terv* (amit leírtak) között. A CIC feladata e kettő folyamatos szinkronban tartása.

## 2. Minden entitás deklaratív módon van leírva

Nem konfigurálunk kézzel, nem scriptelünk változást – hanem leírjuk, *minek kell lennie*. A rendszer ebből következteti le a végrehajtandó lépéseket.

## 3. Validáció minden előtt

Bármilyen adat, leírás, változtatás csak akkor léphet be a rendszerbe, ha az *sémaszinten* érvényes. A validáció nem feature – ez maga a biztonsági keret.

## 4. Nincs workaround – csak szabályos megoldás

Ha valamit „külön kell kezelni”, akkor a rendszer *nem tudja garantálni* a működést. Minden entitás vagy része a gráfnak, vagy nem.

## 5. Minden változás nyomon követhető

A rendszer minden állapotváltozást naplóz, visszavezethetővé tesz, és következményeit kezeli. Semmi sem történik „csendben”.
