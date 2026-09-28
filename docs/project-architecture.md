# Project Architecture

## Architecture Overview

VAJRA follows a modular web-application architecture where the user interface, backend services, surveillance data and media assets are separated.

```text
                    VAJRA
                      │
          ┌───────────┴───────────┐
          │                       │
     Frontend                 Backend
   React + TS                Node + Express
          │                       │
   ┌──────┼────────┐        ┌─────┼──────┐
   │      │        │        │     │      │
Auth   CCTV   Dashboard   Settings Health Audit
   │      │        │        │     │      │
   └──────┴────────┴────────┴─────┴──────┘
                      │
             Surveillance Data
                      │
              CCTV Video Assets
```

## Frontend Architecture

### React Application

The frontend contains reusable components for:

- Authentication
- Biometric verification
- CCTV monitoring
- Surveillance analytics
- Settings
- Dashboard views

### Main Source Structure

```text
src/
├── components/
│   ├── biometric/
│   ├── landing/
│   ├── verification/
│   ├── surveillance/
│   └── settings/
├── data/
├── assets/
├── App.tsx
├── main.tsx
└── index.css
```

## Backend Architecture

The backend is implemented using Node.js and Express.

```text
server.ts
   │
   ├── Health API
   ├── Settings API
   ├── Settings Persistence
   ├── Audit Logs
   └── Configuration Reset
```

## CCTV Architecture

```text
CCTV / Recorded Video
        ↓
public/surveillance/
        ↓
CCTV Monitoring Component
        ↓
Video Playback + HUD
        ↓
Operator Dashboard
```

The prototype contains four camera videos and four recorded CCTV clips.

## Surveillance Data Architecture

```text
surveillanceData.ts
        │
        ├── Cameras
        ├── Recordings
        ├── Human Detections
        ├── Vehicle Analytics
        ├── Face Detections
        ├── ANPR Matches
        ├── Virtual Fence Events
        ├── Suspicious Activities
        ├── Night Movement
        ├── Alerts
        └── Event Logs
```

## Authentication Architecture

```text
Login
  ↓
Service / Rank Verification
  ↓
Password / PIN
  ↓
Iris
  ↓
Face
  ↓
Voice
  ↓
Access Granted
  ↓
VAJRA Dashboard
```

## Project Directory

```text
VAJRA/
├── public/
│   └── surveillance/
│       ├── camera01.mp4
│       ├── camera02.mp4
│       ├── camera03.mp4
│       ├── camera04.mp4
│       ├── rec_camera01_1830.mp4
│       ├── rec_camera02_1915.mp4
│       ├── rec_camera03_2200.mp4
│       └── rec_camera04_0230.mp4
│
├── src/
│   ├── components/
│   ├── data/
│   ├── assets/
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
│
├── server.ts
├── package.json
├── vite.config.ts
├── tsconfig.json
├── index.html
└── README.md
```

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React + TypeScript |
| Build Tool | Vite |
| Backend | Node.js + Express |
| Styling | Tailwind CSS |
| Charts | Recharts |
| Maps | MapLibre GL |
| Reports | jsPDF |
| Icons | Lucide React |
| AI SDK | Google GenAI SDK |
| Media | MP4 CCTV videos |

## Future Architecture Expansion

The prototype can later be extended with:

- Real IP/RTSP CCTV streams
- Real-time AI inference
- Central event database
- Production ANPR
- Real-time alert delivery
- Role-based access control
- Additional camera nodes
- Secure production deployment
