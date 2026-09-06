# SasyaSamanvay

SasyaSamanvay is a static HTML frontend with a small local Node.js backend for development.

## Run locally

Requirements: Node.js 18 or newer.

```powershell
npm start
```

Open http://localhost:3000 in a browser.

The server hosts the HTML pages and exposes the API from the same origin, so no CORS setup is needed.

## Development credentials

Farmer OTP: `123456` after requesting an OTP with any valid 10-digit mobile number.

Staff accounts use password `password`:

- Center In-Charge: `AP-CTR-0231`
- Quality Inspector: `AP-QCI-0042`
- Quantity Inspector: `AP-QNI-0018`
- Disbursing Officer: `AP-DO-0077`

## API currently connected

- `POST /api/auth/farmer/request-otp`
- `POST /api/auth/farmer/verify-otp`
- `POST /api/farmers`
- `GET /api/farmers/:id/dashboard`
- `POST /api/slots/:slotId/book`
- `POST /api/auth/staff/login`

Development data is stored in `data/store.json`, which is ignored by Git. This is intentionally a local demo backend; production use should replace the fixed OTP, demo passwords, JSON storage, and in-memory session tokens with a real identity provider, database, and secure session management.
