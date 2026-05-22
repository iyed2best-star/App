# 🪟 Guide Installation EXE Windows

## 📥 Télécharger l'Application

### Option 1: Direct Download
```
https://github.com/iyed2best-star/App/releases/download/v1.0.0/ai_app.exe
```

### Option 2: Build depuis le code source
```bash
git clone --branch feature/cross-platform-ai https://github.com/iyed2best-star/App.git
cd App
build_windows.bat
```

## 💾 Installation

### Méthode 1: Exécution Directe (Simple)
1. **Double-clic** sur `ai_app.exe`
2. **Attendre** le chargement
3. **Profiter!** 🎉

### Méthode 2: Créer un Raccourci (Bureau)
1. **Clic droit** sur `ai_app.exe`
2. **"Créer un raccourci"**
3. **Glisser** vers le bureau

### Méthode 3: Installer dans Program Files
1. **Créer** dossier `C:\Program Files\AI App\`
2. **Copier** `ai_app.exe` dedans
3. **Créer** raccourci depuis `ai_app.exe`
4. **Ajouter** à menu Démarrage (optionnel)

## 🔧 Configuration Système

### Prérequis
- Windows 10/11 (64-bit)
- 150 MB d'espace libre
- Connexion internet (pour IA)

### Dépendances (Si absent)
Télécharger et installer:
- [Visual C++ Redistributable](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads)
- [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/net48)

```batch
REM Install automatiquement
vcredist_x64.exe /install /quiet /norestart
```

## ⚙️ Paramètres Windows

### Pour Utiliser la Caméra (OCR)
```
Settings → Privacy & Security → Camera → Allow apps to access camera
→ Toggle ON for "AI App"
```

### Pour Microphone (futur)
```
Settings → Privacy & Security → Microphone → Allow
```

### Pare-feu Windows
Si **bloqué par le pare-feu**:

1. **Ouvrir** Windows Defender Firewall
2. **Click** "Allow app through firewall"
3. **Check** "AI App"
4. **OK**

Ou via PowerShell (Admin):
```powershell
New-NetFirewallRule -DisplayName "AI App" -Direction Inbound -Program "C:\Program Files\AI App\ai_app.exe" -Action Allow
```

## 📱 Premiers Pas

### 1️⃣ Ajouter Clé API
Au premier lancement:
```
Settings → API Configuration
Coller clé: sk-proj-qAT6ZGp5...
```

### 2️⃣ Permissions
- ✅ **Camera** - Pour OCR
- ✅ **Photos** - Pour galerie
- ✅ **Internet** - Pour chat IA
- ✅ **Storage** - Pour cache

### 3️⃣ Choisir Langue
```
Settings → Language
Options: 🇫🇷 FR | 🇬🇧 EN | 🇪🇸 ES | 🇩🇪 DE
```

## 🎮 Utilisation

### 💬 Chat IA
```
1. Click "Chat IA"
2. Taper message
3. Attendre réponse GPT-3.5
```

### 📸 Reconnaissance d'Images
```
1. Click "OCR"
2. Prendre photo ou importer
3. Texte extrait automatiquement
```

### 🌍 Traduction
```
1. Click "Traduction"
2. Sélectionner langue
3. Taper/Coller texte
4. Résultat instantané
```

## 🔒 Sécurité

### Certificat SSL
L'app utilise HTTPS pour API:
```
✅ Connexion sécurisée
✅ Données chiffrées
✅ Pas de keylogger
```

### Clé API
```
🔐 Stockée localement (pas cloud)
🔐 Jamais transmise à tiers
🔐 Supprimable dans settings
```

### Antivirus
- Tous les builds signés numériquement
- Aucun malware/spyware
- Scans réguliers

## 🐛 Dépannage

### "Fichier non trouvé"
```
❌ Solution:
1. Vérifier chemin d'installation
2. Réinstaller l'app
3. Vérifier les permissions
```

### "Accès refusé"
```
❌ Solution:
1. Lancer en tant qu'administrateur (clic droit)
2. Désactiver antivirus temporairement
3. Ajouter exception pare-feu
```

### "App ne démarre pas"
```
❌ Solution:
1. Vérifier .NET Framework 4.8
2. Installer Visual C++ Redistributable
3. Redémarrer l'ordinateur
```

### "Camera ne fonctionne pas"
```
❌ Solution:
1. Vérifier permissions Windows
2. Redémarrer app
3. Vérifier câble/driver caméra
```

### "Pas de connexion API"
```
❌ Solution:
1. Vérifier connexion internet
2. Vérifier clé API
3. Vérifier pare-feu Windows
```

## 🔄 Mise à Jour

### Vérifier version
```
Help → About
Version: 1.0.0 (Build 2024)
```

### Mettre à Jour
```
1. Télécharger nouvelle version
2. Backup clé API (settings)
3. Remplacer ai_app.exe
4. Redémarrer app
```

### Auto-Update (futur)
```
Help → Check for Updates
Télécharge auto si disponible
```

## 📊 Logs & Diagnostics

### Fichier Log
```
C:\Users\[YourUser]\AppData\Local\AI App\logs\app.log
```

### Ouvrir dans Notepad++
```powershell
notepad++ $env:APPDATA\..\Local\AI App\logs\app.log
```

### Envoyer Logs Support
```
Click "Help" → "Send Logs"
Ou copier vers: support@aiapp.dev
```

## 📦 Désinstallation

### Méthode 1: Suppression Simple
```
1. Delete ai_app.exe
2. Delete raccourci bureau
3. C'est tout! 🎉
```

### Méthode 2: Cleanup Complet
```powershell
# Supprimer dossier config
Remove-Item $env:APPDATA\..\Local\AI App -Recurse -Force

# Supprimer du registre
reg delete "HKEY_CURRENT_USER\Software\AI App" /f
```

### Méthode 3: Installer Manager (à venir)
```
Control Panel → Programs → Uninstall Program
Search "AI App" → Uninstall
```

## 💡 Tips & Tricks

### Shortcut Clavier
- `Ctrl+N` - Nouveau chat
- `Ctrl+C` - Copier réponse
- `Ctrl+S` - Sauvegarder
- `Ctrl+Q` - Quitter

### Performance
- Fermer apps inutiles
- Vérifier RAM libre (min 4GB)
- Désactiver extensions navigateur

### Batterie (Laptop)
- Mode Eco dans settings
- Réduire refresh rate
- Fermer onglets inutilisés

## 🌐 Support Multilingue

```
🇫🇷 Français ✅
🇬🇧 English ✅
🇪🇸 Español ✅
🇩🇪 Deutsch ✅
🇸🇦 العربية ✅
🇨🇳 中文 ✅
```

## 📞 Besoin d'Aide?

1. **FAQ**: [https://github.com/iyed2best-star/App/wiki](FAQ)
2. **Issues**: [Ouvrir issue](https://github.com/iyed2best-star/App/issues)
3. **Email**: support@aiapp.dev
4. **Discord**: [Rejoindre serveur](discord.gg/aiapp)

## 🎯 Features Prochaines

- 🎤 Reconnaissance vocale
- 📊 Analyse documents
- 🔄 Sync cloud
- 🎨 Themes personnalisés
- 🤖 Chat offline mode

---

**✨ Profite de l'IA sur Windows! Partage & évalue! ⭐**
