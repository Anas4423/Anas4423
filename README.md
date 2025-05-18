🛒 Azrou Sané - Application de Gestion E-commerce
Bienvenue dans l'application de gestion e-commerce Azrou Sané, spécialisée dans la distribution de produits sanitaires au Maroc. Cette application permet la gestion  des produits, des commandes, de la messagerie interne, des paramètres de site, et plus encore.

📦 Fonctionnalités principales
Gestion des produits (ajout, mise à jour, affichage en page d’accueil, etc.)

Gestion des commandes (multi-statuts, historiques)

Messagerie interne entre utilisateurs

Paramétrage complet de la page d’accueil (slides, textes, couleurs, etc.)

Suivi des connexions et des visites

Paramètres du site (logo, footer, etc.)

🧱 Structure des tables principales
✅ utilisateurs
Contient les informations des clients et des administrateurs.

✅ produits
Stocke les produits en vente, leur prix, quantité, image, etc.

✅ commandes & ligne_commandes
Gèrent les commandes passées, les produits associés, les statuts, etc.

✅ historique_commandes
Historique des changements de statut d’une commande.

✅ messages
Système de messagerie entre utilisateurs.

✅ homepage_settings, homepage_slides, slider_images
Gèrent le contenu dynamique de la page d’accueil.

✅ site_settings & footer_settings
Configuration de l'apparence globale du site et du pied de page.

✅ visitor_logs & client_connections
Enregistrement des visites et connexions utilisateur.

⚙️ Installation
1. Cloner le projet
bash
Copy
Edit
git clone https://github.com/votre-utilisateur/azrou-sane.git
cd azrou-sane
2. Créer la base de données
Créer une base de données MySQL et importer le script SQL ci-dessous :

sql
Copy
Edit
-- azrou_sane.sql
-- Contient les tables listées dans ce projet
3. Configurer l'application (si Laravel par exemple)
Créer le fichier .env :

bash
Copy
Edit
cp .env.example .env
Configurer les variables de connexion à la base de données :

dotenv
Copy
Edit
DB_DATABASE=azrou_sane
DB_USERNAME=root
DB_PASSWORD=
Puis générer la clé :

bash
Copy
Edit
php artisan key:generate
4. Lancer le serveur
bash
Copy
Edit
php artisan serve
📊 Statuts de commande
Statut	Signification
en_attente	Commande en attente de validation
confirmee	Validée par l'administrateur
en_preparation	En cours de préparation
expediee	Envoyée au client
livree	Commande livrée
annulee	Commande annulée

💬 Exemple de données (homepage)
sql
Copy
Edit
INSERT INTO homepage_settings (setting_key, setting_value) VALUES
('main_title', 'Azrou Sané'),
('subtitle', 'Leader dans la distribution de produits sanitaires au Maroc'),
('button_text', 'Découvrir nos produits');
✍️ Auteur
Développé par : LKHAYAT Anas

Encadré par : EL HAYYANI Isam

Entreprise : Azrou Sané

Année de formation : 2024/2025
