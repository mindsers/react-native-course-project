# Tasktrack

## 🎯 Contexte & objectifs
Gère des tâches à faire liées à des lieux. Reçois des notifications quand tu es proche.

Tu dois développer une app mobile qui permet à l’utilisateur de :
- Créer des tâches associées à un lieu
- Recevoir une notification quand il passe près du lieu
- Suivre ses tâches dans une liste ou sur une carte

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
### 🗂 Liste des tâches
- Vue scrollable
- Affichage des tâches avec nom, lieu, statut (fait/pas fait)
- Marquage comme “fait”
- Tri par distance ou par date

### 📍 Carte interactive
- Affichage de l’utilisateur + des tâches sur la carte
- Bouton pour centrer la vue

### ➕ Ajout d’une tâche
- Formulaire avec :
  - Nom
  - Description (optionnelle)
  - Position (via géoloc automatique ou carte cliquable)
- Validation des champs

### 🔔 Notification
- En background, la position est checkée toutes les X minutes (mock si besoin)
- Si proche d’une tâche non faite → notif

## 📦 Supabase
Schéma à créer dans ton projet :
- users (id, name, email)
- tasks (id, user_id, title, description, location, done, created_at)

Contraintes Supabase :
- Vous ne pouvez pas modifier le schéma ci-dessus
- Auth Supabase (email + mot de passe)
- Vous devez :
  - Explorer la base seul (tables visibles dans le dashboard)
  - Vous adapter au format des données (ex : champ location au format geography)
  - Filtrer les tâches de l’utilisateur connecté (user_id)
  - Implémenter la pagination via range() pour afficher les tâches 10 par 10
  - Stocker localement les tâches avec AsyncStorage pour un usage offline
  - Synchroniser les données locales et Supabase à la reconnexion

## 🎁 Bonus techniques
- In-App Purchase pour débloquer +10 tâches
- Thème dark/light dynamique
- Animations ou transitions avancées
- Deep linking ou partage d’éléments
- Suggestions intelligentes basées sur l’historique
- Possibilité d’attacher une photo à une tâche (expo-image-picker)

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