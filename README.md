# Kanban Supreme - Application Kanban

Une application de gestion de tâches desktop moderne basée sur la méthodologie Kanban, développée en C++ avec Qt Framework.

## 📋 Table des matières

- [Aperçu](#aperçu)
- [Fonctionnalités](#fonctionnalités)
- [Architecture](#architecture)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Guide d'utilisation](#guide-dutilisation)
- [Structure du projet](#structure-du-projet)
- [Documentation](#documentation)

## 🎯 Aperçu

**Kanban Supreme** est une application desktop intuitive permettant de gérer des projets et des tâches en utilisant le système Kanban. Elle permet aux utilisateurs d'organiser leurs travaux en colonnes (À faire, En cours, Terminé) pour une meilleure visualisation du flux de travail.

### Caractéristiques principales

- Interface graphique moderne et conviviale
- Gestion visuelle des tâches par glisser-déposer
- Organisation des tâches en tableaux Kanban
- Suppression et création facile de tâches
- Icônes intuitives pour les actions
- Persistance des données

## ✨ Fonctionnalités

### Gestion des tâches

- ✅ **Créer des tâches** : Ajouter facilement de nouvelles tâches
- ✏️ **Modifier des tâches** : Mettre à jour les informations de tâche
- 🗑️ **Supprimer des tâches** : Supprimer les tâches avec confirmation
- 📋 **Visualisation en colonnes** : 
  - À faire (To Do)
  - En cours (In Progress)
  - Terminé (Done)

### Interface utilisateur

- Boutons d'action clairs avec icônes
- Dialogue de confirmation pour les suppressions
- Affichage des images d'icônes (PNG)
- Interface responsive et intuitive
- Organisation visuelle des tâches par statut

## 🏗️ Architecture

L'application est structurée selon l'architecture Qt standard :

```
Kanban_Supreme/
├── .gitignore                      # Configuration Git
├── Kanban_Supreme.pro              # Fichier projet Qt
├── mainwindow.h / mainwindow.cpp   # Fenêtre principale
├── mainwindowCopy.h                # Sauvegarde configuration
├── dialog.h / dialog.cpp           # Dialogues
├── dialog.ui                       # Interface utilisateur (XML)
└── [assets]                        # Ressources (icônes PNG)
    ├── delete_40623.png
    ├── new-file_40454.png
    └── new_folder_add_icon_231483.png
```

### Composants principaux

#### MainWindow
- Gère la fenêtre principale de l'application
- Orchestration des interactions utilisateur
- Gestion du tableau Kanban

#### Dialog
- Dialogues personnalisés pour les interactions utilisateur
- Formulaires de saisie
- Messages de confirmation

#### Interface UI
- Fichiers `.ui` (Qt Designer XML)
- Définition visuelle des éléments d'interface
- Layout et organisation des widgets

## 📦 Prérequis

- **Système d'exploitation** : Windows, macOS ou Linux
- **Qt Framework** : Qt 5.12 ou supérieur
- **Compilateur** : 
  - MinGW 7.3+ (Windows)
  - GCC 5.0+ (Linux)
  - Clang 9.0+ (macOS)
- **C++ Standard** : C++11 ou supérieur

### Dépendances

- Qt Core
- Qt Gui
- Qt Widgets

## 🚀 Installation

### 1. Clone du repository

```bash
git clone https://github.com/RAYANEBIO/Kanban-app.git
cd Kanban-app
```

### 2. Extraction de l'archive

```bash
# Extraire Kanban_Supreme.rar
unrar x Kanban_Supreme.rar
# ou avec 7-Zip
7z x Kanban_Supreme.rar
```

### 3. Configuration Qt

```bash
# Naviguer vers le répertoire source
cd Kanban_Supreme

# Générer les fichiers Makefile avec qmake
qmake Kanban_Supreme.pro

# Compiler le projet
make
# ou
nmake  # sur Windows avec MSVC
```

### 4. Exécution

```bash
# Linux/macOS
./Kanban_Supreme

# Windows
Kanban_Supreme.exe
```

## 📖 Guide d'utilisation

### Démarrage

1. Lancez l'application `Kanban_Supreme`
2. L'interface affiche un tableau avec 3 colonnes principales

### Créer une tâche

1. Cliquez sur l'icône **"Nouvelle tâche"** (nouveau fichier)
2. Entrez le titre de la tâche
3. Confirmez en cliquant sur "Ajouter"

### Modifier une tâche

1. Cliquez sur la tâche à modifier
2. Mettez à jour les informations
3. Confirmez les modifications

### Supprimer une tâche

1. Cliquez sur l'icône **"Supprimer"** (poubelle) sur la tâche
2. Confirmez la suppression dans le dialogue
3. La tâche est supprimée immédiatement

### Gérer le flux de travail

- **Colonnes Kanban** :
  - **À faire** : Nouvelles tâches créées
  - **En cours** : Tâches en cours de réalisation
  - **Terminé** : Tâches complétées

## 📁 Structure du projet

### Fichiers source

- **mainwindow.h / mainwindow.cpp** : Classe principale de l'application
- **mainwindowCopy.h** : Fichier de secours
- **dialog.h / dialog.cpp** : Classes de dialogue
- **dialog.ui** : Définition XML de l'interface

### Ressources

- **delete_40623.png** : Icône de suppression (40x40 pixels)
- **new-file_40454.png** : Icône d'ajout (40x40 pixels)
- **new_folder_add_icon_231483.png** : Icône de dossier (créer)

### Configuration

- **Kanban_Supreme.pro** : Fichier projet Qt (qmake)
- **.gitignore** : Fichiers ignorés par Git

## 📚 Documentation

### Fichiers inclus

- **README.pdf** : Documentation complète du projet
- **Manuel d'utilisation.pdf** : Guide détaillé pour les utilisateurs
- **diagramme de cas d'utilisation.pdf** : Cas d'utilisation UML
- **diagramme de classe.pdf** : Diagramme des classes UML

Pour consulter la documentation détaillée, veuillez vous référer aux fichiers PDF inclus.

## 🔧 Développement

### Compilation en debug

```bash
qmake CONFIG+=debug Kanban_Supreme.pro
make
```

### Compilation en release

```bash
qmake CONFIG+=release Kanban_Supreme.pro
make
```

### Nettoyage du projet

```bash
make clean
rm -rf Makefile
```

## 🎨 Personnalisation

### Ajouter des icônes

1. Placez les fichiers PNG dans le répertoire du projet
2. Référencez-les dans le code Qt :

```cpp
QIcon icon(":/path/to/icon.png");
```

### Modifier l'interface

1. Ouvrez `dialog.ui` avec Qt Designer
2. Modifiez les widgets et layouts
3. Sauvegardez les modifications
4. Recompilez le projet

## 🐛 Dépannage

### Erreurs de compilation

**Problème** : Qt introuvable
```bash
# Solution : Configurez le chemin Qt
export PATH=/usr/lib/qt5/bin:$PATH
```

**Problème** : Erreurs de linking
```bash
# Solution : Vérifiez les dépendances Qt
qmake -v
```

### Problèmes d'exécution

- Assurez-vous que toutes les icônes PNG sont présentes
- Vérifiez les permissions d'exécution
- Consultez les logs d'erreur pour les détails

## 👨‍💻 Auteur

**RAYANEBIO**

- GitHub : https://github.com/RAYANEBIO
- Repository : https://github.com/RAYANEBIO/Kanban-app

## 📄 License

Ce projet n'a pas de licence spécifiée. Pour plus d'informations, consultez le propriétaire du repository.

## 🤝 Contribution

Les contributions sont bienvenues ! N'hésitez pas à :

1. Fork le repository
2. Créer une branche pour votre fonctionnalité
3. Commiter vos changements
4. Pousser vers la branche
5. Ouvrir une Pull Request

## 📞 Support

Pour toute question ou problème :

- Ouvrez une issue sur GitHub
- Consultez les fichiers PDF de documentation
- Vérifiez le manuel d'utilisation

## 📝 Notes de version

**Version actuelle** : 1.0.0

### Fonctionnalités implémentées

- ✅ Interface Kanban avec 3 colonnes
- ✅ Création de tâches
- ✅ Suppression de tâches
- ✅ Icônes intuitives
- ✅ Interface graphique Qt

### Prochaines améliorations possibles

- [ ] Glisser-déposer des tâches
- [ ] Persévérance automatique en base de données
- [ ] Système de priorités
- [ ] Filtrage et recherche
- [ ] Export/Import de données
- [ ] Thèmes personnalisables

---

**Dernier update** : Juin 2026
