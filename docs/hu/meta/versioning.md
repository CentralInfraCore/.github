# Verziókezelés a CIC-ben

A CentralInfraCore (CIC) rendszerben a verziózás nem csupán fájlnevekhez tartozó címke — hanem **a tudás érvényességének és viselkedésének határozott állítása**.

---

## 🧠 Verziók jelentése

A CIC-ben a verziózás:

* **értelmezési kontextust** határoz meg (pl. sémaértelmezés v0.1)
* **végrehajtási útvonalat** befolyásol (pl. relay csak v1.0-val működik)
* **AI-navigációt** korlátoz/hangol (pl. prompt csak adott séma-verzióval működik)

---

## 📌 Hol alkalmazunk verziót?

* **Sémák**: `schema/version: v0.1`, `cert/selfsigned/v1.0`
* **Objektumok**: az `object.kind` mezőhöz tartozik
* **Relay-k**: a támogatott verziók listája `supports: [v0.1, v0.2]`
* **Promptok**: prompt csak bizonyos séma-verziókhoz passzolhat

---

## 🧩 Verziólogika típusai

| Típus     | Példa           | Jellemző                              |
| --------- | --------------- | ------------------------------------- |
| Stabil    | v1.0            | Fagyasztott, dokumentált              |
| Előnézeti | v0.2-beta       | AI-navigálható, de nem éles           |
| Belső     | internal-202506 | Csak belső teszt vagy konverzió célra |

---

## 🔁 Verzióváltás folyamata

1. Sémaújítás (`v0.2`): új mezők, új öröklési logika
2. Relay upgrade: új relay-kompatibilitási mátrix
3. Prompt igazítás: új válaszformátum, új szereplők

---

## 🎯 Miért ilyen fontos?

* **Biztonságos tudásevolúciót** biztosít a rendszer belsejében
* Lehetővé teszi **PoC és éles tudás párhuzamos futtatását**
* AI-nak segít a **megfelelő kontextus kiválasztásában**

---

*Készült mesterséges intelligencia együttműködésével. A tudás nem csak változik — verziót vált.*
