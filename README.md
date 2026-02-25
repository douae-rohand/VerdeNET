# VerdeNET🛠️

**VerdeNET** est une plateforme moderne de mise en relation entre clients et prestataires de services (Intervenants) pour divers services à domicile tels que la plomberie, le ménage, le jardinage, et bien plus encore.

Développée avec **Laravel 12** et **Vue.js 3**, elle offre une solution robuste pour la gestion des interventions, des évaluations et des interactions utilisateurs.

---

## 🌟 Fonctionnalités Clés

### 👤 Pour les Clients
- **Catalogue de Services** : Parcourez et recherchez divers services à domicile.
- **Découverte de Prestataires** : Trouvez des intervenants qualifiés basés sur leurs notes, leur localisation et leur disponibilité.
- **Réservation Facile** : Créez des demandes de service avec des détails spécifiques, adresses et photos.
- **Gestion des Interventions** : Suivez le statut de vos demandes (En attente, Acceptée, Terminée).
- **Évaluations Bidirectionnelles** : Évaluez votre expérience et consultez les avis laissés par les prestataires.
- **Favoris** : Enregistrez vos intervenants préférés pour un accès rapide.
- **Réclamations** : Signalez tout problème via un système de support dédié.

### 👷 Pour les Intervenants
- **Gestion de Profil** : Présentez vos compétences, votre expérience et votre biographie.
- **Souscription aux Services** : Inscrivez-vous pour proposer des services spécifiques (soumis à validation admin).
- **Contrôle des Tâches et Tarifs** : Définissez vos propres prix pour les tâches que vous effectuez.
- **Gestion des Disponibilités** : Configurez vos horaires hebdomadaires réguliers ou des créneaux spécifiques.
- **Tableau de Bord des Réservations** : Gérez efficacement les demandes entrantes et marquez les interventions comme terminées.
- **Génération de Factures** : Générez automatiquement des factures professionnelles pour les travaux terminés.

### 🛡️ Pour les Administrateurs
- **Tableau de Bord Complet** : Statistiques en temps réel sur les utilisateurs, les services et les interventions.
- **Gestion des Utilisateurs** : Activez, désactivez et examinez les profils clients et intervenants.
- **Supervision des Services** : Créez et gérez le catalogue de services, les tâches et les prérequis.
- **Résolution des Litiges** : Gérez les réclamations avec un historique complet du contexte de l'intervention.
- **Exportation de Données** : Exportez l'historique et les rapports aux formats CSV ou PDF.

---

## 🚀 Stack Technologique

- **Backend** : [Laravel 12](https://laravel.com/) (PHP 8.2+)
- **Frontend** : [Vue.js 3](https://vuejs.org/) + [Vite](https://vitejs.dev/) + [Tailwind CSS](https://tailwindcss.com/)
- **Base de données** : MySQL 8.0
- **Temps Réel** : [Laravel Reverb](https://reverb.laravel.com/) (WebSockets)
- **Infrastructure** : Docker & Docker Compose
- **Authentification** : Laravel Sanctum & Socialite (Google OAuth)

---

## 🛠️ Installation

### Prérequis
- [Docker](https://www.docker.com/) & Docker Compose
- Node.js (v20+)

### Procédure

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/douae-rohand/service_Pro.git
   cd service_Pro
   ```

2. **Configurer les variables d'environnement** :
   - Copiez `backend/.env.example` vers `backend/.env`
   - Copiez `frontend/.env.example` vers `frontend/.env` (si applicable)

3. **Lancer avec Docker** :
   ```bash
   docker-compose up -d --build
   ```

4. **Initialiser le Backend** :
   ```bash
   docker exec -it laravel_app composer setup
   ```
   *Note : Ce script installe les dépendances, génère les clés et exécute les migrations/seeders.*

5. **Accéder à l'application** :
   - **Frontend** : [http://localhost](http://localhost)
   - **Backend API** : [http://localhost:8000](http://localhost:8000)
   - **phpMyAdmin** : [http://localhost:8081](http://localhost:8081)

---

## 📁 Structure du Projet

```text
.
├── backend/            # API Laravel 12
│   ├── app/            # Logique métier, Modèles, Contrôleurs
│   ├── database/       # Migrations et Seeders
│   └── routes/         # Routes API & Channels
├── frontend/           # Application Vue.js 3
│   ├── src/            # Composants, Vues, Services
│   └── public/         # Assets statiques
└── docker-compose.yml  # Orchestration de l'infrastructure
```

---

## 📄 Documentation

Pour une documentation détaillée de l'analyse et de la conception, veuillez consulter :
- [Analyse Complète du Projet](file:///c:/Users/viet/Desktop/TPs/PHP/service_Pro/ANALYSE_COMPLETE_PROJET.md)
- [Analyse de Synchronisation Temps Réel](file:///c:/Users/viet/Desktop/TPs/PHP/service_Pro/ANALYSE_SYNCHRONISATION_TEMPS_REEL.md)
- [Logique de Gestion des Services](file:///c:/Users/viet/Desktop/TPs/PHP/service_Pro/GESTION_SERVICES_INTERVENANT_ADMIN.md)

---

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.
