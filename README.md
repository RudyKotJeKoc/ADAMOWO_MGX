# 📻 Radio Adamowo

**Słuchaj szumu prawdy w eterze manipulacji.**

Radio Adamowo to edukacyjna aplikacja webowa (PWA) poświęcona analizie toksycznych relacji i manipulacji psychologicznej. Projekt zawiera interaktywne audycje, materiały edukacyjne oraz narzędzia do rozpoznawania wzorców przemocy psychologicznej.

## ✨ Funkcje

- 🎵 **Webowe radio** z różnymi playlistami muzycznymi (546 utworów w 5 kategoriach)
- 🎙️ **Audycje analityczne** o manipulacji psychologicznej (16 podcastów edukacyjnych)
- 📱 **Progressive Web App** - możliwość instalacji na telefonie
- 🎬 **Materiały wideo** dokumentalne
- 🖼️ **Galeria studia** radiowego
- 🎯 **Interaktywne narzędzia** edukacyjne (AI chat, kalendarz notatek)
- 📚 **Poradniki** rozpoznawania toksycznych zachowań
- **Responsywny design** na wszystkie urządzenia

## 📁 Struktura plików

```
/
├── index.html              # Strona główna
├── style.css               # Style CSS
├── script.js               # JavaScript
├── playlist.json           # Lista utworów
├── manifest.json           # Manifest PWA
├── sw.js                   # Service Worker
├── .htaccess              # Konfiguracja Apache
├── robots.txt             # SEO
├── music/                 # Pliki muzyczne (546 plików)
│   ├── Utwor (1-357).mp3
│   ├── barbara/           # 46 plików
│   ├── disco/             # 25 plików
│   ├── hiphop/            # 53 pliki
│   └── kids/              # 46 plików
├── audio/                 # Podcasty (16 plików)
└── public/
    ├── images/studio/     # Zdjęcia studia (4 pliki)
    └── video/             # Materiał wideo
```

## 🚀 Instalacja

1. **Skopiuj wszystkie pliki** do folderu `www` na serwerze
2. **Dodaj pliki multimedialne**:
   - 546 plików MP3 do folderów `music/`
   - 16 podcastów do `audio/`
   - 4 zdjęcia studia do `public/images/studio/`
   - Materiał wideo do `public/video/`
3. **Skonfiguruj serwer** (Apache z .htaccess lub Nginx)

## 📱 PWA

Aplikacja obsługuje Progressive Web App:
- Instalowalna na urządzeniach mobilnych
- Działanie offline (cache)
- Powiadomienia push
- Kontrola multimediów z poziomu systemu

## 🔧 Wymagania serwera

- **Serwer web**: Apache/Nginx
- **PHP**: Opcjonalnie (dla zaawansowanych funkcji)
- **HTTPS**: Zalecane dla PWA
- **Kompresja**: Gzip/Deflate
- **MIME types**: audio/mpeg, video/mp4

## 📞 Wsparcie

W przypadku problemów technicznych sprawdź:
1. Czy wszystkie pliki zostały wgrane
2. Czy serwer obsługuje pliki .htaccess
3. Czy MIME types są poprawnie skonfigurowane
4. Czy ścieżki do plików są poprawne

## 📄 Licencja

Projekt edukacyjny - Radio Adamowo © 2025