# Web Julsa Industrial

Perfil B — Aplicación web. Repo generado sobre la metodología Nortex (Spec-Driven
Development / OpenSpec + Specboot).

## Fuentes de verdad del proyecto

- `docs/fase2-define-spec.md` — especificación de producto (aprobada, v0.3).
- `docs/fase3-design.md` — diseño visual y wireframes (aprobado, v0.1).
- `openspec/changes/add-web-julsa-r1/` — cambio OpenSpec activo (proposal, design, tasks).
- `docs/base-standards.md` — reglas de desarrollo para todos los agentes.
- `docs/agents-efficiency.md` — reglas de eficiencia de tokens.

## Stack

Next.js + TypeScript · Supabase (Postgres, Auth, Storage) · Vercel.

## Estado

Implementado: web pública (inicio, nosotros, contacto, cuatro líneas de producto, textos
legales), portal de cliente y panel de administración (productos, pedidos y clientes), con
Supabase para base de datos, autenticación y almacenamiento (4 migraciones, con RLS y
endurecimiento de seguridad). 127 tests unitarios, un flujo e2e crítico con Playwright y CI en
GitHub Actions. Las tareas de `openspec/changes/add-web-julsa-r1/tasks.md` no se han ido
marcando y no reflejan este avance.

## Desarrollo

```bash
cp .env.example .env.local   # rellenar con los valores del proyecto Supabase
npm ci
npm run dev
npm run lint && npx tsc --noEmit && npm test
```
