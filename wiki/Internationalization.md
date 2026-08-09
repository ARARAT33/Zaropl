# 🌍 Internationalization (i18n) System

## Overview

AWE_Forge supports **10 languages** with a complete translation system. Every user-facing string is stored in `LANG` and retrieved via `t(key)`.

## Supported Languages

| Code | Language | Flag |
|------|----------|------|
| `en` | English | 🇺🇸 |
| `hy` | Armenian (Հայերեն) | 🇦🇲 |
| `ru` | Russian (Русский) | 🇷🇺 |
| `zh` | Chinese (中文) | 🇨🇳 |
| `es` | Spanish (Español) | 🇪🇸 |
| `ar` | Arabic (العربية) | 🇸🇦 |
| `ja` | Japanese (日本語) | 🇯🇵 |
| `de` | German (Deutsch) | 🇩🇪 |
| `fr` | French (Français) | 🇫🇷 |
| `pt` | Portuguese (Português) | 🇧🇷 |

## How It Works

### Translation Function
```javascript
function t(key) {
  return (LANG[currentLang] || LANG.en)[key] || LANG.en[key] || key;
}
```
Three-tier fallback: current language → English → raw key.

### Language Switching
```javascript
function setLanguage(code) {
  currentLang = code;
  localStorage.setItem("awe-lang", code);
  updateLangUI();
  navigate("#" + currentPage); // Re-render
}
```

### RTL Support
Arabic sets `direction: "rtl"` — the layout flips automatically:
```javascript
document.documentElement.dir = l.direction === "rtl" ? "rtl" : "ltr";
```

### Translation Keys (164 total)
Navigation, Hero, Stats, Actions, UI, Tools, and ~100 more keys.

### Adding a New Language
Add a new dictionary in `LANG`:
```javascript
LANG["it"] = { name: "Italiano", flag: "🇮🇹", code: "it", home: "Inizio", ... };
```
The language automatically appears in the dropdown.

### Persistence
Language preference saved to localStorage on every change, restored on page load.