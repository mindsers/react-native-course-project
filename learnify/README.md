# Learnify

## 🎯 Contexte & objectifs
Crée des flashcards, révise-les chaque jour et suis ta progression.

Tu dois créer une app de révision avec des flashcards personnalisables, des rappels pour réviser, et un suivi des progrès. L’utilisateur peut créer des decks de cartes, les consulter via un mode apprentissage ou test, et configurer des notifications quotidiennes.

Ce projet doit être déployable sur un téléphone via Expo Go, et utilisable sans backend lourd (utilisez Supabase à la base).

## 🧠 Objectifs pédagogiques
- Géolocalisation ou capteurs (`expo-location`)
- Notifications (`expo-notifications`)
- `StyleSheet.create()` obligatoire
- Navigation avec `expo-router`
- Flexbox pour la mise en page
- Context React pour les préférences ou état global
- Supabase : auth, pagination, sync offline
- (Bonus) In-App Purchase (`expo-in-app-purchases`)

## 🔧 Fonctionnalités à implémenter
### 📖 Decks de flashcards
- Création, édition, suppression
- Chaque deck contient plusieurs cartes (question + réponse)
- Stockage local (AsyncStorage ou SQLite)

### 🧠 Mode apprentissage
- Swipe entre les cartes
- Possibilité de marquer comme “connu” ou “à revoir”
- Animation ou flip visuel entre question et réponse

### 📝 Mode test (QCM)
- Affichage d’une question avec plusieurs réponses possibles
- Calcul d’un score à la fin

### 📊 Statistiques
- % de bonne réponses par deck
- Nombre de sessions effectuées
- Dernière date de révision

### ⏰ Notifications
- Planifier un rappel chaque jour à 10h pour réviser
- Possibilité de changer l’heure du rappel

## 📦 Supabase
Schéma à créer dans ton projet :
- users (id, name, email)
- decks (id, user_id, title, created_at)
- flashcards (id, deck_id, question, answer)
- sessions (id, user_id, deck_id, correct_answers, total_questions, created_at)

Contraintes Supabase :
- Vous ne pouvez pas modifier le schéma ci-dessus
- Auth Supabase (email + mot de passe)
- Vous devez :
  - Explorer la base seul
  - Vous adapter au format des données (flashcards liées à un deck_id, sessions à un user_id)
  - Filtrer les decks et sessions de l’utilisateur connecté
  - Implémenter la pagination des decks (ex : 5 par 5)
  - Stocker localement les decks et flashcards pour permettre une révision hors ligne
  - Synchroniser les sessions et la progression dès que la connexion revient

## 🎁 Bonus techniques
- In-App Purchase pour débloquer la création de +3 decks
- Thème dark/light dynamique
- Animations ou transitions avancées
- Export / import de decks (JSON ou clipboard)
- Suggestion de deck en fonction de la localisation (ex : “anglais pro” au bureau)

## 🧪 Évaluation (sur 20)

| Critère                         | Points |
|---------------------------------|--------|
| Fonctionnalités de base         | 8      |
| Structure et qualité du code    | 3      |
| UX et responsivité              | 3      |
| Respect des notions imposées    | 3      |
| Bonus techniques                | 3      |

## 🧠 Rappel : Anti-triche GPT
L’usage de ChatGPT est autorisé comme assistant, mais :
- Vous devez comprendre et pouvoir justifier votre code
- Toute réponse floue ou copiée sans explication = retrait de points

Voir le README principal pour plus d'informations.