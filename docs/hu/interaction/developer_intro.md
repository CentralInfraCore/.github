# Developer – Nem kell mindent tudnod, csak ne te legyél a hiba forrása

## 💡 Nem a világot építed. Egy formába illeszkedsz.

A CIC nem abban segít, hogy kevesebbet hibázz, hanem hogy **a hibáid ne jussanak be a rendszerbe**.

Fejlesztőként nem kell tudnod, hol megy a relay, milyen validáció van a policy mögött vagy hogyan néz ki egy auditlog. Neked csak az a dolgod, hogy **amit átadsz, az legyen leírva, értelmezhető és valid**.

---

## 🧩 Mit kapsz, ha CIC-ben gondolkodsz?

* **Nincs "hogyan"** – csak "minek kell lennie".
* **Nem kell env file, config map, init script** – a rendszer *megmondja*, mit kap a szolgáltatás.
* **Nem kell regressziótól félned** – ha nem valid, be se kerül.
* **Nem kell elmagyaráznod, hogy "mi a service"** – a leírás *önmagát definiálja*.

---

## ✍️ Mit vár el tőled a rendszer?

* Egyértelmű schema-konform struktúrát.
* Deklarált be- és kimeneti interfészt.
* Nem workaroundot, hanem értelmezhető viselkedést.

Ne hackeld meg a környezeted. Írd le, mit vársz el.
A CIC biztosítja.

---

## 🧠 Mi történik a leírásoddal?

* A schema validálja.
* A relay továbbítja.
* A state összeveti a jelenlegi állapottal.
* Az output loggolva, követhetően, visszacsatolva kerül vissza hozzád.

Ez nem CI pipeline. Ez **üzemelési valóság**.

---

## 🎯 Miért jó ez neked?

* Mert nem kell végtelen debugolás.
* Mert a rendszer elmondja, ha nem stimmel, *mielőtt deploy lenne*.
* Mert bármikor visszanézheted, **mi volt az input, a szándék, és a következmény**.

Ez nem gúzsba köt. Ez **a te szándékod térképe**.
És mostantól *csak az kerül be, ami megfelel ennek.*
