# 🚀 Deployment Instructies

## Welke Bestanden MOET je uploaden?

### ✅ ESSENTIEEL (Moet mee):
```
📄 index.html              - Hoofdapplicatie
📄 manifest.json           - PWA configuratie  
📄 service-worker.js       - Offline functionaliteit
🖼️ icon-192.png           - App icoon (klein)
🖼️ icon-512.png           - App icoon (groot)
```

### ⚠️ OPTIONEEL (Mag mee maar niet nodig):
```
📄 generate-icons.html     - Icon generator tool (niet nodig als je icons al hebt)
🖼️ humasol_logo.png       - Logo (alleen als je die in index.html gebruikt)
🖼️ logo_24u.png           - Logo (alleen als je die in index.html gebruikt)
🖼️ Instagram_icon.png     - Social media icoon (alleen als gebruikt)
📖 HANDLEIDING.md          - Gebruikershandleiding (handig voor team)
📖 PWA-README.md           - Technische documentatie
📖 QUICK-START.md          - Snelstart gids
```

## 📦 Minimale Upload (Snelste Optie):

**Upload alleen deze 5 bestanden:**
1. `index.html`
2. `manifest.json`
3. `service-worker.js`
4. `icon-192.png`
5. `icon-512.png`

**Dat is het!** De app werkt dan volledig. ✅

---

## 🌐 GitHub Pages Deployment (Stap-voor-Stap):

### Methode 1: Via Website (Geen Technische Kennis Nodig)

