# Planify

## 🎯 Contexte & objectifs
Organise un événement entre amis avec proposition de dates, votes et notifications.

Tu dois développer une application mobile avec React Native + Expo qui permet à un utilisateur de :
- Créer un événement avec plusieurs dates proposées
- Partager un lien vers l’événement
- Permettre à d’autres de voter pour leurs dates préférées
- Visualiser les résultats des votes en temps réel (ou mocké)

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
### Création d’un événement
- Titre de l’événement
- Description facultative
- Proposition de 2 à 5 dates/heures
- Génération d’un eventId unique
- Enregistrement local (ou Supabase si vous avez le temps)

### Partage de l’événement
- Copie d’un “lien” dans le presse-papiers (simulateur de deep linking)
- Exemple de lien : planify://event/abcd1234

### Participation
- Entrée du nom du participant
- Vote pour une ou plusieurs dates proposées
- Sauvegarde du vote

### Visualisation des résultats
- Vue des résultats en tableau ou graphique simple
- Mise à jour en direct (ou reload manuel)
- Date gagnante mise en évidence

## 📦 Supabase
Schéma à créer dans ton projet :
- users (id, name, email)
- events (id, title, description, location, proposed_dates, owner_id, created_at)
- votes (user_id, event_id, selected_dates)

Contraintes Supabase :
- Vous ne pouvez pas modifier le schéma ci-dessus
- Auth Supabase (email + mot de passe ou magic link)
- Vous devez :
  - Explorer la base seul
  - Vous adapter au format des données (proposed_dates est un tableau de dates, selected_dates aussi)
  - Filtrer les votes et événements par utilisateur connecté
  - Implémenter la pagination sur les événements disponibles ou votés
  - Stocker localement les votes et événements pour usage offline
  - Synchroniser automatiquement les données dès que la connexion revient

## 🎁 Bonus techniques
- In-App Purchase pour débloquer plus de 5 dates à proposer
- Thème dark/light dynamique
- Drag & drop pour réorganiser les dates
- Deep linking pour accéder directement à un eventId

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