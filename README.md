# 📻 Radio Adamowo

**Słuchaj szumu prawdy w eterze manipulacji**

Radio Adamowo to edukacyjna aplikacja webowa Progressive Web App (PWA) poświęcona zwiększaniu świadomości na temat toksycznych relacji i manipulacji psychologicznej. Projekt oferuje interaktywne narzędzia edukacyjne, streaming audio oraz poradniki dotyczące rozpoznawania i radzenia sobie z manipulacją.

## ✨ Funkcjonalności

### 🎵 **Odtwarzacz Audio/Radio**
- Stream na żywo z HLS.js
- Lokalne playlisty (ambient, disco, hip-hop)
- Podcasty edukacyjne
- Kontrolki mediów z Media Session API
- Wizualizer audio w czasie rzeczywistym

### 📱 **Progressive Web App (PWA)**
- Instalacja na urządzeniu mobilnym i desktop
- Działanie offline z Service Worker
- Responsywny design
- Inteligentny system cache'owania

### 🎓 **Narzędzia Edukacyjne**
- **Poradnik "8 Grzechów Toksycznych Osób"** - szczegółowy przewodnik rozpoznawania manipulacji
- **Symulator AI** - interaktywne doświadczenie manipulacji psychologicznej
- **Galeria Studio** - zdjęcia i materiały z programu
- **Materiały wideo** - dokumentalne treści edukacyjne

### 🔧 **Zaawansowane Funkcje**
- Notatki z kalendarzem wydarzeń
- Integracja z Media Session API
- Automatyczny cache mediów
- Obsługa gestów i skrótów klawiszowych

## 🚀 Instalacja i Uruchomienie

### Wymagania
- Node.js >= 18.0.0
- pnpm >= 8.0.0 (zalecane) lub npm

### Szybkie uruchomienie

```bash
# Klonowanie repozytorium
git clone https://github.com/RudyKotJeKoc/ADAMOWO_MGX.git
cd ADAMOWO_MGX

# Instalacja zależności
pnpm install

# Uruchomienie serwera deweloperskiego
pnpm run dev

# Zbudowanie wersji produkcyjnej
pnpm run build

# Podgląd wersji produkcyjnej
pnpm run preview
```

### Konfiguracja Stream URL

Aby skonfigurować rzeczywisty stream audio, edytuj plik `script.js`:

```javascript
// Zmień URL na rzeczywisty adres streamu
const STREAM_URL = 'https://your-radio-stream.com/stream.m3u8';
```

## 📁 Struktura Projektu

```
ADAMOWO_MGX/
├── index.html              # Główna strona aplikacji
├── style.css              # Style CSS z obsługą animacji
├── script.js              # Główna logika JavaScript
├── sw.js                  # Service Worker (PWA)
├── manifest.json          # Manifest PWA
├── vite.config.js         # Konfiguracja Vite
├── package.json           # Konfiguracja projektu i dependencies
├── playlist.json          # Konfiguracja playlist
├── robots.txt             # Konfiguracja SEO
├── public/
│   ├── images/studio/     # Zdjęcia studia (wymagane: studio-1.png do studio-4.png)
│   ├── video/            # Pliki wideo (sprawa-adamowo.mp4)
│   └── data/             # Dodatkowe dane JSON
├── audio/                # Pliki audio/podcasty
└── music/                # Pliki muzyczne
```

## 🎨 Personalizacja

### Kolory i Motyw
Główne zmienne CSS w `style.css`:
```css
:root {
    --color-primary: #f59e0b;     /* amber-500 */
    --color-secondary: #dc2626;   /* red-600 */
    --color-background: #000000;  /* black */
    --color-text: #e0e0e0;        /* light gray */
}
```

### Dodawanie Mediów

1. **Zdjęcia studia**: Umieść pliki w `public/images/studio/`
   - `studio-1.png` - główne zdjęcie studia
   - `studio-2.png` - serce radia
   - `studio-3.png` - ekspertka
   - `studio-4.png` - prowadzący

2. **Audio/Podcasty**: Umieść pliki w katalogu `audio/`

3. **Materiały wideo**: Umieść w `public/video/`

## 🔧 Funkcjonalności Techniczne

### Service Worker i PWA
- **Static Cache**: Podstawowe pliki aplikacji
- **Dynamic Cache**: Media i treści dynamiczne
- **Offline Support**: Aplikacja działa bez połączenia internetowego
- **Background Sync**: Synchronizacja danych w tle

### Bezpieczeństwo i Prywatność
- Brak zewnętrznych trackerów
- Lokalne przechowywanie danych
- CSP (Content Security Policy) ready
- HTTPS ready

### Performance
- Lazy loading obrazów
- Optimized caching strategy
- Minimalne zależności zewnętrzne
- Progressive loading

## 📋 Dostępne Skrypty

```bash
# Development
pnpm run dev          # Serwer developerski na porcie 3000

# Production
pnpm run build        # Budowanie wersji produkcyjnej
pnpm run preview      # Podgląd buildu na porcie 4173

# Maintenance
pnpm run lint         # Sprawdzenie kodu
pnpm run serve        # Alias dla preview
```

## 🌐 Deployment

### Vite Build
```bash
pnpm run build
```

Pliki gotowe do deployment znajdą się w folderze `dist/`.

### Zalecane Platformy
- **Netlify**: Automatyczny deployment z GitHub
- **Vercel**: Optimized dla aplikacji PWA
- **GitHub Pages**: Darmowy hosting statyczny
- **Firebase Hosting**: Zaawansowane funkcje PWA

### Konfiguracja HTTPS
Aplikacja wymaga HTTPS dla pełnej funkcjonalności PWA:
- Service Worker
- Media Session API
- Push notifications (opcjonalnie)

## 🔍 SEO i Dostępność

### Meta Tagi
- Open Graph dla social media
- Twitter Cards
- Strukturalne dane JSON-LD
- Meta description i keywords

### Dostępność (a11y)
- ARIA labels dla interaktywnych elementów
- Semantic HTML
- Keyboard navigation
- Screen reader support

## 🐛 Troubleshooting

### Najczęstsze Problemy

1. **Stream nie działa**: Sprawdź STREAM_URL w `script.js`
2. **PWA nie instaluje się**: Wymagany HTTPS
3. **Brak audio**: Sprawdź czy pliki istnieją w katalogach
4. **Service Worker nie działa**: Wyczyść cache przeglądarki

### Debug Mode
Włącz konsole deweloperską (F12) aby zobaczyć logi aplikacji.

## 📄 Licencja

ISC License - szczegóły w pliku LICENSE

## 👥 Kontakt

**Radio Adamowo Team**  
🌐 Website: https://radio-adamowo.com  
📧 Email: contact@radio-adamowo.com

---

## ⚠️ Ważne Uwagi

- Aplikacja zawiera treści edukacyjne dotyczące przemocy psychologicznej
- Materiały przeznaczone są wyłącznie do celów informacyjnych i edukacyjnych  
- W przypadku sytuacji kryzysowej skontaktuj się z odpowiednimi służbami pomocy

**Telefony zaufania:**
- Niebieska Linia: 800 120 002
- Centrum Praw Kobiet: 800 120 226