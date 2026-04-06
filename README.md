# Base réglementaire — Faisabilité architecturale Belle-Île-en-Mer

## Objet
Ce repository constitue la **base de données réglementaire** alimentant l'outil de pré-faisabilité architecturale de [desarchitectures.fr](https://desarchitectures.fr).

Il est consulté en temps réel par l'IA pour analyser la cohérence entre un projet client et le cadre réglementaire en vigueur sur Belle-Île-en-Mer.

---

## Structure

```
/
├── communes/
│   ├── le-palais/
│   │   ├── zones.json          ← Zonages PLU + règles par zone
│   │   └── servitudes.json     ← Servitudes spécifiques (à créer)
│   ├── bangor/
│   │   └── zones.json
│   ├── sauzon/
│   │   └── zones.json
│   └── locmaria/
│       └── zones.json
│
├── reglementation-generale/
│   ├── loi-littoral.md         ← Loi Littoral appliquée à Belle-Île
│   ├── abf.md                  ← Prescriptions ABF UDAP Morbihan
│   ├── natura2000.md           ← Périmètres et contraintes Natura 2000
│   └── scot.md                 ← SCoT (à créer)
│
└── README.md
```

---

## Format des fichiers zones.json

Chaque fichier `zones.json` contient la liste des zones du PLU communal avec :

| Champ | Description |
|---|---|
| `code` | Code de zone (UA, UB, N, A...) |
| `libelle` | Intitulé complet de la zone |
| `constructible` | true / false |
| `types_autorises` | Liste des types de projets autorisés |
| `hauteur_max` | Hauteur maximale autorisée |
| `emprise_sol_max` | Emprise au sol maximale (%) |
| `abf` | Soumis à avis ABF (true/false) |
| `loi_littoral` | Loi Littoral applicable (true/false) |
| `natura2000` | Périmètre Natura 2000 (true/false) |
| `prescriptions_architecturales` | Liste des prescriptions imposées |
| `interdictions` | Liste des interdictions |
| `notes` | Commentaires libres de l'architecte |

---

## Mise à jour

Ce fichier est maintenu par l'équipe [desarchitectures](https://desarchitectures.fr).

**Fréquence de mise à jour recommandée** :
- Après toute révision ou modification de PLU communal
- Après tout arrêté préfectoral modifiant les périmètres ABF ou Natura 2000
- Après évolution législative significative (loi, ordonnance, décret)

**Avertissement** : Ces données sont fournies à titre indicatif et ne constituent pas un document réglementaire opposable. Seuls les documents d'urbanisme officiels (PLU approuvés, arrêtés, servitudes) font foi. Une consultation directe des services instructeurs est toujours recommandée.

---

## Licence
Usage interne — desarchitectures.fr — Tous droits réservés.
