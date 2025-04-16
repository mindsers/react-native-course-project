# 📱 Projets React Native – Cursus Lead Fullstack Developer

Ce repo contient 5 projets Expo à réaliser en binôme. Chaque projet est conçu pour durer 2 à 3 jours et couvre toutes les notions React Native vues en cours.

## 📦 Projets disponibles

- [Planify](./planify) – Organisation d'événements avec vote
- [TaskTrack](./tasktrack) – To-do list géolocalisée
- [Learnify](./learnify) – App de révision par flashcards
- [EcoWalk](./ecowalk) – Suivi de parcours de marche
- [EventMe](./eventme) – Découverte d'événements par intérêt

## 🎯 Objectifs communs

- Navigation `expo-router`
- Styles avec `StyleSheet.create()`
- Layout responsive via Flexbox
- Contexts React
- Notifications
- Capteurs natifs (géoloc minimum)
- Backend Supabase (auth, pagination, sync)
- Bonus : In-App Purchases

## 🔧 Installation commune

Pour créer les projets vous devez utiliser les deux commandes suivantes :

```bash
npx create-expo-app@latest
npx expo install expo-router expo-location expo-notifications expo-in-app-purchases @react-native-async-storage/async-storage
```

## 🧠 Rappel : GPT & Copilot
Vous avez le droit d’utiliser des outils d’assistance (ChatGPT, Copilot, Stack Overflow…) et surtout les supports de cours en PDF, mais vous devez prouver que vous comprenez ce que vous faites. Les projets sont évalués sur la qualité de la conception, l’implémentation et la compréhension.

### ✅ Ce qui est autorisé

- Utiliser une IA pour débloquer un bug ou comprendre un module
- Demander une idée de structure ou d’approche
- Gagner du temps sur de la doc ou du boilerplate

### ❌ Ce qui est interdit
- Copier/coller un écran ou une fonctionnalité sans comprendre le code
- Générer une app entière sans réflexion perso
- Générer du code que vous ne seriez pas capables d’expliquer à l’oral

### 💬 Ce que vous devez savoir expliquer (à l’oral ou à l’écrit)
- Pourquoi vous avez structuré le projet de cette façon
- Le rôle de chaque fichier/fonction principale
- Comment fonctionne au moins les notifications, les contextes, les interactions natives
- Comment vous avez intégré chaque exigence technique du brief

### ⚠️ Sanctions
- Une explication non satisfaisante (à la seule discrétion du profésseur) = retrait de points
- Un projet entièrement généré sans logique propre ni architecture = validation refusée