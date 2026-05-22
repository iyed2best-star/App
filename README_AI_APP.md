# Application IA Android

Une application Android complète avec **3 modules IA intégrés**.

## 🚀 Fonctionnalités

### 1️⃣ Chat IA Intelligent
- Conversation en temps réel avec OpenAI GPT-3.5-turbo
- Interface élégante avec RecyclerView
- Gestion asynchrone avec Coroutines

### 2️⃣ Reconnaissance d'Images (OCR)
- Capture via caméra en temps réel
- Import depuis la galerie
- Extraction de texte avec Google ML Kit
- Support multilingue

### 3️⃣ Traduction Instantanée
- 6 langues supportées
  - 🇫🇷 Français
  - 🇬🇧 Anglais
  - 🇪🇸 Espagnol
  - 🇩🇪 Allemand
  - 🇸🇦 Arabe
  - 🇨🇳 Chinois
- Google ML Kit Translation

## 📦 Architecture

```
app/
├── ui/               # Activities
├── model/            # Data models
├── adapter/          # RecyclerView adapters
├── network/          # API clients
└── res/
    ├── layout/       # XML layouts
    ├── drawable/     # Custom drawables
    └── values/       # Strings, colors, styles
```

## 🛠️ Technologies

- **Kotlin** - Langage moderne
- **Retrofit 2** - Client HTTP
- **Google ML Kit** - Vision & NLP
- **Coroutines** - Asynchrone
- **AndroidX** - Support library
- **Room Database** - Stockage local (optionnel)

## 📋 Prérequis

1. **API Key OpenAI**
   ```kotlin
   AIApiClient.setApiKey("your-api-key-here")
   ```

2. **Permissions dans AndroidManifest.xml**
   ```xml
   <uses-permission android:name="android.permission.INTERNET" />
   <uses-permission android:name="android.permission.CAMERA" />
   <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
   ```

## 🔧 Installation

1. Clone la branche `feature/ai-app`
2. Ouvre le projet dans Android Studio
3. Configure ta clé API OpenAI
4. Build & Run

## 📱 Déploiement

Utilise `codemagic.yaml` pour le CI/CD automatique:
```bash
flutter build apk --release
```

## 📄 Licence

MIT - Libre d'utilisation

---

**Développé avec ❤️ pour Android & IA**
