# 📱 PWA (Progressive Web App) Setup

## ✅ Wat is toegevoegd:

### 1. **Manifest.json**
- App naam: "24u Loop Leuven Tracker"
- Korte naam: "24u Loop"
- Standalone modus (volledige app ervaring)
- Humasol oranje theme color (#f2a342)
- Portrait orientatie

### 2. **Service Worker** 
- Offline functionaliteit (cache belangrijke bestanden)
- Automatische updates in de achtergrond
- Network-first strategie voor Firebase (altijd verse data)
- Cache-first voor statische resources (snellere laadtijd)

### 3. **PWA Meta Tags**
- Theme color voor browser UI
- Apple mobile web app support
- Icon links voor verschillende platformen

### 4. **Installeer Knop**
- Verschijnt automatisch als de app installeerbaar is
- Zichtbaar naast de dark mode toggle
- Verdwijnt na installatie

## 🎨 Icons Maken:

### Optie 1: Automatische Icons (Simpel)
1. Open `generate-icons.html` in je browser
2. Klik op "Download 192x192" en "Download 512x512"
3. Plaats beide PNG bestanden in de hoofdmap (zelfde folder als index.html)
4. Klaar! ✅

### Optie 2: Custom Icons (Professioneel)
1. Maak je eigen icon design met:
   - **192x192 pixels** (voor standaard icon)
   - **512x512 pixels** (voor high-res displays)
   - PNG formaat met transparante achtergrond optioneel
   - Gebruik Humasol kleuren: #f2a342 (oranje) en #863c14 (bruin)
   
2. Benoem ze als:
   - `icon-192.png`
   - `icon-512.png`
   
3. Plaats in de hoofdmap naast index.html

4. Tips voor goede PWA icons:
   - Gebruik eenvoudige, herkenbare vormen
   - Zorg voor goed contrast
   - Test op verschillende achtergronden
   - Vermijd kleine details (moeilijk zichtbaar op kleine schermen)

## 📲 Installatie Testen:

### Op Desktop (Chrome/Edge):
1. Open de app in Chrome of Edge
2. Kijk naar de adresbalk - er verschijnt een installatie icoon ⊕
3. Of: Menu → "App installeren" of "Installeren..."
4. De app wordt toegevoegd aan je startmenu/taakbalk

### Op Android:
1. Open de app in Chrome
2. Menu (⋮) → "App installeren" of "Toevoegen aan startscherm"
3. De app verschijnt op je home screen als een normale app
4. Opent in volledige scherm zonder browser UI

### Op iOS (iPhone/iPad):
1. Open de app in Safari
2. Deel knop (□↑) → "Zet op beginscherm"
3. Pas de naam aan indien gewenst
4. De app verschijnt op je home screen

## 🎯 Voordelen van PWA:

### ✅ App-achtige Ervaring
- Volledige scherm (geen browser UI)
- Eigen icoon op home screen
- Verschijnt in app-lijst van apparaat
- Snelle toegang vanaf home screen

### ✅ Offline Werking
- App laadt altijd (ook zonder internet)
- Timer blijft werken offline
- Data wordt lokaal opgeslagen
- Automatische sync wanneer online

### ✅ Betere Prestaties
- Snellere laadtijd door caching
- Minder data verbruik
- Werkt ook bij slechte verbinding
- Updates in de achtergrond

### ✅ Native-achtige Features
- Push notificaties mogelijk (kan later toegevoegd worden)
- Badge notifications op app icon
- Integratie met OS (bijv. delen vanuit andere apps)
- Werkt op alle platforms (Android, iOS, Desktop)

## 🔧 Technische Details:

### Service Worker Cache Strategie:
- **Statische bestanden**: Cache-first met background update
- **Firebase data**: Network-only (altijd verse data)
- **Offline fallback**: Toont offline pagina bij geen verbinding

### Automatische Updates:
- Service worker controleert elk minuut op updates
- Nieuwe versies worden automatisch geïnstalleerd
- Gebruikers krijgen altijd de laatste versie

### Browser Support:
- ✅ Chrome (Desktop & Android)
- ✅ Edge (Desktop & Android)
- ✅ Safari (iOS & macOS)
- ✅ Firefox (Desktop & Android)
- ✅ Opera (Desktop & Android)

## 🚀 Deployment Tips:

1. **HTTPS vereist**: PWA werkt alleen via HTTPS (localhost is OK voor testen)
2. **Manifest validatie**: Gebruik Chrome DevTools → Application → Manifest
3. **Service Worker testen**: Chrome DevTools → Application → Service Workers
4. **Icons controleren**: Chrome DevTools → Application → Icons

## 📱 Na Installatie:

De app werkt nu als een echte native app:
- Start vanaf home screen
- Geen browser UI meer
- Eigen venster/task in task switcher
- Blijft werken bij slechte/geen verbinding
- Automatische updates

Perfect voor het 24u event waarbij betrouwbaarheid cruciaal is! 🏃‍♂️💪
