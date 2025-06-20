# Séma a CIC-ben

A CentralInfraCore (CIC) rendszerben a **séma** nem csupán adatstruktúra-leírás — hanem a rendszerlogika gerince. Meghatározza az objektumok szerkezetét, érvényességi szabályait, alapértelmezett örökléseit és viselkedési korlátait.

## Mi az a séma?

A CIC-ben a séma leírja:

* **Kötelező mezők**: Amit minden objektumnak tartalmaznia kell
* **Opcionális mezők alapértelmezéssel**: Amik kihagyhatók, de ismert alapértékkel feltöltődnek
* **Típuskorlátok**: Elfogadott formátumok (pl. string, lista, logikai érték)
* **Beágyazott logika**: Objektum-alobjektum kapcsolatok, öröklési szabályok
* **Szemantikai kizárások**: Egymást kizáró mezők vagy kombinációk

A sémák YAML-formátumban vannak deklarálva, és verziózottak (pl. `v0.1/node/basic`).

## A séma szerepei

* **Bemeneti validáció**: Ellenőrzi a leíró fájlban megadott objektumok helyességét
* **Relay konfiguráció**: Feltételes végrehajtási útvonalak meghatározása
* **Állapotszármaztatás**: Hiányzó értékek előállítása
* **Dokumentáció**: Segít az emberi és AI-feldolgozásban is

## Példa sémarészlet

```yaml
kind: cic-node
version: v0.1
schema:
  required:
    - os
    - network.ip
  optional:
    hostname: auto
    ssh: false
  mutually_exclusive:
    - [ip, dhcp]
```

Ez a séma meghatározza:

* Az objektumnak kötelező megadni az `os` és `network.ip` mezőket
* A `hostname` opcionális, de alapértelmezett értéke `auto`
* `ip` és `dhcp` mezők nem szerepelhetnek egyszerre

## Séma vs Statikus típusdefiníció

| Tulajdonság  | Statikus típus      | CIC séma                         |
| ------------ | ------------------- | -------------------------------- |
| Célterület   | Kódbázis            | Infrastruktúra-leíró fájlok      |
| Kontextus    | Fordítási idő       | Validáció + származtatás + relay |
| Bővíthetőség | Korlátozott         | Teljes YAML-alapú modularitás    |
| Használat    | Fejlesztői eszközök | Operátor, AI és relay rendszerek |

## Tervezési célok

* **Szilárd, tesztelhető szerződéseket** biztosítani a rétegek között
* **Moduláris bővíthetőséget** és öröklést lehetővé tenni
* **Futásidejű validálást támogatni kódírás nélkül**

---

*Készült mesterséges intelligencia együttműködésével, emberi validációval.*
