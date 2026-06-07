# ADP Volley-Ball — Outil EPS d'aide à la décision
## CRMEF Inezgane · CRMEF-SM-EPS_Coll3_EQ_01 · Promotion 2025-2026

Outil de diagnostic et de planification pédagogique différenciée en Volley-Ball.

---

## 🚀 Déploiement sur GitHub Pages

### Structure du dépôt

```
/                        ← racine du dépôt
├── index.html           ← redirection automatique vers /outil/
├── .nojekyll            ← empêche Jekyll de traiter les fichiers
├── README.md            ← ce fichier
└── outil/               ← application compilée (ne pas modifier)
    ├── index.html
    └── assets/
        ├── index-*.js
        └── index-*.css
```

### Étapes de déploiement

1. **Créer un dépôt GitHub** (ex: `adp-volley-eps`)
2. **Pousser ce dossier** à la racine du dépôt (`main` branch)
3. **Activer GitHub Pages** :
   - Aller dans `Settings → Pages`
   - Source : `Deploy from a branch`
   - Branch : `main` / `/ (root)`
   - Cliquer sur **Save**
4. L'URL sera : `https://votre-compte.github.io/adp-volley-eps/`

---

## ✅ Fonctionnalités

| Condition | Statut | Détail |
|-----------|--------|--------|
| 1. 100 % autonome sans serveur | ✅ | HTML/CSS/JS statiques compilés par Vite |
| 2. Données privées & locales | ✅ | localStorage uniquement + bandeau informatif |
| 3. Persistance automatique | ✅ | Autosauvegarde toutes les 0,8 s dans localStorage |
| 4. Responsive mobile | ✅ | Tailwind CSS, boutons tactiles, layout adaptatif |
| 5. Bouton Réinitialiser avec confirmation | ✅ | Modal ResetModal avec double confirmation |
| 6. Export JSON + Import JSON | ✅ | Téléchargement de session + re-import fichier |
| 7. Export CSV + Impression PDF | ✅ | CSV UTF-8 BOM (Excel/arabe) + window.print() |
| 8. Données de démonstration | ✅ | Bouton "Données tests (échantillon)" — 10 élèves |
| 9. Chemins relatifs | ✅ | `base: './'` dans vite.config.ts |
| 10. Structure GitHub Pages | ✅ | `index.html` racine + redirect vers `outil/` |

---

## 📱 Utilisation hors connexion

Une fois la page chargée dans le navigateur, l'outil fonctionne **sans connexion internet** (terrain de sport). Toutes les données sont stockées localement.

## 📂 Format CSV d'import

```csv
Nom_Eleve ; Equipe ; Resultat ; Victoire ; C1 ; C2 ; C3
Pierre ; E1 ; 15-10 ; O ; N1 ; N2 ; N1
Marie ; E1 ; 15-10 ; O ; N2 ; N3 ; N2
Jean ; E2 ; 10-15 ; N ; N3 ; N1 ; N1
```

- Séparateur : `;` ou `,`
- Niveaux : `N1`, `N2`, `N3` (ou `A`, `B`, `C`)
- Victoire : `O` (oui) ou `N` (non)
