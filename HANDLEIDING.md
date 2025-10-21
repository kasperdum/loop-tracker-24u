# 📱 24u Loop Leuven - Gebruikershandleiding

## 🌐 Stap 1: App Online Zetten

Je hebt de app nu lokaal draaien. Om deze naar iedereen door te sturen moet je de app **online hosten**. Hier zijn de beste opties:

### Optie A: GitHub Pages (GRATIS & MAKKELIJK) ⭐ AANGERADEN
1. Maak een GitHub account aan (als je die nog niet hebt)
2. Maak een nieuw repository: "loop-tracker-24u"
3. Upload alle bestanden:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `generate-icons.html`
   - `icon-192.png` en `icon-512.png` (nadat je ze hebt gegenereerd)
4. Ga naar Settings → Pages
5. Selecteer: Source = "main branch"
6. Je krijgt een URL zoals: `https://jouwnaam.github.io/loop-tracker-24u/`
7. **Dit is de link die je deelt met iedereen!** ✅

### Optie B: Firebase Hosting (GRATIS)
1. Je gebruikt al Firebase voor de database
2. Installeer Firebase CLI: `npm install -g firebase-tools`
3. Run: `firebase init hosting`
4. Deploy: `firebase deploy --only hosting`
5. Je krijgt een URL zoals: `https://jouw-project.web.app/`

