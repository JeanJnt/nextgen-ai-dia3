# Trustworthy Generative AI - DIA 3

ESILV - Majeure Data & Artificial Intelligence (A4 / S7)  
Cours : Next-Generation AI (Didier Parisot)  
Pack version : `2026-10-14-students-1`  

## Sub-group Identification

- **Classe / Groupe** : DIA 3
- **Sous-groupe** : Sub-group 1 (à ajuster avec le numéro exact de table / sous-groupe)
- **Membres du sous-groupe** :
  - Louis Le Forestier (louis.le_forestier@edu.devinci.fr)
  - [Membre 2]
  - [Membre 3]
  - [Membre 4]
  - [Membre 5]
  - [Membre 6]
  - [Membre 7]
  - [Membre 8]

## Environment & Prerequisites

- **Python** : >= 3.10 (testé sous Python 3.11.9, SQLite 3.45.1)
- **Dépendances** : bibliothèque standard Python + `requests`
- **Empreinte de la base SQLite (`boutique.sqlite`)** :
  `0077e235adc2ca647b484e3083c98a6d7cae3ef3655ce366a299caf13398fec2` (seed `20260925`)

## Setup Instructions

1. Créer et activer l'environnement virtuel :
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   pip install requests
   ```

2. Exporter les clés d'API (sans jamais les commiter) :
   ```powershell
   $env:GROQ_API_KEY = "gsk_..."
   $env:OPENROUTER_API_KEY = "sk-or-v1-..."
   ```

3. Vérifier les accès et l'intégrité :
   ```powershell
   cd kit-td1
   python verify-data.py
   python check_access.py
   ```

## Repository Structure

```text
├── .gitignore                          # Protection des secrets et fichiers locaux
├── README.md                           # Identification du sous-groupe et commandes
├── prompts-en.md                       # Prompts système et templates utilisés
├── reference-td1.csv                   # Vérités de référence C01 à C20 calculées en SQL
├── model-question-comparison-en.csv    # Comparaison détaillée modèle x question
├── five-model-summary-en.csv           # Synthèse des 5 modèles autorisés et coûts
├── configuration-comparison-en.csv     # Comparaison des configurations (TD3)
├── cost-calculation-en.csv             # Calculs de coûts (TD3)
├── contributions-en.csv                # Répartition des contributions des membres
├── voting-tests-en.csv                 # Tests du vote k-sur-n (TD2)
├── routing-rule-en.md                  # Règle de routage du sous-groupe (TD2)
├── reports/
│   ├── td1.md                          # Compte-rendu du TD 1
│   ├── td2.md                          # Compte-rendu du TD 2
│   └── td3.md                          # Compte-rendu du TD 3
└── kit-td1/
    ├── data/                           # Base boutique.sqlite et CSV de référence
    ├── schema.sql                      # Schéma relationnel (3 tables)
    ├── questions-td1.json              # 20 questions de chiffre d'affaires
    ├── modeles-autorises.json          # Modèles autorisés et paramètres
    ├── skeleton-multi-llm-en.py        # Squelette d'orchestration
    ├── sandbox_sqlite.py               # Bac à sable SQLite en lecture seule
    ├── check_access.py                 # Vérificateur d'accès
    ├── verify-data.py                  # Vérificateur d'intégrité SHA-256
    ├── atelier-vote.py                 # Atelier TD 2 vote
    └── atelier-routage.py              # Atelier TD 2 routage
```
