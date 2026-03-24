# OpenG7 Medical Referral Router

![OpenG7 Medical Referral Router](docs/assets/banner-openg7-medical-referral-router.png)

Open-source platform for routing medical referrals across facilities, regions, specialties, and operational constraints.

## Investor Pitch

OpenG7 Medical Referral Router transforms fragmented referral coordination into a usable operational workflow. Instead of relying on phone trees, PDFs, local habits, and manual escalation, teams get a shared routing surface that can suggest viable referral paths based on availability, urgency, geography, and service constraints.

Funding this repository helps deliver:
- Decision-grade visibility across referral paths, wait pressure, and routing bottlenecks
- A vendor-neutral stack built on Angular, shared API contracts, and open referral logic
- Faster coordination through triage-aware rules, filters, and structured transfer workflows
- A stronger bridge between administrative teams, receiving facilities, and regional planners

Near-term funding unlocks:
- Better referral intake and matching flows
- Stronger routing explainability and corridor analysis
- More resilient rule configuration, search, and eligibility modeling
- Hardening of operator tooling for real-world interfacility coordination

How to support:
- GitHub Sponsors
- Pilot partnerships
- Public-sector collaboration
- Data and integration partnerships
- In-kind infrastructure or expert review

---

**Languages:** [English](#english) | [Français](#francais)

<a id="english"></a>

## English

### What it is

OpenG7 Medical Referral Router is an open-source repository for a referral coordination platform. It helps route care requests toward appropriate services based on operational criteria rather than fragmented local knowledge alone.

The repository is intended to support:
- an Angular front-end for referral intake, routing views, and decision support
- shared contracts for referral requests, constraints, routing decisions, and explanations
- operator-facing workflows for referral intake, reassignment, escalation, and tracking
- documentation for routing logic, governance, and policy boundaries

This project is not a diagnostic engine and not a replacement for clinical judgment. It is a coordination and routing layer.

### Why it exists

Referral workflows often fail where complexity rises: incomplete visibility into destination options, uneven intake rules, inconsistent routing practices, and low transparency on why a path was chosen.

OpenG7 Medical Referral Router exists to provide:
- a unified routing surface for non-diagnostic referral coordination
- explainable routing decisions based on operational criteria
- reusable routing contracts, selectors, and orchestration patterns
- a documented foundation that can evolve across specialties and jurisdictions

### What it enables

- Referral intake and normalization
- Specialty and service matching
- Urgency-sensitive routing support
- Geographic and transfer-aware destination ranking
- Routing explanations and override workflows
- Escalation tracking and backlog visibility

### Repository Structure

- `src/app/core/`: app bootstrap, providers, config, routing, guards
- `src/app/shared/`: UI primitives, utilities, helpers, reusable models
- `src/app/features/medical-referral-router/`: referral routing domain
- `src/app/features/medical-referral-router/pages/`: page-level route shells
- `src/app/features/medical-referral-router/components/`: intake forms, result lists, explanations, queues
- `src/app/features/medical-referral-router/data-access/`: API clients, adapters, routing DTOs
- `src/app/features/medical-referral-router/store/`: global state for cross-app routing context when needed
- `src/app/features/medical-referral-router/signals/`: local signal-first orchestration
- `docs/`: onboarding, architecture, routing policies, roadmap
- `packages/contracts/`: shared contracts and validation schemas
- `infra/`: deployment and infrastructure manifests

### Suggested Front-End Surfaces

- `src/app/features/medical-referral-router/pages/referral-router-page.component.ts`
- `src/app/features/medical-referral-router/components/referral-intake-form/referral-intake-form.component.ts`
- `src/app/features/medical-referral-router/components/routing-results/routing-results.component.ts`
- `src/app/features/medical-referral-router/components/routing-explanation/routing-explanation.component.ts`
- `src/app/features/medical-referral-router/components/referral-queue/referral-queue.component.ts`
- `src/app/features/medical-referral-router/components/escalation-panel/escalation-panel.component.ts`

### Getting Started

1. Enable Corepack and verify Yarn:
   ```bash
   corepack enable
   yarn --version
   ```
2. Install dependencies:
   ```bash
   yarn install
   ```
3. Create a local environment file if needed:
   ```bash
   cp .env.example .env.local
   ```
4. Start the web application:
   ```bash
   yarn dev
   ```
5. Run tests:
   ```bash
   yarn test
   ```

Useful repo-level scripts:
- `yarn dev`
- `yarn test`
- `yarn test:e2e`
- `yarn lint`
- `yarn typecheck`
- `yarn build`

Detailed guides live in `docs/`:
- `docs/getting-started.md`
- `docs/architecture.md`
- `docs/routing-model.md`
- `docs/policies.md`
- `docs/roadmap.md`

### Routing Surfaces

The platform is expected to support operator surfaces for routing and coordination.

Examples:
- referral intake board
- match suggestions with explanations
- corridor-aware destination ranking
- reassignment and escalation workflows
- backlog and delay visibility

### Where does code live?

- Use `src/app/features/medical-referral-router/` for domain UI and orchestration
- Keep local state signal-first close to each routing workflow
- Use `src/app/features/medical-referral-router/store/` only for global context that truly spans the app
- Put routing contracts in `packages/contracts/`
- Keep policy boundaries documented in `docs/`

### Contributing

Read `CONTRIBUTING.md` for workflow, checks, and security expectations.
The code of conduct in `CODE_OF_CONDUCT.md` applies to all community spaces.
Support and governance details live in `SUPPORT.md`.

Community first steps:
- Use issue and PR templates
- Add screenshots for visible UI changes
- Document any operational, privacy, or policy impact
- Prefer explainable and testable routing increments

### License & Security

- License: MIT (`LICENSE`)
- Responsible disclosure: see `SECURITY.md`

---

<a id="francais"></a>

## Français

### Ce que c'est

OpenG7 Medical Referral Router est un dépôt open source pour une plateforme de coordination des références médicales. Il aide à orienter les demandes de soins vers les bons services selon des critères opérationnels, plutôt que de dépendre uniquement de la connaissance locale fragmentée.

Le dépôt a pour but de soutenir :
- un front Angular pour l’entrée des demandes, les vues de routage et l’aide à la décision
- des contrats partagés pour les requêtes de référence, contraintes, décisions de routage et explications
- des parcours opérateurs pour l’entrée, la réaffectation, l’escalade et le suivi des références
- une documentation sur la logique de routage, la gouvernance et les frontières de politique

Ce projet n’est ni un moteur diagnostique ni un remplacement du jugement clinique. C’est une couche de coordination et de routage.

### Pourquoi ce projet existe

Les parcours de référence échouent souvent quand la complexité augmente : visibilité incomplète sur les destinations possibles, règles d’entrée inégales, pratiques de routage incohérentes et faible transparence sur les raisons d’un choix.

OpenG7 Medical Referral Router sert à fournir :
- une surface de routage unifiée pour la coordination non diagnostique des références
- des décisions de routage explicables selon des critères opérationnels
- des contrats, sélecteurs et patterns d’orchestration réutilisables
- une base documentée qui peut évoluer à travers les spécialités et juridictions

### Ce que ça permet

- Entrée et normalisation des références
- Appariement par spécialité et par service
- Support de routage sensible à l’urgence
- Classement des destinations selon la géographie et les transferts
- Explications de routage et workflows de dérogation
- Suivi des escalades et visibilité sur les arriérés

### Structure du dépôt

- `src/app/core/` : bootstrap applicatif, providers, configuration, routing, guards
- `src/app/shared/` : primitives UI, utilitaires, helpers, modèles réutilisables
- `src/app/features/medical-referral-router/` : domaine du routage des références
- `src/app/features/medical-referral-router/pages/` : shells de pages et surfaces de routes
- `src/app/features/medical-referral-router/components/` : formulaires d’entrée, résultats, explications, files
- `src/app/features/medical-referral-router/data-access/` : clients API, adaptateurs, DTOs de routage
- `src/app/features/medical-referral-router/store/` : état global quand un contexte de routage doit être partagé
- `src/app/features/medical-referral-router/signals/` : orchestration locale signal-first
- `docs/` : onboarding, architecture, politiques de routage, roadmap
- `packages/contracts/` : contrats partagés et schémas de validation
- `infra/` : manifests de déploiement et infrastructure

### Surfaces front-end suggérées

- `src/app/features/medical-referral-router/pages/referral-router-page.component.ts`
- `src/app/features/medical-referral-router/components/referral-intake-form/referral-intake-form.component.ts`
- `src/app/features/medical-referral-router/components/routing-results/routing-results.component.ts`
- `src/app/features/medical-referral-router/components/routing-explanation/routing-explanation.component.ts`
- `src/app/features/medical-referral-router/components/referral-queue/referral-queue.component.ts`
- `src/app/features/medical-referral-router/components/escalation-panel/escalation-panel.component.ts`

### Pour commencer

1. Activez Corepack et vérifiez Yarn :
   ```bash
   corepack enable
   yarn --version
   ```
2. Installez les dépendances :
   ```bash
   yarn install
   ```
3. Créez un fichier d’environnement local au besoin :
   ```bash
   cp .env.example .env.local
   ```
4. Lancez l’application web :
   ```bash
   yarn dev
   ```
5. Lancez les tests :
   ```bash
   yarn test
   ```

Scripts utiles à la racine :
- `yarn dev`
- `yarn test`
- `yarn test:e2e`
- `yarn lint`
- `yarn typecheck`
- `yarn build`

Guides détaillés dans `docs/` :
- `docs/getting-started.md`
- `docs/architecture.md`
- `docs/routing-model.md`
- `docs/policies.md`
- `docs/roadmap.md`

### Surfaces de routage

La plateforme vise à supporter des surfaces opérateurs pour le routage et la coordination.

Exemples :
- tableau d’entrée des références
- suggestions d’appariement avec explications
- classement des destinations sensible aux corridors
- workflows de réaffectation et d’escalade
- visibilité sur les retards et files d’attente

### Où vit le code ?

- Utilisez `src/app/features/medical-referral-router/` pour l’UI métier et l’orchestration
- Gardez l’état local en signal-first près de chaque workflow de routage
- Utilisez `src/app/features/medical-referral-router/store/` seulement pour le contexte global réellement transverse
- Placez les contrats de routage dans `packages/contracts/`
- Documentez les frontières de politique dans `docs/`

### Contribuer

Lisez `CONTRIBUTING.md` pour le workflow, les vérifications et les attentes de sécurité.
Le code de conduite dans `CODE_OF_CONDUCT.md` s’applique à tous les espaces communautaires.
Les détails de support et de gouvernance sont dans `SUPPORT.md`.

Premiers pas communautaires :
- utilisez les templates d’issues et de PR
- ajoutez des captures pour les changements UI visibles
- documentez tout impact opérationnel, de confidentialité ou de politique
- privilégiez des incréments de routage explicables et testables

### Licence & sécurité

- Licence : MIT (`LICENSE`)
- Divulgation responsable : voir `SECURITY.md`
