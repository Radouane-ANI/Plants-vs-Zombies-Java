# 🌻 Plants vs. Zombies — Implémentation Java & Swing

[![Java](https://img.shields.io/badge/Java-8%2B-orange.svg?logo=openjdk)](https://openjdk.org/)
[![GUI](https://img.shields.io/badge/GUI-Swing-blue.svg)](https://docs.oracle.com/javase/tutorial/uiswing/)
[![Pattern](https://img.shields.io/badge/Architecture-MVC-brightgreen.svg)]()

![Logo du projet](banniere.png)

Une réimplémentation complète et fidèle en **Java** du célèbre jeu d'arcade et de stratégie *Plants vs. Zombies*, structurée selon une architecture **Modèle-Vue-Contrôleur (MVC)** claire et évolutive.

---

## 🎮 Mécaniques de Jeu

Le joueur doit défendre sa maison contre des vagues successives de zombies en positionnant stratégiquement différentes plantes sur une grille de jeu en temps réel :

- **Économie de Soleils** : Production naturelle de soleils et génération active via les Tournesols pour financer les plantations.
- **Ligne de défense ultime** : Chaque ligne est protégée par une **tondeuse de secours** qui s'active si un zombie atteint l'extrémité gauche du jardin.
- **Système de vagues & Progression** : Gestion dynamique des niveaux avec augmentation progressive de la difficulté via [`GestionnaireNiveaux`](src/model/GestionnaireNiveaux.java).

---

## 🌿 Bestiaire & Unités

### 🌸 Les Plantes
- **Tournesol** : Génère des soleils supplémentaires à intervalles réguliers.
- **Tire-pois (Peashooter)** : Tire des projectiles standards en ligne droite.
- **Pois gelé (Snow Pea)** : Projette des billes givrées qui ralentissent les assaillants.
- **Noix muraille (Wall-nut)** : Rempart doté d'une grande résistance pour bloquer la progression ennemie.
- **Bombe cerise (Cherry Bomb)** : Explosion de zone à dégâts massifs.
- **Mine patate (Potato Mine)** : Armement souterrain explosif au contact après un temps d'amorçage.
- **Chomper (Mangeuse)** : Dévore instantanément un zombie avant d'entrer en phase de digestion.

### 🧟 Les Zombies
- **Zombie classique** : Attaquant standard régulier.
- **Zombie cône** : Doté d'une protection crânienne doublant ses points de vie.
- **Zombie journal** : Vitesse décuplée une fois son journal protecteur détruit.
- **Zombie sportif** : Équipé d'un casque de football américain, très rapide et robuste.

---

## 🏗️ Architecture Logicielle (MVC)

```
src/
├── model/        # Logique métier, états du plateau, gestion des projectiles et entités
│   ├── plante/   # Hiérarchie orientée objet des plantes
│   └── zombie/   # Hiérarchie orientée objet des zombies
├── gui/          # Vues graphiques Swing, fenêtres, animations et rendus d'images
└── controleur/   # Gestion de la boucle de jeu temps réel (Tick), entrées souris et menus
```

---

## 🚀 Installation & Lancement

### Lancement direct via le JAR précompilé
```bash
java -jar PlantsVsZombies.jar
```

### Compilation manuelle depuis les sources
```bash
# Compilation
javac -cp src -d bin src/gui/App.java

# Exécution
java -cp bin:src gui.App
```

---

## 👥 Auteurs
- **Radouane Aouini**
- **Chioukh S.**
