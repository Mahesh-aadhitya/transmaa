# Transmaa

A unified logistics platform combining truck booking, a pre-owned commercial vehicle marketplace, and finance/insurance enquiries — for customers, drivers, and staff, on one backend.

## Live

- App: https://transmaa-orpin.vercel.app
- API: https://transmaa-backend-71cb.onrender.com

The landing page offers three portals: **Customer**, **Staff**, and **Driver**.

## Logging in

- **Customer / Driver**: log in with a registered mobile number or email. An OTP is sent to the registered email address. A static demo code also always works, for quick testing.
- **Staff**: log in with a registered mobile number and password (staff accounts are provisioned by an admin).

New customers and drivers can self-register from their respective login screens.

## Structure

```
backend/    Node/Express + MongoDB API, shared by all three portals
frontend/   React + Vite single-page app (customer, staff, driver routes)
```

## Local development

```bash
# Backend
cd backend
npm install
npm run dev      # requires a .env with MONGODB_URI, JWT_SECRET, etc.

# Frontend
cd frontend
npm install
npm run dev
```

The frontend defaults to `http://localhost:5050` for the API in development (`VITE_API_BASE_URL` overrides this).
