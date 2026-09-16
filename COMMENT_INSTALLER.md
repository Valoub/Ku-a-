# Kuça — Transformer le projet en appli Android (.apk)

Tout le code est déjà prêt. Deux façons d'obtenir le fichier `.apk` final :

- **Option A — depuis ton téléphone, sans rien installer** (recommandée)
- **Option B — avec un ordinateur et Android Studio**

---

## Option A — Compiler dans le cloud (GitHub), depuis ton téléphone

Le projet contient déjà tout le nécessaire (`.github/workflows/build-apk.yml`)
pour que GitHub compile l'appli à ta place, sur ses propres serveurs.

1. Crée un compte gratuit sur https://github.com (si tu n'en as pas)
2. Crée un nouveau dépôt (bouton **"New repository"**), nomme-le par exemple
   `kuca-app`, laisse-le en **Public** ou **Private**, ne coche aucune case
   d'initialisation, puis clique **"Create repository"**
3. Sur la page qui suit, clique sur **"uploading an existing file"**
4. Depuis ton téléphone (ou ordinateur), sélectionne **tout le contenu** du
   dossier `kuca-app` de ce zip (pas le zip lui-même, ce qu'il y a dedans :
   `android`, `www`, `.github`, etc.) et dépose-le
5. Valide ("Commit changes")
6. Va dans l'onglet **"Actions"** en haut du dépôt : une compilation démarre
   automatiquement (icône ronde jaune → verte quand c'est fini, ~5-10 min)
7. Une fois vert, clique sur le run terminé, puis tout en bas dans
   **"Artifacts"** → télécharge **"Kuca-app-debug"** (c'est un .zip contenant
   ton `.apk`)
8. Dézippe, transfère le `.apk` sur ton téléphone Android si besoin, ouvre-le
   pour l'installer (autorise "sources inconnues" si demandé)

Aucune installation, aucun code à écrire — juste déposer des fichiers sur un
site web et cliquer sur un bouton de téléchargement.

---

## Option B — Avec un ordinateur (Android Studio)

### Étape 1 — Installer Android Studio

Télécharge et installe Android Studio (gratuit) :
https://developer.android.com/studio

Au premier lancement, laisse-le installer les composants proposés par défaut
(ça peut prendre 10-15 minutes).

### Étape 2 — Ouvrir le projet

1. Dans Android Studio, clique sur **"Open"**
2. Sélectionne le dossier **`android`** qui se trouve dans ce zip
   (pas le dossier racine `kuca-app`, bien le sous-dossier `android`)
3. Attends que Android Studio synchronise le projet (barre de progression en
   bas, ça peut prendre quelques minutes la première fois)

### Étape 3 — Générer l'appli (.apk)

1. Dans le menu du haut : **Build → Build Bundle(s) / APK(s) → Build APK(s)**
2. Une fois terminé, un lien "locate" apparaît en bas à droite → clique dessus
3. Ton fichier `app-debug.apk` est prêt : c'est ton appli Kuça installable !

### Étape 4 — L'installer sur un téléphone Android

- Branche ton téléphone en USB (active le "débogage USB" dans les paramètres
  développeur), puis dans Android Studio clique sur le bouton ▶️ **Run**
- OU transfère le fichier `.apk` sur ton téléphone (mail, Drive, clé USB) et
  ouvre-le directement dessus pour l'installer (autorise "sources inconnues"
  si demandé)

## Et pour l'App Store (iPhone) ?

Il faut un Mac + Xcode (gratuit) + un compte développeur Apple (99$/an).
Dis-le-moi si tu veux que je prépare aussi la version iOS — la structure est
identique, seule la dernière étape de compilation change.

## Pour republier une nouvelle version après une modification de l'appli

Si je te fournis un nouveau fichier `index.html` mis à jour :
1. Remplace `android/app/src/main/assets/public/index.html` par le nouveau
2. Dans Android Studio : **Build → Build Bundle(s) / APK(s) → Build APK(s)**

---
**Nom de l'appli :** Kuça
**Identifiant :** com.kuca.immobilier
