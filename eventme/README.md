# Eventme

## 🎯 Contexte & objectifs
Trouve et suis des événements selon tes centres d’intérêt.

Tu dois développer une application mobile permettant :
- de découvrir des événements autour de soi selon ses intérêts
- de s’y inscrire et recevoir une notification
- de suivre les événements passés et à venir
- de filtrer les événements (gratuit, payant, proche, populaire…)

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
### 🧭 Accueil / événements recommandés
- Affichage des événements proches selon centres d’intérêt
- Tri par popularité, gratuité, proximité, date

### 🔍 Recherche & filtres
- Filtres : catégories (musique, pro, sport…), distance, gratuit/payant
- Barre de recherche avec debounce

### 📅 Détail d’un événement
- Infos : titre, date, heure, lieu, description
- Bouton “Je participe”
- Ajout dans “mes événements”

### 🛎 Notifications
- Notification automatique 1h avant l’événement
- Option pour être rappelé le jour d’avant

### 📂 Mes événements
- Liste des événements à venir + passés
- Possibilité d’annuler sa participation

## 📦 Supabase
Schéma à créer dans ton projet :
- users (id, name, email)
- events (id, title, description, date, location, category, is_premium, created_at)
- event_participants (user_id, event_id, registered_at)

Contraintes Supabase :
- Vous ne pouvez pas modifier le schéma ci-dessus
- Auth Supabase (email + mot de passe)
- Vous devez :
  - Explorer la base seul
  - Vous adapter au format des données (location au format geography, is_premium booléen)
  - Filtrer les participations de l’utilisateur connecté via event_participants
  - Implémenter la pagination des événements par distance ou date
  - Stocker localement les participations et événements pour consultation offline
  - Synchroniser automatiquement les participations à la reconnexion
  - Restreindre l’accès aux événements is_premium en fonction d’un flag local ou d’un achat intégré (bonus)

## 🎁 Bonus techniques
- In-App Purchase pour débloquer une limite (à définir selon projet)
- Thème dark/light dynamique
- Animations ou transitions avancées
- Deep linking ou partage d’éléments
- Map des événements (vue carte optionnelle)

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
