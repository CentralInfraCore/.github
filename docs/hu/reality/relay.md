# Relay a CIC rendszerben

A CentralInfraCore (CIC) rendszerben a **relay** nem egy üzenetküldő vagy hálózati protokoll — hanem egy logikai vezérlőpont. Feladata, hogy sémavezérelt módon kezelje az állapotváltozásokat: érvényesítse, alkalmazza, és ha szükséges, továbbítsa őket.

## Mi az a Relay?

A relay egy **sémaérzékeny végrehajtási csomópont**, amely:

* bemenetként új objektumokat vagy konfigurációkat fogad,
* ezeket validálja a hozzá tartozó sémával,
* alkalmazza az érintett infrastruktúra-objektumon,
* továbbítja az eredményt más komponensek (pl. állapotfigyelő, generátor) felé.

A relay-ek láncolhatók: egyik relay kimenete lehet a másik bemenete. Így irányított gráf (DAG) szerű logika valósul meg.

## A relay feladatai

* **Sémavizsgálat**: Bemeneti struktúrák és szabályok ellenőrzése.
* **Relay-fejlécek kezelése**: Metaadatok alapján történő verziózás, célzás, hatókör meghatározás.
* **Állapotmódosítás**: Csak akkor történik változás, ha a bemeneti delta érvényes.
* **Továbbítás**: A következő rendszerkomponens számára előkészített kimenet generálása.

## Példa munkafolyamat (self-signed tanúsítvány)

```yaml
- input: új objektum "selfsigned-cert-abc"
- relay: sémaellenőrzés (v0.1/cert/selfsigned)
- frissítés: kívánt állapot – lejárat, DNS SAN, kulcsparaméterek
- továbbítás: state-tracker és secret generator komponens felé
```

## Relay vs Hagyományos CI/CD

| Funkció               | Klasszikus CI/CD        | CIC Relay                            |
| --------------------- | ----------------------- | ------------------------------------ |
| Indítás               | Commit vagy webhook     | Állapot + séma-delta + fejléc        |
| Validálás             | Manuális vagy részleges | Sémaalapú, kötelező                  |
| Folyamatlogika        | Pipeline lépések        | Irányított relay-útvonalak           |
| Újrafelhasználhatóság | Szkriptfüggő modulok    | Sémához kötött relézhető csomópontok |
| Hiba kezelése         | Futásidejű hibák        | Strukturált visszafordított relay    |

## Tervezési célok

* Infrastruktúra állapotváltozások **ellenőrizhetősége és visszavonhatósága**
* **Emberi és AI-alapú bemenetek támogatása**
* **Finomhangolt irányítás** a végrehajtási útvonalak felett

---

*Készült AI együttműködésben. Emberi felülvizsgálattal és sémakompatibilis szándékkal.*
