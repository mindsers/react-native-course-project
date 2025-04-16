# Ecowalk

## 🎯 Contexte & objectifs
Découvre et suis des parcours de randonnée autour de toi.

Tu dois créer une application qui permet à un utilisateur de :
- Découvrir des parcours autour de lui (balades, randos)
- Suivre sa progression en temps réel sur une carte
- Être notifié à l’arrivée ou à certaines étapes
- Visualiser ses statistiques de marche

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
### 🌍 Liste des parcours
- Affichage de balades avec titre, durée, distance, description
- Tri par distance (géolocalisation)
- Marquage “déjà fait” ou “favori”

### 🗺️ Détail et carte du parcours
- Carte avec le tracé
- Bouton “Commencer la balade”

### 🧭 Suivi du parcours en temps réel
- Position utilisateur sur la carte
- Notification quand il atteint la fin ou un POI
- Mesure temps réel : distance parcourue, vitesse, durée

### 📊 Statistiques
- Distance totale marchée
- Temps total passé
- Nombre de balades terminées

## 📦 Supabase
Schéma à créer dans ton projet :
- users (id, name, email)
- walks (id, title, description, distance_km, duration_min, path, is_premium)
- pois (id, walk_id, title, description, location)
- user_walks (id, user_id, walk_id, started_at, finished_at, steps_count)

Contraintes Supabase :
- Vous ne pouvez pas modifier le schéma ci-dessus
- Auth Supabase (email + mot de passe)
- Vous devez :
  - Explorer la base seul
  - Vous adapter au format des données (path = tracé GPS, pois.location = géopoint)
  - Filtrer les balades réalisées (user_walks) par utilisateur connecté
  - Implémenter la pagination sur la liste des balades (walks)
  - Stocker localement la progression (user_walks) et les balades disponibles
  - Synchroniser les balades faites (et POIs visités, si implémenté) à la reconnexion
  - Restreindre l’accès aux balades is_premium selon achat intégré (bonus)

## 🎁 Bonus techniques
- In-App Purchase pour débloquer +10 parcours ou des filtres premium (durée, difficulté…)
- Thème dark/light dynamique
- Animations ou transitions avancées
- Deep linking ou partage d’éléments
- Ajout de ses propres balades avec tracé
- Photos sur les parcours (POIs illustrés)

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
