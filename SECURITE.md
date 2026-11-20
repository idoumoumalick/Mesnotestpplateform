# Registre des failles — Séance 1

## 1. Acteurs

**Acteurs légitimes :**
- Étudiant : consulte ses notes et les matières.
- Enseignant : gère les notes des étudiants.
- Administrateur : gère les utilisateurs et l'application.

**Acteurs potentiellement malveillants :**
- Un étudiant qui tente d'accéder aux notes d'un autre étudiant.
- Une personne extérieure qui cherche à accéder à l'application sans autorisation.
- Un utilisateur légitime qui tente d'abuser de ses permissions.

## 2. Biens à protéger

Classement du plus sensible au moins sensible :

1. Données personnelles et identifiants des utilisateurs.
2. Notes et résultats académiques des étudiants.
3. Jetons d'authentification et informations de connexion.
4. Intégrité des matières et des données de l'application.
5. Disponibilité du service et code source.

## 3. Points d'entrée

- Formulaires de connexion et d'authentification.
- Routes HTTP de l'API.
- Interfaces web de l'application.
- Paramètres transmis dans les requêtes HTTP.
- Dépendances externes installées avec npm.

## 4. Scénarios d'attaque

1. Un étudiant essaie de consulter les notes d'un autre étudiant en modifiant l'identifiant transmis dans une requête HTTP.
2. Un attaquant essaie de modifier les notes d'un étudiant en envoyant une requête non autorisée à l'API.
3. Une personne extérieure essaie d'accéder aux données de l'application en utilisant un jeton d'authentification volé.