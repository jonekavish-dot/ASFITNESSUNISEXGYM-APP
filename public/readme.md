# 💪 A.S. Fitness — Command Center

> A complete gym management system built for **A.S. Fitness**, featuring a dual-portal 
> architecture with real-time Firebase sync, secure multi-user authentication, and 
> a fully responsive mobile-first design.

---

## 🏗️ Architecture

| Portal | User | Purpose |
|--------|------|---------|
| `index.html` — Gym Portal | Shankar (Owner) | Day-to-day gym operations |
| `admin.html` — Admin Portal | Kavish S R (Developer) | Analytics, oversight & control |

Both portals share the same **Firebase Firestore** database — any change 
on one portal reflects on the other in real time (< 2 seconds).

---

## ✨ Features

### 🏋️ Gym Portal
- **Member Management** — Add, edit, renew members with plan selection (A/B · Strength/Cardio)
- **Exercise Categories A–F** — 6 training types, each with 7 exercises. Members are assigned a category on joining
- **Smart Attendance** — Exercise checkbox system per member category. Present button disabled until at least one exercise is ticked
- **Renewal System** — 1/3/6/12 month renewal with plan change option, editable fee, payment method selection, and automatic revenue tracking
- **Revenue Analytics** — Real monthly revenue charts built from actual join dates and renewal dates (no fake data)
- **Trainers & Schedule** — Manage trainers, sessions, and their attendance separately
- **Export** — Members, trainers, and attendance exported to Excel, PDF, and CSV
- **Firebase Settings** — Password-gated Firebase config with registered account management
- **Auto-Logout** — 3-minute inactivity timer with 30-second warning before logout

### 🔐 Admin Portal
- **Dashboard** — 8 live KPI cards including total revenue, renewal revenue, and today's attendance
- **Attendance Viewer** — Date-preserved attendance view showing exercises completed per member, color-coded by status
- **Exercise Analytics** — Category distribution cards, most-done exercises today, attendance by category
- **Member Table** — Searchable, filterable, paginated table with renewal history and total paid
- **Trainer Attendance** — Staff attendance tracking separate from members
- **Firebase Auth** — Email/Password login with multi-user support and secondary app for account creation
- **Auto-Logout** — 3-minute inactivity timer matching gym portal

---

## 🔐 Security

- **Firebase Email Authentication** — Server-side auth, no local password bypass possible
- **Session via `sessionStorage`** — Survives page refresh, clears on tab close
- **No cached auth bypass** — Firebase session is explicitly cleared on fresh page load
- **Password-gated Firebase settings** — Config fields hidden behind gym password
- **No password hints** — Failed login attempts never reveal the password
- **Auto-logout** — 3 minutes of inactivity logs out automatically on both portals

---

## ⚡ Tech Stack

| Technology | Usage |
|-----------|-------|
| **HTML5 / CSS3 / Vanilla JS** | Single-file architecture, no frameworks |
| **Firebase Firestore** | Real-time cloud database, offline persistence |
| **Firebase Authentication** | Email/Password multi-user auth |
| **IndexedDB** | Local offline storage for gym portal |
| **Chart.js** | Revenue trends, growth charts, analytics |
| **jsPDF + AutoTable** | PDF export |
| **SheetJS (XLSX)** | Excel export |
| **CSS Grid + Flexbox** | Responsive layout |

---

## 📱 Responsive Design

- **Desktop (> 900px)** — Full sidebar, all table columns, multi-column charts
- **Tablet (600–900px)** — Collapsed sidebar, hamburger menu, stacked charts
- **Mobile (< 600px)** — Bottom navigation bar, slide-up modals, touch-optimized attendance cards

---

## 🔄 Real-Time Data Sync