# ASFITNESSUNISEXGYM-APP

🏋️ A.S. Fitness Command Center — Full-stack gym management system with Firebase sync, dual-portal access, and real-time attendance tracking.

This repo holds the **A.S. Fitness portal** only, and is kept as the reference
implementation of the gym's day-to-day system.

| Path | App | Firebase project |
|------|-----|------------------|
| `public/`, `firebase.json`, `.firebaserc` | Gym portal (`index.html`) + admin portal (`admin.html`). See [`public/readme.md`](public/readme.md). | `gym-portal-9b223` |

Deploy from the repo root with `firebase deploy`.

## Related project

The PS76 / BIZ HACK '26 build (**GymFlow**) previously lived in `ps76/` here. It now has
its own repository, so the two evolve independently:

**https://github.com/jonekavish-dot/GYMFLOW_CODEAVENGERS_BIZ-HACK** — Firebase project `ps76-gym`

GymFlow started as a port of this portal's features. This repo stays unchanged as the
reference; new hackathon work happens there.
