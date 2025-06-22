# Állapot a CIC-ben

A CentralInfraCore (CIC) rendszerben az **állapot** nem csupán egy pillanatfelvétel – hanem egy verziózott, deklaratív struktúra, amely tükrözi az infrastruktúra minden objektumának kívánt, származtatott és megfigyelt állapotát.

## Mi az állapot?

A CIC különbséget tesz az állapot három rétege között:

* **Deklarált állapot**: Amit a felhasználó közvetlenül meghatároz a leíró fájlban.
* **Származtatott állapot**: Ami az alapértelmezések, öröklés vagy kapcsolatok alapján jön létre.
* **Megfigyelt állapot**: Amit a valós környezetből visszaolvas vagy érvényesít a rendszer.

Ez a három szint dinamikus egységet alkot, lehetővé téve a CIC számára az összevetést, ellenőrzést és a szükséges korrekciót.

## Az állapot szerepei

* **Validáció**: A deklarált + származtatott állapot sémák alapján kerül ellenőrzésre.
* **Összehasonlítás**: A megfigyelt és deklarált állapot eltérései a „drift” detektálásához vezetnek.
* **Alkalmazás**: Ha a deklarált ≠ megfigyelt → a CIC relé útján állapotkorrekciót hajt végre.
* **Visszagörgetés**: A verziózott állapot lehetővé teszi a múltbeli állapotok visszaállítását.

## Példa

```yaml
object: cic-node-1
state:
  declared:
    os: debian-12
    network:
      ip: 10.0.5.83
  derived:
    fqdn: cic-node-1.infra.local
  observed:
    os: debian-11
    network:
      ip: 10.0.5.83
```

Ez az állapotobjektum hibajelzést váltana ki: az `os` mező nem egyezik.

## Hogyan kezeli a CIC az állapotot?

1. **Betölti a deklarált állapotot** a leíróból
2. **Séma alapján származtatja** a kapcsolódó értékeket
3. **Összeveti a megfigyelt állapottal**
4. **Relé aktiválásával** javítja az eltérést

## Tervezési célok

* Biztosítani a teljes rálátást arra, hogy az infrastruktúrának **milyennek kellene lennie**, **milyen lehet**, és **milyen ténylegesen**
* Lehetővé tenni az **AI által támogatott validálást**
* Támogatni a **deklaratív diff-alapú korrekciót és visszagörgetést**

---

*Készült mesterséges intelligencia együttműködésével, emberi validációval.*
