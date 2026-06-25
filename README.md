# geekhub-docs

Documentación pública de [Geek Hub](https://geekhub.mx) en Mintlify.

URL de producción: [docs.geekhub.mx](https://docs.geekhub.mx)

## Estructura

```
geekhub-docs/
├── mint.json              # Config Mintlify (nav, theme, branding)
├── introduction.mdx       # Landing
├── quickstart.mdx         # 5-min start guide
├── authentication.mdx     # API keys
├── concepts/
│   ├── billing.mdx        # CFDI, MXN, markup
│   ├── balance.mdx        # Saldo, descuentos
│   └── errors.mdx         # Catálogo de errores
├── api-reference/
│   ├── chat/
│   │   ├── overview.mdx
│   │   └── completions.mdx
│   ├── images/
│   │   ├── overview.mdx
│   │   └── generations.mdx
│   └── videos/
│       ├── overview.mdx
│       ├── generations.mdx
│       └── poll.mdx
├── models/
│   ├── index.mdx
│   ├── chat.mdx
│   ├── images.mdx
│   └── videos.mdx
└── logo-{light,dark}.svg + favicon.svg
```

## Dev local

```bash
npm i -g mintlify
mintlify dev    # http://localhost:3000
```

## Deploy

Push a `main` → Mintlify rebuilds automáticamente.

Setup inicial:
1. Sign in en [mintlify.com](https://mintlify.com) con GitHub
2. Conecta este repo
3. Configura custom domain: `docs.geekhub.mx`
4. Agrega CNAME `docs.geekhub.mx` → `cname.mintlify.com` en tu DNS

## Conventions

- Frontmatter con `title` + `description` en cada MDX
- Code blocks con language tag para syntax highlighting
- Usa `<CodeGroup>` para mostrar el mismo ejemplo en Python/Node/curl
- Usa `<Card>`, `<CardGroup>` para CTAs visuales
- Usa `<Info>`, `<Warning>`, `<Tip>` para callouts
- Mantén precios sincronizados con `geekhub-inference/src/lib/models.ts`
