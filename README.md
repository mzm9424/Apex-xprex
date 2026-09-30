# APEXEXPRESS Logistics Tracking Demo

A modern parcel tracking dashboard built with React and Vite for a simulated global logistics workflow. The app showcases shipment status tracking, customs hold handling, dispatcher controls, and role-based parcel status updates for a courier / freight operations demo.

## Overview

This project is a single-page logistics tracking application for viewing parcel journeys across shipping zones, including:

- live-looking parcel tracking results
- on-hold customs detention workflows
- dispatcher terminal for status updates
- authentication and role validation patterns in middleware
- simulated administrative actions for customs clearance release

The app uses a dark freight-ops design system with orange, white, and black accents to resemble a high-visibility logistics platform.

## Features

- Parcel lookup by tracking code
- Shipment lifecycle views for in-transit and on-hold states
- Customs hold simulation for Cairo / Egypt detention flow
- Dispatcher terminal with role-based authorization keys
- Timeline and status tracking history for each parcel
- Local storage-backed parcel records for demo persistence
- Responsive single-page UI built in React

## Tech Stack

- React 19
- TypeScript
- Vite
- Tailwind CSS
- Lucide React icons
- Express
- dotenv
- Google GenAI SDK

## Project Structure

```text
.
├── database/
│   ├── parcels.json
│   └── users.db
├── middleware/
│   └── auth.js
├── public/
│   ├── images/
│   ├── on-hold.html
│   ├── result.html
│   └── track.html
├── src/
│   ├── App.tsx
│   ├── assets/
│   ├── index.css
│   └── main.tsx
├── .env.example
├── .gitignore
├── index.html
├── metadata.json
├── package.json
├── tsconfig.json
├── vite.config.ts
└── README.md
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Install dependencies

```bash
npm install
```

### Run the app in development mode

```bash
npm run dev
```

The app will start on:

```text
http://localhost:3000
```

### Build for production

```bash
npm run build
```

### Preview production build

```bash
npm run preview
```

## Demo Credentials

The app includes sample authorization keys used in the dispatcher and customs workflows. These are defined in `middleware/auth.js`:

- `APEX-DISPATCH-990` — Dispatcher role
- `EGY-CUST-AUTH-41` — Cairo customs officer role
- `DEMO-KEY-2026` — Supervisor/demo role

These credentials are intended for demo and testing use within the app.

## Environment Variables

A sample environment file is included at `.env.example`.

```env
# Example environment values
PORT=3000
```

Copy it to a real environment file if needed for your local configuration.

## Notes

- This repository includes mock parcel data and simulated operational workflows rather than production logistics infrastructure.
- The app stores parcel state in browser localStorage by default for demo persistence.
- The code in `middleware/auth.js` demonstrates validation logic for parcel identifiers and status transition permissions.
- Some UI assets and static pages under `public/` are used as part of the demo experience.

## License

This project does not currently declare a repository license in the GitHub metadata. If you plan to distribute or reuse it, confirm the intended licensing before publication.

## Contributing

Contributions are welcome. For local development:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run the build and verify the app locally
5. Open a pull request

## Support

For questions about project behavior or demo flows, review the application code and middleware examples in:

- `src/App.tsx`
- `middleware/auth.js`
- `database/parcels.json`
