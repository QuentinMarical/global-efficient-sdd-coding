# AGENTS.md — Contexte & Règles du Projet

> **Directive agent :** Applique systématiquement le protocole de la Skill `global-efficient-sdd-coding` (divulgation progressive, FinOps, SDD, Zero-Trust) en t'appuyant sur les paramètres ci-dessous.

## 1. Stack Technique & Versions Cibles (Anti-Obsolescence)
- **Langage / Runtime :** [ex. Node.js 22 LTS / Python 3.13 / .NET 9]
- **Framework principal :** [ex. Next.js 15 (App Router) / FastAPI 0.115]
- **Base de données / ORM :** [ex. PostgreSQL 17 + Drizzle ORM]
- **Tests & Qualité :** [ex. Vitest, Ruff, ESLint 9 (flat config)]
- **Interdictions explicites (Legacy) :** [ex. Pas de Pages Router, pas de `moment.js`, pas d'appels `fetch` sans gestion de timeout]

## 2. Carte du Dépôt (Divulgation Progressive)
Ne parcours pas tout le dépôt. Cible directement ces répertoires :
- `/specs` : Spécifications fonctionnelles et techniques (source de vérité avant tout code).
- `/src/core` : Logique métier pure (indépendante de l'interface et du réseau).
- `/src/api` : Routes, contrôleurs et validation des entrées.
- `/tests` : Tests unitaires et d'intégration.

## 3. Commandes de Validation
Exécute ces commandes pour vérifier ton travail (en cas d'échec, n'extrais que la ligne d'erreur pertinente) :
- **Linter / Typage :** `[ex. pnpm lint && pnpm typecheck]`
- **Tests unitaires :** `[ex. pnpm test]`
- **Build :** `[ex. pnpm build]`

## 4. Zones Protégées (Zero-Trust)
- **Accès/modification interdits sans accord explicite :** `.env*`, `/infra`, `.github/workflows/*`, migrations déjà appliquées.
- **Dépendances externes :** Aucune installation de nouveau paquet sans validation humaine préalable. Privilégie les API natives.

## 5. Définition de « Terminé » (Definition of Done)
Une tâche n'est considérée comme achevée que lorsque :
1. Le code respecte strictement la spécification dans `/specs` (aucune fonctionnalité non demandée).
2. Les modifications sont chirurgicales (*small diffs*).
3. Les tests unitaires couvrent la modification et passent avec succès.
4. Le linter et le typage ne remontent aucune erreur.
