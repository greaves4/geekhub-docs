# geekhub-docs

Documentación pública de [Geek Hub](https://geekhub.mx) en Mintlify.

URL de producción: [docs.geekhub.mx](https://docs.geekhub.mx)

## Estructura

```
geekhub-docs/
├── mint.json
├── introduction.mdx / quickstart.mdx / authentication.mdx
├── concepts/          # billing, balance, errors, fallbacks, guardrails, zdr, regions, openrouter
├── api-reference/     # chat, images, videos, audio/speech, embeddings, generation
└── models/            # index, chat, images, videos
```

## Dev local

```bash
npm i -g mintlify
mintlify dev    # http://localhost:3000
```

## Deploy

Push a `main` → Mintlify rebuilds automáticamente.

## Conventions

- Frontmatter `title` + `description` en cada MDX
- Precios de tablas = **USD proveedor**; sell ≈ ×1.09 (ver `concepts/billing.mdx`)
- Fuente de verdad de catálogo: `GET /v1/models` (`geekhub-inference/src/lib/models.ts`)
- No documentar endpoints WIP (p. ej. STT) hasta que estén en `main` del gateway
