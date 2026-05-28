# SecureStorageLabJava 🔐

Application Android (Java) démontrant la persistance locale sécurisée des données.

## 📋 Description

Lab 14 – Programmation Mobile : Android avec Java  

Ce projet illustre les bonnes pratiques de stockage local sous Android :
- SharedPreferences (données non sensibles)
- EncryptedSharedPreferences (tokens/secrets)
- Fichiers internes (texte UTF-8, JSON)
- Cache temporaire (cacheDir)
- Stockage externe app-specific

## 🎥 Vidéo Démo

[![Démo](https://img.shields.io/badge/▶-Voir%20la%20démo-red)](https://youtu.be/oAXwV642xMk?si=8Dw8-UmeTIvkeCc7)

## 🏗️ Architecture
com.example.securestoragejava/
├── ui/          → MainActivity
├── prefs/       → AppPrefs, SecurePrefs
├── files/       → InternalTextStore, StudentsJsonStore
├── cache/       → CacheStore
├── external/    → ExternalAppFilesStore
└── model/       → Student

## ✅ Fonctionnalités

| Fonctionnalité | Description |
|---|---|
| Sauvegarder prefs | Sauvegarde nom, langue, thème |
| Charger prefs | Restaure les préférences |
| Token chiffré | Stockage sécurisé via EncryptedSharedPreferences |
| Sauvegarder JSON | Écrit students.json en stockage interne |
| Charger JSON | Lit et affiche la liste des étudiants |
| Effacer | Nettoyage complet de toutes les données |

## 🔒 Checklist Sécurité

- ✅ Aucun token dans les logs
- ✅ EncryptedSharedPreferences pour les secrets
- ✅ MODE_PRIVATE pour les fichiers internes
- ✅ Token masqué à l'écran
- ✅ Nettoyage complet disponible
- ✅ Encodage UTF-8 imposé
- ✅ Exceptions gérées sans fuite d'informations

## 🛠️ Technologies

- Java
- Android SDK (API 24+)
- AndroidX Security Crypto 1.1.0-alpha06
- org.json

## ▶️ Lancer le projet

1. Cloner le repo
2. Ouvrir avec Android Studio
3. Sync Gradle
4. Lancer sur émulateur API 24+