### Optie C: Netlify (GRATIS)
1. Ga naar [netlify.com](https://netlify.com)
2. Sleep je project folder naar de website
3. Je krijgt direct een URL
4. Elke update = nieuwe folder slepen

### Optie D: Eigen Server
Als je school/organisatie een webserver heeft, upload alle bestanden daar.

---

## 📲 Stap 2: App Openen op Smartphone

### Android (Chrome):
1. **Open de link** die je hebt gekregen (bijv. GitHub Pages URL)
2. De app opent in Chrome
3. Kijk naar het **menu (⋮)** rechtsboven
4. Je ziet: **"App installeren"** of **"Installeren..."**
5. Klik daarop → De app wordt geïnstalleerd!
6. **Vind de app terug**: Op je home screen als normaal app icoon 📱

### iPhone/iPad (Safari):
1. **Open de link** in Safari (NIET Chrome!)
2. Klik op de **"Deel" knop** onderaan (vierkant met pijl ↗)
3. Scroll naar beneden → **"Zet op beginscherm"**
4. Pas de naam aan (bijv. "24u Loop")
5. Klik **"Voeg toe"**
6. **Vind de app terug**: Op je home screen als normaal app icoon 📱

### Direct Gebruiken (Zonder Installeren):
- Je kunt de link ook gewoon openen in de browser
- De app werkt perfect zonder te installeren
- PWA = Progressive, niet verplicht!
- Installeren geeft wel betere ervaring (volledige scherm, sneller)

---

## 💻 Stap 3: Gebruiken op PC/Laptop

### Niets is veranderd! ✅
- De app werkt **exact hetzelfde** als voorheen
- Open gewoon de link in Chrome, Edge, Firefox, etc.
- Alle functionaliteit blijft hetzelfde:
  - Timer ✅
  - Wachtrij ✅
  - Rankings ✅
  - Admin functies ✅
  - Dark mode ✅
  - Export naar CSV ✅

### Ook Installeerbaar op PC:
1. Open de app in Chrome of Edge
2. Kijk naar de **adresbalk** → installatie icoon ⊕
3. Of: Menu → **"App installeren"**
4. De app wordt toegevoegd aan je Startmenu/Taakbalk
5. Start voortaan vanaf daar (eigen venster, geen browser UI)

---

## 👥 Stap 4: Link Delen met Team

### Wat moet je delen?
**Alleen de URL!** Bijvoorbeeld:
- `https://jouwnaam.github.io/loop-tracker-24u/`
- Of je Firebase/Netlify URL

### Hoe delen?
📧 **Email**: Stuur de link naar alle vrijwilligers  
💬 **WhatsApp/Telegram**: Deel in groepschat  
📱 **QR Code**: Maak een QR code van de URL (bijv. via qr-code-generator.com)  
📋 **Tijdens Event**: Print QR code op posters/briefing materiaal

### Voorbeeld Bericht:
```
📱 24u Loop Leuven Tracker

Hoi allemaal! Gebruik deze app tijdens het event:
🔗 https://jouwnaam.github.io/loop-tracker-24u/

📲 SMARTPHONE: 
- Android: Open link → Menu → "App installeren"
- iPhone: Open in Safari → Deel → "Zet op beginscherm"

💻 LAPTOP/PC:
- Open gewoon de link in je browser

✨ Werkt ook offline!
```

---

## 🔒 Stap 5: Icons Genereren (Eerst Doen!)

**BELANGRIJK**: Voor PWA moet je de icons eerst maken:

1. **Open**: `http://localhost:8080/generate-icons.html`
2. **Download**: Beide icons (192x192 en 512x512)
3. **Plaats**: In je project folder (naast index.html)
4. **Upload**: Samen met de andere bestanden naar hosting

Zonder icons werkt de PWA installatie niet goed!

---

## ❓ Veelgestelde Vragen

### "Ziet iedereen dezelfde data?"
✅ **JA!** Iedereen die de link opent ziet dezelfde data dankzij Firebase.
- Alle apparaten synchroniseren real-time
- Rondetijden worden direct gedeeld
- Wachtrij updates instant

### "Werkt het zonder internet?"
✅ **JA!** Dankzij PWA:
- App blijft werken offline
- Data wordt lokaal opgeslagen
- Synchroniseert automatisch wanneer online
- Perfect voor plekken met slechte verbinding!

### "Moet iedereen installeren?"
❌ **NEE!** 
- Gewoon de link openen werkt ook prima
- Installeren is optioneel (maar wel fijner)
- Je kunt ook gewoon in de browser werken

### "Kan ik updates doen tijdens het event?"
✅ **JA!**
- Upload nieuwe versie naar je hosting
- Service Worker update automatisch
- Gebruikers krijgen de nieuwe versie binnen 1 minuut
- Geen re-installatie nodig!

### "Werkt dark mode op alle apparaten?"
✅ **JA!** 
- Werkt op smartphone, tablet, laptop, desktop
- Toggle knop zichtbaar naast "Online" indicator
- Keuze wordt onthouden per apparaat

### "Kan ik CSV exporteren op smartphone?"
✅ **JA!**
- Admin tab → "Exporteer naar CSV"
- Bestand wordt gedownload naar je telefoon
- Open in Excel/Sheets op telefoon of PC

---

## 🎯 Checklist Voor Launch

Voordat je de link deelt:

- [ ] Icons gegenereerd en geplaatst (`icon-192.png`, `icon-512.png`)
- [ ] Firebase configuratie ingevuld (anders alleen lokaal)
- [ ] Alle bestanden geüpload naar hosting
- [ ] Link getest op smartphone (Android + iPhone)
- [ ] Link getest op PC/laptop
- [ ] PWA installatie getest
- [ ] Dark mode getest
- [ ] Offline functionaliteit getest (vliegtuigmodus!)
- [ ] CSV export getest
- [ ] Link gedeeld met team

---

## 🆘 Hulp Nodig?

### Browser Console Checken:
1. Op PC: F12 → Console tab
2. Kijk naar errors (rood)
3. Veel voorkomende problemen:
   - Firebase config ontbreekt
   - Icons niet gevonden (404)
   - Service Worker registratie mislukt

### PWA Checken:
Chrome → F12 → **Application tab**
- **Manifest**: Zie je de icons?
- **Service Workers**: Status = "Activated"?
- **Storage**: LocalStorage data aanwezig?

---

## 🎉 Klaar!

Je app is nu:
- ✅ Een echte PWA
- ✅ Installeerbaar op alle apparaten
- ✅ Werkend offline
- ✅ Klaar om te delen

**Volgende stap**: Upload naar GitHub Pages en deel de link! 🚀
