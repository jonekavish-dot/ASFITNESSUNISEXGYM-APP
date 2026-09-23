# ASFITNESSUNISEXGYM-APP
🏋️ A.S. Fitness Command Center — Full-stack gym management system with Firebase sync, dual-portal access, and real-time attendance tracking.

## Repository layout

This repo holds two independent apps. Each has its own Firebase project and deploys separately.

| Path | App | Firebase project |
|------|-----|------------------|
| `public/`, `firebase.json`, `.firebaserc` | **A.S. Fitness portal**: gym portal (`index.html`) + admin portal (`admin.html`). See [`public/readme.md`](public/readme.md). | `gym-portal-9b223` |
| `ps76/` | **GymFlow**: PS76 hackathon build (BIZ HACK '26), membership & class booking. See [`ps76/README.md`](ps76/README.md). | `ps76-gym` |
| `.github/workflows/ps76.yml` | CI for `ps76/`: rules tests, deploy on `main` | – |

Deploy the portal from the repo root with `firebase deploy`. Deploy GymFlow from `ps76/` (see its README).
