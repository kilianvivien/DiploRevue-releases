<div align="center">

<img src="assets/icon.png" alt="DiploRevue" width="160" height="160" />

# DiploRevue

**Générateur moderne de revues de presse pour les professionnels de la diplomatie et de l'information**

[![Dernière version](https://img.shields.io/github/v/release/kilianvivien/DiploRevue-releases?label=derni%C3%A8re%20version&color=blue)](https://github.com/kilianvivien/DiploRevue-releases/releases/latest)

<sub>macOS universel · Apple Silicon et Intel — stockage local, orienté confidentialité</sub>

<a href="#quest-ce-que-diplorevue-">Présentation</a> ·
<a href="#installer-lapplication">Installer</a> ·
<a href="#mettre-à-jour">Mettre à jour</a> ·
<a href="#questions-fréquentes">FAQ</a>

</div>

---

## Qu'est-ce que DiploRevue ?

DiploRevue est une application de bureau qui sert à préparer, rédiger et diffuser des revues de
presse professionnelles. Elle réunit un éditeur structuré, l'import de sources PDF, DOCX et RSS,
une assistance IA multi-fournisseurs et des exports prêts à l'envoi en HTML, e-mail, DOCX ou PDF.
Elle s'adresse aux diplomates, analystes, journalistes et équipes de veille qui doivent transformer
rapidement des sources hétérogènes en synthèses éditoriales propres et vérifiables. Vos revues sont
enregistrées localement sur votre machine, pas sur un serveur distant.

---

## À propos de ce dépôt

Ce dépôt **ne contient pas le code source** de DiploRevue. Il ne sert qu'à **distribuer
l'application** : vous y trouvez les fichiers d'installation de chaque version, ainsi que le fichier
que l'application consulte pour savoir si une mise à jour est disponible.

C'est donc l'endroit où télécharger DiploRevue, et rien d'autre. Le code source est développé
séparément et n'est pas public.

---

## Nouveautés de la version 2.2.2

- Modèles Mistral : GLM 5.3, Mistral Large 4, DeepSeek V4.1 Flash 1017 et GLM 5.3 Flash disponibles en génération et en traduction.
- SDK Google GenAI 2.31.0 et dépendances de l’éditeur, des exports et du bureau actualisées.
- Correctifs de sécurité des dépendances réseau et de test, sans changement du format des données.

[Consulter les notes et télécharger DiploRevue 2.2.2](https://github.com/kilianvivien/DiploRevue-releases/releases/tag/v2.2.2).

---

## Installer l'application

**1. Téléchargez le paquet macOS universel** depuis la
[dernière version](https://github.com/kilianvivien/DiploRevue-releases/releases/latest)
(section « Assets », en bas de la page).

| Votre système | Fichier à télécharger |
| --- | --- |
| **macOS** (Intel et Apple Silicon) | `DiploRevue_<version>_universal.dmg` |

Les autres fichiers de la liste (`.sig`, `.app.tar.gz`) servent uniquement au mécanisme de mise à
jour automatique. **Vous n'avez pas à les télécharger.**

Depuis la version 2.0.2, les nouvelles releases distribuent uniquement le paquet macOS universel. Les anciennes versions Windows et Linux restent accessibles dans l’historique des releases.

**2. Installez l’application sur votre Mac :**

<details open>
<summary><b>macOS</b></summary>

### Installation

1. Ouvrez le fichier `.dmg` téléchargé.
2. Glissez l'icône **DiploRevue** dans le dossier **Applications**.
3. Éjectez l'image disque, puis ouvrez **Applications** et double-cliquez sur **DiploRevue**.

### Autoriser l'application au premier lancement

Au tout premier lancement, macOS **bloque** l'application et affiche un message du type
« *Apple n'a pas pu vérifier que « DiploRevue » ne contient pas de logiciel malveillant* ».

C'est normal et attendu : DiploRevue n'est pas distribuée via l'App Store et n'est pas signée
avec un certificat de développeur Apple payant. Le message ne signale pas un problème avec le
fichier que vous avez téléchargé. Voici comment autoriser l'application — **une seule fois** :

1. **Double-cliquez sur DiploRevue.** Le blocage apparaît. Cliquez sur **Terminé**.
   > ⚠️ Cliquez bien sur **Terminé**, surtout pas sur **Déplacer vers la corbeille**. Cette
   > première tentative est indispensable : c'est elle qui fait apparaître le bouton
   > d'autorisation à l'étape suivante.
2. Ouvrez le menu  (en haut à gauche de l'écran) → **Réglages Système**.
3. Dans la colonne de gauche, choisissez **Confidentialité et sécurité**.
4. **Faites défiler jusqu'en bas** de la page, jusqu'à la section **Sécurité**. Vous y lisez :
   *« « DiploRevue » a été bloqué pour protéger votre Mac. »*
5. Cliquez sur le bouton **Ouvrir quand même**, à droite de ce message.
6. Authentifiez-vous avec **Touch ID** ou votre **mot de passe de session**.
7. Une dernière fenêtre de confirmation s'affiche : cliquez à nouveau sur **Ouvrir quand même**.

DiploRevue s'ouvre, et l'autorisation est mémorisée : **les lancements suivants se font
normalement, d'un simple double-clic.** Vous n'aurez pas à recommencer, y compris après les
mises à jour automatiques.

> **Le bouton « Ouvrir quand même » n'apparaît pas ?**
> Il ne s'affiche que pendant **environ une heure** après la tentative de lancement bloquée, et
> uniquement si celle-ci a bien eu lieu. Revenez à l'étape 1, double-cliquez sur l'application
> pour déclencher le blocage, puis retournez immédiatement dans **Confidentialité et sécurité**.

> **Le clic droit → « Ouvrir » ne fonctionne plus.**
> Cette astuce, très répandue dans les tutoriels plus anciens, a été **supprimée par Apple à
> partir de macOS 15 Sequoia**. Sur macOS 15, macOS 26 Tahoe et versions ultérieures, le passage
> par **Réglages Système → Confidentialité et sécurité** décrit ci-dessus est le seul moyen
> d'autoriser l'application.

### Si macOS affirme que l'application « est endommagée »

Ce message apparaît lorsque l'attribut de quarantaine appliqué aux fichiers téléchargés empêche
l'ouverture. Ouvrez **Terminal** (Applications → Utilitaires), exécutez la commande suivante,
saisissez votre mot de passe si demandé, puis relancez DiploRevue :

```bash
xattr -dr com.apple.quarantine /Applications/DiploRevue.app
```

</details>

---

## Mettre à jour

**Vous n'avez rien à faire.** Une fois DiploRevue installé, l'application vérifie d'elle-même s'il
existe une version plus récente et vous la propose dans une fenêtre listant les nouveautés.

Quand vous acceptez :

1. La nouvelle version est téléchargée automatiquement.
2. Sa **signature cryptographique est vérifiée** avant toute installation — si le fichier avait été
   modifié en chemin, l'installation serait refusée.
3. L'application redémarre pour terminer la mise à jour.

Vous n'avez donc besoin de revenir sur cette page que pour votre **première** installation, ou pour
réinstaller l'application depuis zéro.

> Les mises à jour automatiques décrites ici concernent l’application macOS.

---

## Questions fréquentes

**Mes revues sont-elles envoyées quelque part ?**
Non. Vos revues sont enregistrées localement, sur votre machine. Les seules données qui sortent de
l'application sont celles que vous transmettez explicitement à un fournisseur d'IA en utilisant les
fonctions d'assistance, et les exports que vous choisissez de diffuser.

**Une mise à jour va-t-elle effacer mon travail ?**
Non. La mise à jour remplace l'application, pas vos données.

**Puis-je revenir à une version précédente ?**
Oui. Toutes les versions restent disponibles sur la page
[Releases](https://github.com/kilianvivien/DiploRevue-releases/releases) ; téléchargez celle qui
vous intéresse et installez-la par-dessus.

**Quelle version ai-je installée ?**
Ouvrez **Paramètres** dans l'application : le numéro de version y est affiché.

**J'ai trouvé un bug.**
Ouvrez un ticket dans l'onglet
[Issues](https://github.com/kilianvivien/DiploRevue-releases/issues) de ce dépôt, en précisant
votre système et votre version de DiploRevue.
