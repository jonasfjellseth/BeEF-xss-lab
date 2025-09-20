# 🐝 BeEF XSS Lab

## 📌 Formål
Dette prosjektet dokumenterer en labøvelse hvor jeg satt opp **BeEF (Browser Exploitation Framework)** i kali, tilpasser hook-filen, injiserer hooken i en sårbar webside via XSS, og observerer den “hooked” browser i BeEFs admin-panel (bl.a. cookies, hostname, PHPSESSIONID).  
Hensikten er for å forstå hvordan en XSS-basert browser-exploit kan brukes til å hente sensitive data fra offerets nettleser, og hvilke mottiltak som reduserer risiko. Alt utført i et lukket testmiljø med uttrykkelig tillatelse.

---

## 🔍 Innhold
Repoen dekker:
- **Scope:** Lokalt lab-oppsett med BeEF og en sårbar test-applikasjon.  
- **Metodikk:** Konfigurere BeEF → endre hook-URL → utføre XSS-injeksjon for å laste hook → observere hooked browser og utvinne cookies/PHPSESSIONID i admin-panelet.  
- **Filer:** Eksempel på hook-fil/payload, konfigurasjonseksempel, skjermbilder og en detaljert LAB.md med steg-for-steg.  
- **Etikk & lovverk:** Tydelig advarsel om at teknikkene kun skal brukes i kontrollerte miljøer med tillatelse.

---

## 🛠️ Verktøy brukt
- **BeEF (Browser Exploitation Framework)** – administrasjon/monitorering av hooked browsers  
- **nettleser** – teste XSS-injeksjon og payload-levering  
- **DVWA VM** – mål for XSS (testmiljø)  
- **Payloads:** tilpasset hook-fil

---

## 📊 Viktigste funn / observasjoner
- En persistent/reflective XSS kan injisere en ekstern hook (BeEF) i offerets DOM, som gir angriper mulighet til å kjøre browser-kommandosett og hente sensitive verdier (cookies, lokal hostname, PHPSESSIONID).  
- BeEFs admin-panel viser detaljert informasjon om hooked browsers (origin, user-agent, cookies).  
- Mottiltak: Content Security Policy (CSP), output-escaping, input-validering, HttpOnly & Secure cookies, sameSite-innstillinger, oppdatering av programvare og begrense inline-scripts.

---

## 📑 Repo-struktur
```bash
beef-xss-lab/
│── README.md
│── LAB.md    
│── LICENSE