#### A. Account Maken:
1. Ga naar [github.com](https://github.com)
2. Klik **"Sign up"**
3. Vul email, wachtwoord, gebruikersnaam in
4. Verifieer je email

#### B. Repository Maken:
1. Klik **"+" rechts boven** → "New repository"
2. **Repository name**: `loop-tracker-24u`
3. **Public** aanvinken (gratis!)
4. ✅ Check "Add a README file"
5. Klik **"Create repository"**

#### C. Bestanden Uploaden:
1. Klik **"Add file"** → **"Upload files"**
2. **Sleep de 5 essentiële bestanden** naar de website:
   - index.html
   - manifest.json
   - service-worker.js
   - icon-192.png
   - icon-512.png
3. Scroll naar beneden → Klik **"Commit changes"**
4. Wacht 10 seconden voor upload

#### D. GitHub Pages Activeren:
1. Klik **"Settings"** (tandwiel icoon bovenaan)
2. Scroll naar beneden in het menu links → Klik **"Pages"**
3. Bij **"Source"**: Selecteer **"main"** branch
4. Klik **"Save"**
5. **WACHT 1-2 MINUTEN** ⏳
6. Refresh de pagina
7. Je ziet nu bovenaan: **"Your site is live at https://..."**
8. **Kopieer die URL!** Dit is je app link! 🎉

#### E. Testen:
1. Open de URL in je browser
2. Test of alles werkt
3. Probeer te installeren als PWA
4. Test dark mode
5. Test offline (vliegtuigmodus)

#### F. Delen:
1. **Deel de URL** met je team via WhatsApp/Email
2. Iedereen kan nu de app gebruiken!

### Methode 2: Via Git (Voor Gevorderden)

```bash
# Clone je repository
git clone https://github.com/jouwnaam/loop-tracker-24u.git
cd loop-tracker-24u

# Kopieer je bestanden
copy "C:\Users\kaspe\OneDrive - KU Leuven\KUL\Humasol\HR\loop-tracker-24u\loop-tracker-24-v3\index.html" .
copy "C:\Users\kaspe\OneDrive - KU Leuven\KUL\Humasol\HR\loop-tracker-24u\loop-tracker-24-v3\manifest.json" .
copy "C:\Users\kaspe\OneDrive - KU Leuven\KUL\Humasol\HR\loop-tracker-24u\loop-tracker-24-v3\service-worker.js" .
copy "C:\Users\kaspe\OneDrive - KU Leuven\KUL\Humasol\HR\loop-tracker-24u\loop-tracker-24-v3\icon-192.png" .
copy "C:\Users\kaspe\OneDrive - KU Leuven\KUL\Humasol\HR\loop-tracker-24u\loop-tracker-24-v3\icon-512.png" .

# Upload
git add .
git commit -m "Deploy 24u Loop tracker PWA"
git push

# Activeer Pages via Settings → Pages → Source: main
```

---

## 🔄 Updates Doen Later:

### Via GitHub Website:
1. Ga naar je repository
2. Klik op het bestand dat je wilt updaten (bijv. `index.html`)
3. Klik **potlood icoon** (rechts boven) om te bewerken
4. Of: **"Upload files"** om nieuwe versie te uploaden
5. Scroll naar beneden → **"Commit changes"**
6. **Automatisch live binnen 1 minuut!** ⚡

### Via Git:
```bash
# Maak wijzigingen in je lokale bestanden
# Dan:
git add .
git commit -m "Update: beschrijving van wijziging"
git push
```

---

## 🎯 Andere Hosting Opties:

### Netlify (Ook Heel Makkelijk):
1. Ga naar [netlify.com](https://netlify.com)
2. Maak account (gratis)
3. **Sleep je folder** naar de website
4. Klaar! Je krijgt direct een URL
5. Updates: Sleep nieuwe versie van folder

### Firebase Hosting:
```bash
# Installeer Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Initialiseer
firebase init hosting
# Kies: public directory = "."

# Deploy
firebase deploy --only hosting
```

### Vercel:
1. Ga naar [vercel.com](https://vercel.com)
2. Maak account (gratis)
3. Connect je GitHub repository
4. Automatische deployment bij elke update!

---

## ⚠️ Belangrijke Checks Voor Launch:

- [ ] **Firebase configuratie ingevuld?**
  → Anders werkt alleen lokale opslag, geen sync tussen apparaten!
  
- [ ] **Icons aanwezig?** (icon-192.png en icon-512.png)
  → Anders installeert de PWA niet goed
  
- [ ] **Service worker geregistreerd?**
  → Open F12 → Console → Moet "Service Worker registered" zien
  
- [ ] **HTTPS?** 
  → GitHub Pages geeft automatisch HTTPS ✅
  → Lokale test (localhost) werkt ook ✅
  
- [ ] **Manifest.json geldig?**
  → Test via Chrome DevTools → Application → Manifest

---

## 🆘 Troubleshooting:

### "PWA installeert niet"
- Check of icons bestaan (icon-192.png, icon-512.png)
- Check manifest.json (geen syntax errors)
- Moet via HTTPS (GitHub Pages = automatisch HTTPS)
- Probeer in Chrome (beste PWA support)

### "Data synchroniseert niet tussen apparaten"
- Firebase configuratie controleren in index.html
- Check of je online bent
- Open F12 → Console → Kijk naar Firebase errors

### "Service Worker registreert niet"
- Check of service-worker.js in dezelfde folder staat
- Open F12 → Application → Service Workers
- Check voor errors in Console

### "Icons niet zichtbaar"
- Check bestandsnamen: exact `icon-192.png` en `icon-512.png`
- Check of ze in dezelfde folder staan als index.html
- Clear browser cache en reload

---

## 📧 Voorbeeld Deployment Email:

```
Onderwerp: 24u Loop Tracker - Live!

Beste team,

De 24u Loop tracker app is nu online! 🎉

🔗 Link: https://jouwnaam.github.io/loop-tracker-24u/

📱 SMARTPHONE:
- Android: Open link → Menu → "App installeren"  
- iPhone: Open in Safari → Deel → "Zet op beginscherm"

💻 LAPTOP/PC:
- Gewoon de link openen in je browser

✨ Features:
- Real-time rondetijden tracking
- Wachtrij beheer
- Rankings & statistieken
- Dark mode voor 's nachts
- Werkt ook offline!
- Export naar Excel

Vragen? Laat het me weten!

Groeten,
[Jouw naam]
```

---

## ✅ Checklist Deployment:

1. [ ] Icons gemaakt (icon-192.png, icon-512.png)
2. [ ] Firebase config ingevuld
3. [ ] GitHub account gemaakt
4. [ ] Repository gemaakt
5. [ ] Bestanden geüpload
6. [ ] GitHub Pages geactiveerd
7. [ ] URL getest op smartphone
8. [ ] URL getest op PC
9. [ ] PWA installatie getest
10. [ ] Offline functionaliteit getest
11. [ ] Dark mode getest
12. [ ] CSV export getest
13. [ ] Link gedeeld met team
14. [ ] Backup gemaakt van alle bestanden

---

**Succes met de deployment! 🚀**
