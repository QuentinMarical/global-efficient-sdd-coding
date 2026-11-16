# global-efficient-sdd-coding

Skill pour agents de code (Claude Code et compatibles) qui impose un protocole d'ingénierie unifié :

1. **FinOps des tokens** — divulgation progressive du dépôt, effort de raisonnement calibré, sorties filtrées, concision.
2. **Spec-First (SDD) & anti-obsolescence** — pas de « vibe coding », alignement sur la stack réelle du projet.
3. **Zero-Trust** — moindre privilège, protection des secrets, validation humaine avant les actions destructrices ou l'ajout de dépendances.
4. **Validation chirurgicale** — tests et contrôles locaux avant de déclarer une tâche terminée.

## Installation

Avec la CLI des skills :

```bash
npx skills add QuentinMarical/global-efficient-sdd-coding -g -y
```

Ou à la main (global, pour tous vos projets) :

```bash
git clone https://github.com/QuentinMarical/global-efficient-sdd-coding.git
cp -r global-efficient-sdd-coding/skills/global-efficient-sdd-coding ~/.claude/skills/
```

Sous Windows (PowerShell), le dossier cible est `$env:USERPROFILE\.claude\skills\`. Redémarrez ensuite Claude Code pour que la skill soit détectée.

## Utilisation

Ajoutez à l'`AGENTS.md` de votre projet la directive suivante (modèle complet dans [`templates/AGENTS.template.md`](templates/AGENTS.template.md)) :

> **Directive agent :** Applique systématiquement le protocole de la Skill `global-efficient-sdd-coding`.

## Contenu

- [`skills/global-efficient-sdd-coding/SKILL.md`](skills/global-efficient-sdd-coding/SKILL.md) — la skill.
- [`templates/AGENTS.template.md`](templates/AGENTS.template.md) — modèle d'`AGENTS.md` à compléter (stack, carte du dépôt, commandes de validation, zones protégées, définition de « Terminé »).

## Licence

[MIT](LICENSE)
