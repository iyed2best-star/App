# Application IA Multi-Plateforme 🌍

Application **cross-platform** avec un seul codebase Flutter compilé pour **Windows, macOS, iOS et Android**.

## 🎯 Plateformes Supportées

| OS | Format | Status | Commande |
|----|--------|--------|----------|
| 🪟 **Windows** | `.exe` | ✅ | `build_windows.bat` |
| 🍎 **macOS** | `.app` / `.dmg` | ✅ | `build_macos.sh` |
| 🔶 **iOS** | `.ipa` | ✅ | `build_ios.sh` |
| 🤖 **Android** | `.apk` / `.aab` | ✅ | `flutter build apk --release` |

## 📦 Features IA

- 💬 **Chat en temps réel** avec GPT-3.5-turbo
- 📸 **OCR & Reconnaissance d'images** (Google ML Kit)
- 🌍 **Traduction** - 6 langues (FR, EN, ES, DE, AR, ZH)
- 🎨 **Dark Mode** - Automatique sur tous les OS
- 🔒 **Sécurisé** - Clé API chiffrée localement

## 🚀 Installation Rapide

### Prérequis
```bash
# Windows
choco install flutter

# macOS
brew install flutter

# ou télécharger depuis https://flutter.dev
```

## 🪟 BUILD WINDOWS (.EXE)

### Méthode 1: Script automatique
```batch
double-click build_windows.bat
```

### Méthode 2: Manuel
```bash
cd flutter_app
flutter pub get
flutter build windows --release

# EXE créé à:
# build\windows\runner\Release\ai_app.exe
```

### ✅ Résultat
- **Fichier**: `ai_app.exe` (~150MB)
- **Installation**: Directe sans dépendance
- **Distribution**: Windows Store / Direct download

---

## 🍎 BUILD macOS (.APP / .DMG)

### Méthode 1: Script automatique
```bash
chmod +x build_macos.sh
./build_macos.sh
```

### Méthode 2: Manuel
```bash
cd flutter_app
flutter pub get
flutter build macos --release

# APP créée à:
# build/macos/Build/Products/Release/ai_app.app
```

### ✅ Résultat
- **Fichier**: `ai_app.app` (~130MB)
- **DMG**: `ai_app.dmg` (~120MB)
- **Distribution**: Mac App Store / Direct download

---

## 🔶 BUILD iOS (.IPA)

### Prérequis
```bash
# Xcode 14+ installé
# Apple Developer Account
# Certificate & Provisioning Profile
```

### Méthode 1: Script automatique
```bash
chmod +x build_ios.sh
./build_ios.sh
```

### Méthode 2: Manuel
```bash
cd flutter_app
flutter pub get
flutter build ios --release

# Puis signer avec Xcode
```

### ✅ Résultat
- **Fichier**: `ai_app.ipa` (~80MB)
- **Distribution**: App Store / TestFlight

---

## 🤖 BUILD Android (.APK / .AAB)

### Méthode rapide
```bash
cd flutter_app

# APK (direct installation)
flutter build apk --release

# AAB (Google Play Store)
flutter build appbundle --release
```

### ✅ Résultat
- **APK**: `app-release.apk` (~60MB)
- **AAB**: `app-release.aab` (~50MB)

---

## 📂 Structure du Projet

```
feature/cross-platform-ai/
├── flutter_app/
│   ├── lib/
│   │   ├── main.dart
│   │   ├── screens/
│   │   │   ├── home_screen.dart
│   │   │   ├── chat_screen.dart
│   │   │   ├── ocr_screen.dart
│   │   │   └── translation_screen.dart
│   │   ├── models/
│   │   ├── services/
│   │   └── widgets/
│   ├── android/           # Android native code
│   ├── ios/               # iOS native code
│   ├── windows/           # Windows native code
│   ├── macos/             # macOS native code
│   ├── pubspec.yaml
│   └── pubspec.lock
├── build_windows.bat      # Script build Windows
├── build_macos.sh         # Script build macOS
├── build_ios.sh           # Script build iOS
├── README_CROSS_PLATFORM.md
└── INSTALLATION_EXE.md
```

## 🔧 Configuration

### Clé API OpenAI
```dart
// lib/services/api_client.dart
const String OPENAI_API_KEY = 'sk-proj-qAT6ZGp5...';
```

### Permissions

#### Windows
```xml
<!-- windows/runner/Runner.rc -->
<!-- Accès internet automatique -->
```

#### macOS
```xml
<!-- macos/Runner/Info.plist -->
<key>NSCameraUsageDescription</key>
<string>L'app a besoin d'accès à la caméra pour OCR</string>
```

#### iOS
```xml
<!-- ios/Runner/Info.plist -->
<key>NSCameraUsageDescription</key>
<string>L'app a besoin d'accès à la caméra</string>
<key>NSPhotoLibraryUsageDescription</key>
<string>L'app a besoin d'accès à la galerie</string>
```

#### Android
```xml
<!-- android/app/src/main/AndroidManifest.xml -->
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
```

## 📊 Comparaison

| Aspect | Web | Natif | Flutter |
|--------|-----|-------|---------|
| Performance | Moyenne | Haute | Haute ✅ |
| Installation | N/A | Complexe | Simple ✅ |
| Codebase | 1 | 4 | 1 ✅ |
| Maintenance | Simple | Complexe | Simple ✅ |
| UX | Web | Natif | Natif ✅ |
| Taille | Petite | Grande | Moyenne ✅ |

## 🎯 Distribution

### Windows
1. **Portable**: Distribuer `.exe` directement
2. **Installer**: Créer avec NSIS/Inno Setup
3. **Store**: Publier sur Microsoft Store

### macOS
1. **Direct**: Partager `.dmg`
2. **App Store**: Publier via Mac App Store
3. **Homebrew**: `brew install ai-app`

### iOS
1. **App Store**: Processus officiel Apple
2. **TestFlight**: Distribution beta
3. **Enterprise**: Distribution interne

### Android
1. **Google Play**: Publication officielle
2. **F-Droid**: Store alternatif
3. **Direct**: Partager `.apk`

## ⚡ Optimisations

- Release builds avec optimisations
- Minification de code
- Compression d'assets
- Caching local
- Offline support

## 🐛 Debugging

### Windows
```bash
flutter run -v
flutter run --release
```

### macOS
```bash
flutter run -v --profile
open build/macos/Build/Products/Release/ai_app.app
```

### iOS
```bash
flutter run -v --profile
# Ou ouvrir avec Xcode
open ios/Runner.xcworkspace
```

### Android
```bash
flutter run -v
# Ou via Android Studio
```

## 📝 Checklist Publication

- [ ] Tester sur tous les OS
- [ ] Vérifier permissions
- [ ] Signer les builds
- [ ] Optimiser taille
- [ ] Créer icons & screenshots
- [ ] Rédiger descriptions
- [ ] Publier sur stores

## 🔗 Liens Utiles

- [Flutter Documentation](https://flutter.dev/docs)
- [Windows Desktop Support](https://flutter.dev/desktop)
- [macOS Desktop Support](https://flutter.dev/mac)
- [iOS App Store](https://developer.apple.com/app-store)
- [Google Play Store](https://play.google.com/console)

## 📞 Support

Pour questions/issues:
1. Vérifier [Flutter Issues](https://github.com/flutter/flutter/issues)
2. Consulter [Stack Overflow](https://stackoverflow.com/questions/tagged/flutter)
3. Ouvrir issue sur ce repo

---

**🚀 1 Codebase → 4 Plateformes Natives → Zéro Duplication!**
