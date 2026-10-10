# FrontEnd — Projet To Do List

**Auteurs** : Raoul FOSSUA TINDO & Lovensky DERVIS  
**Contexte** : Cours Web Programming 1.x — UFAZ / Unistra  
**Étape** : N1 — Structure des données JSON (1A → 1E)  
**Version** : 1.0.0

---

## 📋 Description

Application **To Do List** Front-End (HTML, CSS, JavaScript, API LocalStorage).

Le projet se déroule en **3 grandes étapes** :

- **Étape 1** : Données JSON (sous-étapes **1A à 1E**) ← *en cours*
- **Étape 2A** : Formulaire web statique (HTML + CSS)
- **Étape 2B** : Formulaire web dynamique (HTML + CSS + JS)
- **Étape 3** : Application web complète (LocalStorage + dashboard)

---

## 🗂️ Organisation des dossiers — Étape 1

/to_do_list
│
├── /étape 1A
│ └── step 1A_Structure_d_UNE_tâche.json
│
├── /étape 1B
│ └── step 1B_Priorités.json
│
├── /étape 1C
│ ├── step 1Ca_Echéances.json
│ ├── step 1Cb_Accomplissement.json
│ └── step 1Cc_Statuts.json
│
├── /étape 1D
│ └── step 1D_Catégories.json
│
├── /étape 1E
│ └── step 1E_HTML_+_tests.html
│
└── to_do_list_README.md


| Dossier | Fichier | Rôle |
|---|---|---|
| `/étape 1A` | `step 1A_Structure_d_UNE_tâche.json` | Structure d'une tâche |
| `/étape 1B` | `step 1B_Priorités.json` | Priorités (Critère 1) |
| `/étape 1C` | `step 1Ca_Echéances.json` | Échéances (Critère 2a) |
| `/étape 1C` | `step 1Cb_Accomplissement.json` | Niveaux d'accomplissement (Critère 2b) |
| `/étape 1C` | `step 1Cc_Statuts.json` | Statuts (Critère 2c) |
| `/étape 1D` | `step 1D_Catégories.json` | Catégories (regroupe les statuts) |
| `/étape 1E` | `step 1E_HTML_+_tests.html` | Page HTML + tests + LocalStorage |

---

## 🔗 Relation PK / FK (Étape 1)

| Table | Clé primaire | Clés étrangères |
|---|---|---|
| `prioritiesList` (1B) | `idPriority` | — |
| `echeancesListe` (1Ca) | `idEcheance` | `idTask` |
| `accomplissementListe` (1Cb) | `idAccomplissement` | `idTask` |
| `statusList` (1Cc) | `idStatus` | — |
| `categoriesList` (1D) | `idCategory` | `idStatus` |
| `tasksList` (1E) | `idTask` | `idPriority` → prioritiesList<br>`idCategory` → categoriesList<br>`idEcheance` → echeancesListe<br>`idAccomplissement` → accomplissementListe |

---

## 🚀 Utilisation (Étape 1)

1. Ouvrir `étape 1E/step 1E_HTML_+_tests.html` dans un navigateur
2. Ouvrir la console **(F12)** pour voir :
   - Les données brutes de chaque fichier JSON
   - La relation **PK/FK** entre les tâches et les critères
   - La **sérialisation LocalStorage** (`stringify` / `parse`)

---

## ✅ Conformité (Étape 1)

- Structure conforme aux consignes du professeur
- 3 fichiers séparés pour l'étape 1C
- Relation PK/FK respectée
- Sérialisation LocalStorage (`stringify` / `parse`)

---

## 🎯 Prochaines étapes

1. **Étape 2A** — Formulaire HTML **statique** (version Mobile)
2. **Étape 2B** — Formulaire HTML **dynamique** (JS + JSON)
3. **Étape 3** — Application complète (LocalStorage + dashboard)

---

## 📌 Notes

- Le projet respecte la logique **Front-End** : pas de Back-End, pas de base MySQL
- Les données sont stockées côté navigateur via **l'API LocalStorage**
- Le code est **commenté** et structuré pour faciliter la maintenance
- Les conventions de nommage du professeur sont respectées (`idXxx`, `validXxx`)

---

**© 2026 — Raoul FOSSUA TINDO & Lovensky DERVIS**