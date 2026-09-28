# VAJRA — Project Structure

## 📁 Complete Project Structure

This document describes the **actual project structure** of the uploaded VAJRA prototype ZIP. The structure below follows the folders and files present in the ZIP rather than using a separate architecture diagram or an assumed project layout.

## Directory Structure

```text
vajra/
├── 📁 src/                                      # React + TypeScript source code
│   ├── 📁 components/                           # Reusable UI components
│   │   ├── 📁 settings/
│   │   │   └── VajraSettingsView.tsx            # Settings interface
│   │   ├── 📁 surveillance/
│   │   │   └── CctvMonitoringView.tsx            # CCTV monitoring interface
│   │   ├── 📁 biometric/
│   │   │   ├── BiometricCardShell.tsx            # Shared biometric card layout
│   │   │   ├── 📁 iris/
│   │   │   │   └── IrisAuthorization.tsx         # Iris authorization
│   │   │   ├── 📁 face/
│   │   │   │   └── FaceAuthorization.tsx         # Face authorization
│   │   │   └── 📁 voice/
│   │   │       └── VoiceAuthorization.tsx        # Voice authorization
│   │   ├── 📁 verification/
│   │   │   ├── SecureVerificationScreen.tsx      # Secure verification screen
│   │   │   └── AccessDeniedScreen.tsx            # Access denied screen
│   │   └── 📁 landing/
│   │       └── VajraAuthLanding.tsx               # Authentication/landing flow
│   ├── 📁 data/
│   │   └── surveillanceData.ts                    # Surveillance data and records
│   ├── 📁 assets/
│   │   └── 📁 images/
│   │       ├── patrol_squad_quarry_1790587044924.jpg
│   │       ├── patrol_quarry_aerial_1790587172706.jpg
│   │       ├── ladakh_valley_recon_1790587935781.jpg
│   │       ├── military_convoy_base_1790588267244.jpg
│   │       └── perimeter_razor_fence_1790588470115.jpg
│   ├── App.tsx                                   # Main React application
│   ├── main.tsx                                  # React application entry point
│   └── index.css                                 # Global styles
│
├── 📁 public/                                    # Static assets served directly
│   ├── 📁 surveillance/
│   │   ├── camera01.mp4
│   │   ├── camera02.mp4
│   │   ├── camera03.mp4
│   │   ├── camera04.mp4
│   │   ├── rec_camera01_1830.mp4
│   │   ├── rec_camera02_1915.mp4
│   │   ├── rec_camera03_2200.mp4
│   │   └── rec_camera04_0230.mp4
│   ├── drone_feed_jk.jpg
│   ├── india_cyber_map.jpg
│   ├── report_drone.jpg
│   ├── report_heatmap.jpg
│   ├── report_ied.jpg
│   ├── report_infiltration.jpg
│   ├── satellite_feed_sector4.jpg
│   ├── naval_base_port.jpg
│   └── loc_road_feed.jpg
│
├── 📄 index.html                                 # HTML entry page
├── 📄 server.ts                                  # Express/Node.js development server
├── 📄 package.json                               # Project scripts and dependencies
├── 📄 package-lock.json                          # Locked npm dependency versions
├── 📄 bun.lock                                   # Bun dependency lock file
├── 📄 vite.config.ts                             # Vite configuration
├── 📄 tsconfig.json                              # TypeScript configuration
├── 📄 metadata.json                              # Project metadata
├── 📄 .env.example                               # Environment variable template
├── 📄 .gitignore                                 # Git ignore rules
└── 📄 README.md                                  # Project setup and run instructions

```

## Key Directories and Files Explained

### 📁 `src/` — Frontend Source Code

The `src/` directory contains the React + TypeScript application code.

- **`components/`** — Reusable screens and UI components.
- **`components/biometric/`** — Iris, face, and voice authorization components.
- **`components/verification/`** — Secure verification and access-denied screens.
- **`components/surveillance/`** — CCTV monitoring interface.
- **`components/settings/`** — VAJRA settings interface.
- **`components/landing/`** — Authentication and landing flow.
- **`data/`** — Surveillance data used by the application.
- **`assets/images/`** — Images used by the React application.
- **`App.tsx`** — Main application component and application flow.
- **`main.tsx`** — React entry point.
- **`index.css`** — Global application styling.

### 📁 `public/` — Public Assets

The `public/` directory contains static media that can be referenced directly by the application.

- **`surveillance/`** — CCTV live-feed and recorded surveillance videos.
- **Image files** — Drone, satellite, map, report, naval-base, and road-feed imagery used by the prototype.

### 📄 Root Configuration Files

- **`package.json`** — Defines the project scripts, dependencies, and development dependencies.
- **`package-lock.json`** — Locks npm dependency versions.
- **`bun.lock`** — Bun dependency lock file included in the project.
- **`vite.config.ts`** — Vite build and development configuration.
- **`tsconfig.json`** — TypeScript compiler configuration.
- **`server.ts`** — Node.js/Express server used to run the development application.
- **`index.html`** — Main HTML entry document.
- **`.env.example`** — Example environment-variable configuration.
- **`metadata.json`** — Project metadata.
- **`.gitignore`** — Files and folders excluded from version control.
- **`README.md`** — Project setup and local run instructions.

