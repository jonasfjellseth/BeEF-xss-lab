# LAB — BeEF

## Forutsetninger
- Kali (angriper) med BeEF installert.
- Offer-VM (Windows/Linux) med nettleser som kan kjøre JavaScript.
- Isolert labnett (NAT/Bridged etter behov) med toveis nettverkstilkobling.
- Tillatelse og samtykke (bruk kun i lab).

---

## Steg 1 — Konfigurer BeEF og nettverk
<img width="288" height="70" alt="1 Hook js" src="https://github.com/user-attachments/assets/0ee72828-6b1a-4e80-a187-2bb69ad84f5e" />

*Endrer hooken*

---

## Steg 2 — Start BeEf
<img width="1404" height="725" alt="2  Oppstart av BeeF command" src="https://github.com/user-attachments/assets/49ee16e5-607b-4c6a-934d-c6f48515a337" />

*Start BeEF fra terminal (./beef).* 

---

## Steg 3 - Åpne adminpanelet
<img width="1219" height="799" alt="3  BeeF login" src="https://github.com/user-attachments/assets/b74542da-69ed-492e-89df-2b1a31a8b55f" />

*BeEF Login*

<img width="1219" height="805" alt="4  BeeF Administrasjonsgrensesnitt" src="https://github.com/user-attachments/assets/51e9d7e9-9600-4e5e-ad02-a63ecc5df79d" />

*BeEF administrasjonsgrensesnitt*

---

## Steg 4 - Injiser hook via XSS
<img width="1234" height="687" alt="5  Utført XSS med Hook" src="https://github.com/user-attachments/assets/1a4d5d62-bf4a-422d-9481-5ca154b51b69" />


*Payload som laster BeEF-hooken*

---

## Steg 5 - Bekrefter "Hooked Browser"
<img width="1963" height="986" alt="6  Hooked terminal og adminpanel" src="https://github.com/user-attachments/assets/447269c2-af9e-459b-a8f8-7e123b3a4e2e" />

<img width="1486" height="238" alt="6 5 Hooked Windows" src="https://github.com/user-attachments/assets/d0d6695f-611a-4b5c-980c-2000c0327a6b" />


*Bekrefter at vi har hooket browseren*

---

### Steg 6 - Funn av Cookies og IP-adresse
<img width="1488" height="492" alt="7  browser window origin, cookies og hostname" src="https://github.com/user-attachments/assets/7bf20fa4-dbb8-4fec-a9d8-54b70f0a4247" />

*Her ser vi informasjon man kan bruke videre som Cookies og IP-adresse av den hookede pc'en.*

---

