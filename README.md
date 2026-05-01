# informationgeometrygroup

Site do grupo de estudos, feito com SvelteKit e publicado no GitHub Pages.

## Desenvolvimento local

```sh
npm install
npm run dev -- --open
```

## Build

```sh
npm run build
npm run preview
```

## Deploy (GitHub Pages)

- O deploy roda via GitHub Actions em `main` e publica no GitHub Pages.
- Em **Settings → Pages**, selecione **Source: GitHub Actions**.

O projeto já está configurado para funcionar em `https://<usuario>.github.io/<repo>/` (com `BASE_PATH` ajustado no workflow).