## 🧩 Frontend Structure

The uploaded prototype follows this frontend organization:

```text
Frontend
└── React + TypeScript
    ├── Components
    │   ├── Landing
    │   ├── Biometric
    │   │   ├── Iris
    │   │   ├── Face
    │   │   └── Voice
    │   ├── Verification
    │   ├── Surveillance
    │   └── Settings
    ├── Data
    ├── Assets
    ├── App.tsx
    ├── main.tsx
    └── index.css
```

## 🖥️ Backend / Server Structure

The uploaded ZIP contains a Node.js server at the project root:

```text
Backend / Server
└── server.ts
    └── Express + Node.js
```

The frontend is served through the Node.js/Express development server defined in `server.ts`, while Vite handles the frontend development/build workflow.

## 🎥 Surveillance Assets

The surveillance portion of the project is organized as:

```text
public/
└── surveillance/
    ├── camera01.mp4
    ├── camera02.mp4
    ├── camera03.mp4
    ├── camera04.mp4
    ├── rec_camera01_1830.mp4
    ├── rec_camera02_1915.mp4
    ├── rec_camera03_2200.mp4
    └── rec_camera04_0230.mp4
```

The corresponding React surveillance implementation is located in:

```text
src/
├── components/
│   └── surveillance/
│       └── CctvMonitoringView.tsx
└── data/
    └── surveillanceData.ts
```

## 🔐 Biometric Verification Structure

The biometric verification components are separated by modality:

```text
src/components/biometric/
├── BiometricCardShell.tsx
├── iris/
│   └── IrisAuthorization.tsx
├── face/
│   └── FaceAuthorization.tsx
└── voice/
    └── VoiceAuthorization.tsx
```

This matches the uploaded prototype's implementation of separate **iris, face, and voice authorization** components.

## 🔄 Verification Flow Structure

The verification-related screens are organized separately:

```text
src/components/
├── landing/
│   └── VajraAuthLanding.tsx
├── biometric/
│   ├── iris/
│   ├── face/
│   └── voice/
└── verification/
    ├── SecureVerificationScreen.tsx
    └── AccessDeniedScreen.tsx
```

## 📦 Project Dependencies

The uploaded `package.json` defines the project as an ES-module application and includes React, React DOM, Vite, Express, TypeScript, Tailwind/Vite tooling, MapLibre, Recharts, Motion, Lucide React, jsPDF, dotenv, and Google GenAI dependencies.

## ▶️ Running the Project

Based on the uploaded project's `package.json` and `README.md`, the main local workflow is:

```bash
# Install dependencies
npm install

# Start the development application
npm run dev

# Build the application
npm run build

# Preview the production build
npm run preview

# Run TypeScript checking
npm run lint

# Start the Node.js server
npm run start
```

## 🧭 Project Navigation

### For Frontend Development

```text
src/
├── components/
├── data/
├── assets/
├── App.tsx
├── main.tsx
└── index.css
```

### For Backend / Server Development

```text
server.ts
```

### For Static Media

```text
public/
```

### For Project Configuration

```text
package.json
package-lock.json
bun.lock
vite.config.ts
tsconfig.json
metadata.json
.env.example
.gitignore
```

## 📊 Project Structure Summary

| Area | Location | Purpose |
|---|---|---|
| Frontend | `src/` | React + TypeScript application |
| UI Components | `src/components/` | Application screens and reusable components |
| Biometric | `src/components/biometric/` | Iris, face, and voice authorization |
| Surveillance | `src/components/surveillance/` | CCTV monitoring |
| Data | `src/data/` | Surveillance/application data |
| Frontend Assets | `src/assets/` | Images used by React |
| Public Assets | `public/` | Static images and surveillance videos |
| Backend/Server | `server.ts` | Node.js/Express server |
| Build Tool | `vite.config.ts` | Vite configuration |
| TypeScript | `tsconfig.json` | TypeScript configuration |
| Dependencies | `package.json` | Scripts and packages |
| Documentation | `README.md` | Setup and run instructions |

## 📁 Actual ZIP Contents

The structure above is based on the uploaded ZIP contents, including the following major areas:

- `src/`
- `src/components/`
- `src/components/biometric/`
- `src/components/biometric/iris/`
- `src/components/biometric/face/`
- `src/components/biometric/voice/`
- `src/components/verification/`
- `src/components/landing/`
- `src/components/settings/`
- `src/components/surveillance/`
- `src/data/`
- `src/assets/images/`
- `public/`
- `public/surveillance/`
- `server.ts`
- `package.json`
- `vite.config.ts`
- `tsconfig.json`
- `index.html`
- `README.md`

---

**This document intentionally uses the term “Project Structure” and reflects the actual folder/file organization of the uploaded VAJRA prototype ZIP.**
