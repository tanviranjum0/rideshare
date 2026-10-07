# QuickRide

Ride-sharing app. React/Vite frontend (`RideFront`, deployed on Vercel) and Node/Express + Socket.IO API (`RideBack`, deployed on Render free tier or Docker/EC2), backed by MongoDB Atlas and Google Maps Platform.

- `RideBack/` — API. See `RideBack/README.md` for environment variables, `RideBack/deploy/README.md` for EC2.
- `RideFront/` — web client. See `RideFront/.env.production.example`.
- `render.yaml` — Render Blueprint for the API (root directory `RideBack`).

## Deploy
1. **API (Render):** New > Blueprint > this repo. Set `MONGODB_PROD_URL`, `GOOGLE_MAPS_API`, `FRONTEND_ORIGINS`, `CLIENT_URL` in the dashboard.
2. **Frontend (Vercel):** import this repo, set Root Directory to `RideFront`. `RideFront/vercel.json` proxies `/api/*` to the Render service.
