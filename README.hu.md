# CentralInfraCore

## Bevezetés

A CentralInfraCore egy egységes infrastruktúra-leíró rendszer, amely teljes életciklus-kezelést biztosít — a hardverbeszerzéstől a teljesen működőképes, hibrid felhőkörnyezetekig. A rendszer nem csupán technológiai szinten hoz újat, hanem egy olyan strukturált gondolkodásmódot is képvisel, amely hosszú távon képes újradefiniálni az infrastruktúra-kezelés és a DevOps szemlélet alapjait.

## Kiemelt architekturális jellemzők

* **Deklaratív infrastruktúra-leírás**: A rendszer minden komponensét YAML-alapú, gráfszerű struktúrában írjuk le — így az infrastruktúra szerkezete és állapota teljesen átláthatóvá válik.
* **Objektumorientált modularitás**: Minden funkció modulokba van szervezve, amelyek egymástól függetlenül értelmezhetők, fejleszthetők és validálhatók.
* **Esemény- és állapotvezérelt működés**: A rendszer nem parancsokat hajt végre, hanem állapotokat követ és reléként dönt: minden változás érvényes állapoton keresztül történik.
* **Verziózott és auditálható állapotlogika**: Minden elem változását és állapotát naplózzuk, visszakereshető módon — ezzel biztosítva az infrastruktúra valódi történetiségét és reprodukálhatóságát.

## Az infrastruktúra-leíró objektummodell

A CentralInfraCore leírómodellje egy irányított gráf, amelyben minden objektum világosan meghatározott szereppel és kapcsolódási lehetőséggel rendelkezik. A gráf felépítése lehetővé teszi az infrastruktúra egészének szemantikus és állapot-alapú értelmezését.

* **Alapobjektumok (Core Objects)**: Olyan entitások, amelyek önálló jelentéssel és életciklussal bírnak. Ezek a rendszer pillérei, például egy fizikai node, egy cluster vagy egy relay végpont.
* **Almodulok (Submodules)**: Támogató jellegű struktúrák, amelyek paraméterhalmazokat, alapértelmezett vagy származtatott értékeket tartalmaznak. Nem értelmezhetők önállóan, de szükségesek a magasabb szintű objektumok működéséhez.
* **Szemantikus kizárások**: Bizonyos attribútumok kizárják egymást annak érdekében, hogy az infrastruktúra logikai konzisztenciája biztosított maradjon (pl. ha „A” attribútum aktív, akkor „B” nem lehet jelen).

## Megvalósítás és integráció

A CentralInfraCore architektúrája nem egy konkrét platformhoz kötött, hanem a logikai modellje révén képes különféle környezetekhez illeszkedni. A megvalósítás mindig az aktuális infrastruktúra sajátosságaihoz igazodó adaptereken és API-kon keresztül történik.

* **Kubernetes-integráció**: A rendszer támogatja a Helm Chart-alapú telepítéseket, és kompatibilis olyan vezérlőeszközökkel, mint a FluxCD, ArgoCD vagy Rancher Fleet. Az integráció nemcsak telepítési, hanem állapot-szinkronizálási szinten is működik.
* **Hagyományos rendszerek kezelése**: A CentralInfraCore deklaratív modellje API-n keresztül képes kapcsolódni akár nem cloud-native környezetekhez is – például virtualizált infrastruktúrákhoz vagy hagyományos Linux-szolgáltatásokhoz.
* **Moduláris API-réteg**: Az egyes komponensek interfészei külön modulokként jelennek meg. Ez lehetővé teszi, hogy külső operátorok és menedzsment eszközök csak a saját működésükhöz szükséges részhez férjenek hozzá – ezzel biztosítva a rendszer stabilitását és skálázhatóságát.

## GitOps megközelítés

A CentralInfraCore nemcsak alkalmazza a GitOps szemléletet, hanem kibővíti azt az infrastruktúra-állapot formalizált, deklaratív és eseményvezérelt kezelésével. A rendszerben a Git nem csupán verzióforrás, hanem a teljes infrastruktúra valós idejű állapotának referenciája.

* **Központi Git repository**: Minden infrastruktúra-leírás és állapotverzió jól strukturált könyvtárszerkezetben van tárolva. A Git commit nemcsak változtatást, hanem állapotváltozási eseményt is jelent.
* **Automatizált és validált állapotalkalmazás**: Minden változás végrehajtása sémaalapú validáción és relay-folyamatokon keresztül történik. Az automatizálás nem csak telepít, hanem értelmez, érvényesít és visszajelez.
* **CI/CD új szinten**: A folyamatos integráció nem pusztán kód- vagy konfigurációszinten történik, hanem a rendszer tudásszintjén. Az állapot és a logika egyaránt tesztelhető, változásai követhetők, a hibák visszavezethetők.

## Használati esetek

A CentralInfraCore nem csupán egy rendszer, amely komplex infrastruktúrákat képes kezelni — hanem egy olyan szemléleti modell, amely új alapokra helyezi az infrastruktúra leírását, változáskezelését és validációját.

A CIC különösen ajánlott olyan vállalati környezetekben, ahol:

* Fizikai, virtualizált vagy Kubernetes-alapú infrastruktúrák egységes és átlátható kezelésére van szükség,
* Verziózott, auditálható és visszaállítható állapotreprezentáció a cél,
* A rendszer architektúrája modulárisan bővül, és a skálázás nemcsak technikai, hanem szervezeti elvárás is,
* Szükség van arra, hogy a konfigurációk ne csak működjenek, hanem értelmezhetők, érvényesíthetők és visszakövethetők legyenek — ember és gép számára egyaránt.

A CIC különösen hasznos, ha a cél a gondolkodás és működés összekötése: nem csak deploy, hanem tudásvezérelt rendszer.

## Dokumentációs szerkezet

A projekt dokumentációja több szinten épül fel, hogy kiszolgálja mind az emberi, mind a mesterséges intelligencia alapú feldolgozást.

* **Magyarázó tudásbázis (magyar és angol)**: `docs/` – szerepalapú, tematikus dokumentumok, négy fő nézőpont mentén:

    * `interaction/` – szerepkörök bevezetése (pl. DevOps, PM, Arch)
    * `reality/` – rendszerlogikai alapok (pl. relay, state, schema)
    * `concept/` – gondolkodási modell, elméleti alapok
    * `usage/` – gyakorlati alkalmazási minták, életciklus, visszagörgetés

* **AI-kompatibilis oktatási réteg**:

    * Oktató promptok: `prompts/` – célzott kérdés-válasz fájlok
    * Navigáció AI-rendszerek számára: `_ai_prompt_index.yaml`
    * Metaadatok és rendszerleírás AI-nak: `meta/cic.yaml`

Ez a szerkezet lehetővé teszi, hogy az emberi és AI-felhasználók eltérő mélységekben, célzottan navigáljanak a tudásbázisban – és akár fokozatosan felfedezzék a mögöttes rendszer komplexitását.

## További információ

Kapcsolat és támogatás:

* Projektvezető: Sinkó Gábor Zoltán

## Licenc

Ez a projekt a [Creative Commons Nevezd meg! – Ne add el! – Így add tovább 4.0 Nemzetközi (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.hu) licenc alatt érhető el.

*Ez a dokumentum mesterséges intelligencia közreműködésével, emberi validációval és szerkesztéssel készült.*
