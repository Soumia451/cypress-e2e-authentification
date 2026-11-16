# Tests E2E automatisés avec Cypress

![Tests E2E](https://github.com/Soumia451/cypress-e2e-authentification/actions/workflows/cypress.yml/badge.svg)

Projet réalisé dans le cadre de ma formation en automatisation des tests (Automation Tester Academy).

Automatisation de scénarios d'authentification sur deux applications de démonstration, avec des cas passants et non passants.

## Scénarios couverts

| Application | Scénario | Vérification |
|---|---|---|
| [SauceDemo](https://www.saucedemo.com/) | Connexion avec des identifiants valides | L'en-tête de la page produits s'affiche |
| SauceDemo | Connexion avec un nom d'utilisateur invalide | La page reste affichée (voir pistes d'amélioration) |
| [Automation Tester Academy](https://practice.automationtesteracademy.com/) | Connexion avec des identifiants valides | Le titre de la page produits s'affiche |
| Automation Tester Academy | Connexion avec un mot de passe invalide | Le message d'erreur « Veuillez vérifier… » s'affiche |

Chaque saisie est contrôlée (`should('have.value', …)`) avant la soumission du formulaire.

## Stack technique

| Outil | Usage |
|---|---|
| Cypress | Automatisation des tests E2E |
| JavaScript | Écriture des scripts de test |
| Git / GitHub | Versioning |
| GitHub Actions | Exécution automatique des tests à chaque push et chaque lundi |

## Structure du projet

```
cypress/
├── e2e/
│   └── Test.cy.js   # Les 4 scénarios d'authentification
├── fixtures/        # Jeux de données de test
└── support/         # Commandes personnalisées et configuration
cypress.config.js    # Configuration Cypress
```

## Lancer les tests

```bash
# Installer les dépendances
npm install

# Ouvrir l'interface Cypress (mode interactif)
npx cypress open

# Lancer tous les tests en mode headless
npx cypress run
```

## Pistes d'amélioration

- Vérifier le message d'erreur affiché dans le scénario d'échec SauceDemo
- Ajouter les parcours panier et commande (tunnel d'achat)
- Externaliser les identifiants dans les fixtures

## Autrice

Soumia Sadki — Analyste QA · [LinkedIn](https://www.linkedin.com/in/soumia-sadki/)
