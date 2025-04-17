# Finance Tracker (Parent Repository)

This repository acts as a **lightweight monorepo** that links together the two main parts of the Finance Tracker application via Git submodules:

- **Frontend** (`/frontend`) → [finance-tracker-client](https://github.com/lauraAlabau/finance-tracker-client)
- **Backend** (`/backend`) → [finance-tracker-server](https://github.com/lauraAlabau/finance-tracker-server)

---

## Project Structure
finance-tracker/ 

├── frontend/ # React + Vite + Tailwind + TypeScript (Git submodule)

├── backend/ # Node.js + Express + MongoDB + TypeScript (Git submodule)

├── .gitmodules # Submodule configuration


## Cloning the Repository with Submodules

To clone this repo with its submodules, use:

```bash
git clone --recurse-submodules git@github.com:lauraAlabau/finance-tracker.git
```

If you've already cloned the repo without submodules:

```bash
git submodule update --init --recursive
```

## Keeping Submodules Updated

```bash
cd frontend
git pull origin main
```
```bash
cd ../backend
git pull origin main
```
```bash
cd ..
git add .
git commit -m "Update submodules to latest commits"
git push
```

## Tech Stack
###Frontend
- Framework: React + TypeScript
- Bundler: Vite
- Styling: Tailwind CSS
- Authentication: Clerk (with @clerk/clerk-react and @clerk/themes)
- Routing: React Router
- Forms: React Hook Form
- Data Tables: React Table
- Utilities: date-fns
- Linting: ESLint with TypeScript plugin

###Backend
- Language: TypeScript (Node.js)
- Framework: Express.js
- Database: MongoDB (via Mongoose)
- Environment variables: dotenv
- Development tooling: Nodemon, ts-node
