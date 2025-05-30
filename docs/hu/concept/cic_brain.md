# CIC – Az infrastruktúra agya

A Central Infrastructure Controller (CIC) nem csupán vezérlő – hanem a rendszer **központi idegrendszere**. A cél nem az, hogy a CIC „irányítson”, hanem hogy **tudja, mi történik**, és **reagálni tudjon, ha eltérés van**.

## Fogalmi hasonlat

A rendszer olyan, mint egy emberi test:
- Az egyes szolgáltatások a szervek.
- A sémák a DNS.
- A relay az idegrendszer.
- A validáció az immunrendszer.

A CIC ezek között tartja fenn az egyensúlyt és a kommunikációt – nem szinkronizál, hanem **rendszerszintű döntéseket hoz**.

## Miért agy, és nem operátor?

Egy klasszikus operátor újraindít, konfigurál, figyel.  
A CIC **gondolkodik, és következtetéseket von le**.

- Nem azt kérdezi, hogy „mi fut?”
- Hanem azt, hogy: „**annak kellene-e futnia?**”

Ez a különbség teszi a CIC-et *reflexívvé*. És ez teszi lehetővé, hogy **rendszerként működjünk, ne csak komponensekként**.
