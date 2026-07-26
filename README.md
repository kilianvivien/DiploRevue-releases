# DiploRevue — distribution

Ce dépôt ne contient aucun code source. Il sert uniquement à distribuer les
binaires signés de [DiploRevue](https://github.com/kilianvivien/DiploRevue)
et le manifeste `latest.json` que lit le système de mise à jour automatique
de l'application de bureau.

Le code source reste privé. Seuls les paquets d'installation publiés ici sont
publics, parce que le client de mise à jour Tauri interroge son point d'entrée
sans authentification et ne peut donc pas lire un dépôt privé.

## Installer DiploRevue

Rendez-vous sur la [dernière version](https://github.com/kilianvivien/DiploRevue-releases/releases/latest)
et téléchargez le paquet correspondant à votre système :

| Système | Fichier |
| --- | --- |
| macOS (Intel et Apple Silicon) | `DiploRevue_<version>_universal.dmg` |
| Windows | `DiploRevue_<version>_x64_en-US.msi` ou `DiploRevue_<version>_x64-setup.exe` |
| Linux (AppImage) | `DiploRevue_<version>_amd64.AppImage` |
| Linux (Debian/Ubuntu) | `DiploRevue_<version>_amd64.deb` |
| Linux (Fedora/RHEL) | `DiploRevue-<version>-1.x86_64.rpm` |

Une fois l'application installée, les versions suivantes sont proposées
automatiquement depuis l'application.

## Publication

Les versions sont construites dans le dépôt privé, puis recopiées ici par le
workflow `Release`. Ne publiez rien à la main dans ce dépôt : le manifeste
`latest.json` contient des URL réécrites vers ce dépôt et une signature par
paquet, qu'un envoi manuel désynchroniserait.
