# DPAF Orly — Slidev

Présentation PAF Orly — Organisation du contrôle transfrontière.

Utilise le [Design System de l'État Français (DSFR)](https://www.systeme-de-design.gouv.fr/) comme thème visuel (police Marianne, couleurs Bleu France / Rouge Marianne).

## Prérequis

- [Node.js](https://nodejs.org/) >= 18
- npm (inclus avec Node.js)

## Installation

```bash
npm install
```

## Développement

Lancer le serveur de développement avec rechargement à chaud :

```bash
npm run dev
```

La présentation s'ouvre automatiquement sur [http://localhost:3030](http://localhost:3030).

## Build (production)

Générer la version statique dans le dossier `dist/` :

```bash
npm run build
```

Le résultat est un site statique autonome (fonctionne **offline**) qui peut être servi par n'importe quel serveur HTTP :

```bash
npx serve dist
```

## Export PDF

Exporter la présentation en PDF :

```bash
npm run export
```

## Déploiement

Le projet est configuré pour :

- **GitHub Pages** — déploiement automatique via `.github/workflows/deploy.yml` (push sur `main`)
- **Netlify** — configuration dans `netlify.toml`
- **Vercel** — configuration dans `vercel.json`

## Structure du projet

```
├── slides.md          # Contenu des slides (Markdown + Vue)
├── styles/
│   └── dsfr.css       # Thème DSFR (variables, fonts Marianne)
├── public/
│   └── fonts/         # Polices Marianne embarquées (offline)
├── components/        # Composants Vue réutilisables
├── pages/             # Slides additionnelles
└── dist/              # Build de production
```

## Liens utiles

- [Slidev](https://sli.dev/) — framework de présentation
- [DSFR](https://www.systeme-de-design.gouv.fr/) — Design System de l'État
