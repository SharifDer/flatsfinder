
---

## ✅ `README.md` for Fullstack Project (Monorepo)

```markdown
# Flatsfinder – Fullstack Web App

**Flatsfinder** is a web platform connecting apartment owners and renters in Sanaa, Yemen. This monorepo includes both the frontend and backend codebases.

---

## 🧩 Project Structure
fullstack-app/
├── frontend/ # React + TypeScript frontend
│ ├── public/
│ ├── src/
│ │ ├── components/ # Navbar, Footer, AuthModal, etc.
│ │ ├── pages/ # ListingsPage, ApartmentDetail, etc.
│ │ ├── contexts/ # UserPreferenceContext
│ │ ├── hooks/
│ │ └── main.tsx
│ └── tailwind.config.js
│
└── backend/ # FastAPI backend
├── app/
│ ├── auth.py
│ ├── data_fetcher.py
│ └── ...
├── services/
│ ├── apartment_services.py
│ ├── storage_cloudinary.py
│ └── user_services.py
├── config/
│ └── routes.py
├── app_dtypes/
│ ├── request_dtypes.py
│ └── response_dtypes.py
├── main.py
└── requirements.txt


---

## 🔷 Frontend Overview (`/frontend`)

### Features

- Browse apartments with filters
- Save favorites
- Contact property owners
- Onboarding for renters/landlords
- Auth modal for login/signup

### Stack

- **React** (TypeScript)
- **React Router**
- **Tailwind CSS**
- **ShadCN UI**, **Lucide Icons**
- **React Query**

### Key Components

- `Navbar`, `Footer`, `SearchBar`, `ApartmentCard`
- `UserOnboardingModal`, `AuthModal`
- `ListingsPage`, `Favorites`, `Dashboard`, `AddApartment`, etc.

### Mobile Support

- Responsive grid layouts
- Optimized modals
- Collapsible navigation

---

## 🟦 Backend Overview (`/backend`)

### Features

- Firebase-based user auth (via JWT)
- Apartment posting with Cloudinary image upload
- Apartment search and filters
- Auth-guarded routes for landlords

### Stack

- **FastAPI**
- **Firebase Admin SDK**
- **Cloudinary API**
- **Pydantic**

### Main Endpoints

| Method | Endpoint                  | Description                       |
|--------|---------------------------|-----------------------------------|
| POST   | `/auth/create-user`       | Create user via Firebase          |
| POST   | `/auth/login`             | User login                        |
| POST   | `/apartments`             | Post new apartment (auth)         |
| GET    | `/apartments`             | Get apartments with filters       |
| GET    | `/apartments/details`     | Get apartment detail              |
| PATCH  | `/apartments/status`      | Update apartment status (auth)    |

---

## 🔐 Auth Flow

- Auth handled via `AuthModal` on frontend
- Tokens stored in client context
- Backend validates JWT with Firebase

---

## 🚀 Deployment

- **Frontend:** Optimized for deployment with any static host (e.g., Vercel, Netlify)
- **Backend:** Deploy via Docker, Uvicorn/Gunicorn, or any ASGI-compatible platform

---

## ⚙️ Dev Setup

### Clone the repo (with submodules if used):

```bash
git clone --recurse-submodules https://github.com/your-username/fullstack-app.git
