# suivi-psy

Un skill Claude qui donne à une IA une posture et des garde-fous pour accompagner une personne suivie en santé mentale : dépression, anxiété, prévention de la rechute, questions sur le traitement ou la thérapie.

## Ce que c'est

- Une **posture** : parler comme un proche compétent, pas comme un manuel ni un coach.
- Des **garde-fous** : jamais de diagnostic, jamais de modification de traitement, jamais d'interprétation d'une séance, priorité absolue à l'équipe soignante.
- Un **protocole de sécurité** face au risque suicidaire, avec des critères clairs et un garde-fou contre la sur-réaction.
- Une **boîte à outils** issue des thérapies cognitivo-comportementales : distorsions cognitives, séquence de Beck, questionnement socratique, activation comportementale, repérage des signaux de rechute.
- Une **couche de fond** en psychologie clinique : modèles de la dépression, rechute, rémission, TCC, EMDR, approche multimodale.
- Des **modèles de profil** pour personnaliser le skill sans jamais publier ses données.

## Ce que ce n'est pas

Ce n'est ni un thérapeute, ni un dispositif médical, ni un outil de diagnostic. Il est conçu pour **compléter** un suivi humain existant, pas pour le remplacer. Si tu traverses une période difficile sans suivi, commence par en parler à ton médecin traitant.

**En cas d'urgence en France : 3114** (prévention du suicide, gratuit, 24 h/24), **15** ou **112**.

## Structure

```
suivi-psy/
├── SKILL.md                              posture, sécurité, autorités, anti-patterns
├── references/
│   ├── guide-operationnel.md             mode d'emploi détaillé et boîte à outils
│   ├── psychologie-clinique-condensee.md couche théorique de fond
│   └── sources.md                        ouvrages de référence et urgences
└── modeles/                              modèles de profil à remplir
    ├── profil-clinique.md
    ├── contexte-de-vie.md
    └── dossier-pro.md
```

## Installation

**Claude Code** : copier le dossier `suivi-psy/` dans `~/.claude/skills/`.

**Claude.ai** : compresser le dossier `suivi-psy/` en zip et l'importer depuis les paramètres, dans la section consacrée aux skills.

## Personnalisation

Le skill fonctionne sans profil, en mode générique. Il devient vraiment utile avec un profil :

1. Créer un dossier `suivi-psy/profil/`.
2. Y copier les fichiers de `modeles/` et les remplir.
3. Réinstaller le skill.

Le dossier `profil/` est exclu par le `.gitignore`. **Ne publie jamais tes données de santé.** Si tu forkes ce dépôt, vérifie avant chaque commit qu'aucun fichier personnel n'est suivi.

## Sources

Le contenu clinique est une synthèse rédigée à partir d'ouvrages de référence listés dans [`references/sources.md`](suivi-psy/references/sources.md). Aucun extrait de ces ouvrages n'est reproduit, ils sont protégés par le droit d'auteur.

## Contribuer

Corrections cliniques, ressources d'urgence d'autres pays, traductions : les issues et pull requests sont bienvenues. Toute contribution clinique doit citer sa source.

## Licence

[CC BY 4.0](LICENSE) : réutilisation libre, y compris commerciale, avec mention de la source.
