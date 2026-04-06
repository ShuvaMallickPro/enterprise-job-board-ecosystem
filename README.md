# Vue Job Website (Mock API) — v2

A job portal built with **Vue 3 + Vite**, **Pinia**, **Vue Router**, and **TailwindCSS**.  
It includes an **Axios Mock API** (via `axios-mock-adapter`) so the app runs locally without a real backend.

- **Live demo**: [job-website-vuejs.netlify.app](https://job-website-vuejs.netlify.app/)
- **GitHub Repository**: [enterprise-job-board-ecosystem](https://github.com/ShuvaMallickPro/enterprise-job-board-ecosystem)
- **Mock API**: enabled automatically from `src/main.js` (imports `server/`)

---

## Features

### Roles

- **Employer**
  - Create and manage job posts
  - Review applicants (approve / reject / shortlist)
  - Manage company/profile information
- **Job Seeker**
  - Browse and filter jobs
  - View job details
  - Apply to jobs
  - Save/bookmark jobs
  - Manage profile / resume / applications

### App

- **Auth flows**: login & registration (mocked), session stored in **localStorage**
- **Dashboards**: separate employer/job seeker dashboard screens
- **UI**: TailwindCSS + Flowbite components
- **State management**: Pinia stores

---

## Tech stack

- **Frontend**: Vue 3, Vite, Vue Router, Pinia
- **Styling**: TailwindCSS, Flowbite
- **Mock API**: Axios + `axios-mock-adapter`
- **UX utilities**: VueUse, Toast/SweetAlert

---

## Getting started (step-by-step)

### 1) Requirements

- **Node.js**: LTS recommended
- **npm**: comes with Node.js

### 2) Install dependencies

```bash
npm install
```

### 3) Run in development

```bash
npm run dev
```

Then open the local URL shown in your terminal (typically [localhost:5173](http://localhost:5173)).

### 4) Build for production

```bash
npm run build
```

### 5) Preview the production build

```bash
npm run preview
```

---

## Mock API (how it works)

This project uses a **mock API layer** under `server/` powered by `axios-mock-adapter`.

- It is **auto-registered** because `src/main.js` imports `../server`.
- API routes are defined in `server/api/*` (jobs, companies, jobseekers, resumes, auth).
- Data is stored in in-memory arrays inside those mock modules.

---

## Demo credentials

You can log in with these seeded users (from `server/api/authentication.js`):

### Employer

- **Email**: `employer01@gmail.com`
- **Password**: `employer01`

### Job Seeker

- **Email**: `jobseeker@gmail.com`
- **Password**: `jobseeker`

---

## Project structure

```text
.
├─ public/                 # Static files
├─ server/                 # Axios mock API (axios-mock-adapter)
│  ├─ api/                 # Mock endpoints
│  ├─ axios-mock.js        # Axios mock adapter setup
│  └─ index.js             # Registers all mock endpoints
├─ src/
│  ├─ assets/              # Images, fonts, global styles
│  ├─ components/          # Shared components
│  ├─ pages/               # Route pages (jobseeker/employer/etc.)
│  ├─ router/              # Vue Router routes
│  ├─ sections/            # Page sections / feature chunks
│  ├─ stores/              # Pinia stores
│  ├─ App.vue              # Root component
│  └─ main.js              # App entry (registers mock API)
├─ vite.config.js
└─ package.json
```

---

## Recommended IDE setup

- VS Code + Volar (disable Vetur)
- See Vite docs: [Vite Configuration Reference](https://vitejs.dev/config/)

---

## License

Add a license file (MIT/Apache-2.0/etc.) if you plan to publish this publicly.
