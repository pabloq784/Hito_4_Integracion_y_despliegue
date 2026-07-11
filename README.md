# MercadoLocal — Hito 4 Integración y despliegue

Proyecto completo con `frontend/` React + Vite y `backend/` Express + PostgreSQL.

## Local

1. En pgAdmin crea la base y ejecuta `backend/database/schema.sql` y `seed.sql`.
2. Copia `backend/.env.example` a `backend/.env` y configura PostgreSQL.
3. Copia `frontend/.env.example` a `frontend/.env`.
4. En dos terminales:
   - `cd backend && npm install && npm run dev`
   - `cd frontend && npm install && npm run dev`

## Producción

- Backend + PostgreSQL: Render. Usa `backend/render.yaml` o crea ambos servicios manualmente.
- Frontend: Netlify. Base directory `frontend`, build `npm run build`, publish `frontend/dist`.
- En Netlify configura `VITE_API_URL=https://TU-BACKEND.onrender.com/api`.
- En Render configura `CORS_ORIGINS=https://TU-SITIO.netlify.app`.
- En la base online ejecuta `backend/database/schema.sql` y `seed.sql`.

## Correcciones integradas

- Productos desde API, sin mocks ni localStorage.
- Orden real por menor/mayor precio.
- JWT persistido y restauración con `/api/perfil`.
- Carrito solo para usuarios autenticados y persistido en PostgreSQL.
- Cantidades, stock, subtotales, total y pago.
- CRUD de direcciones y publicaciones.
- Indicadores de carga, errores y validaciones.
- Stock descontado al confirmar la orden.
- Configuración `DATABASE_URL`, SSL, CORS y redirects SPA.
