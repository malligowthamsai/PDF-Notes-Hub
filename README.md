# PDF Notes Hub 📚

A modern, full-stack web application to browse, search, view, and download curated PDF notes.

---

## 🛠 Tech Stack

| Layer    | Technology                    |
|----------|-------------------------------|
| Frontend | React 18 + Vite + Tailwind CSS |
| Backend  | Node.js + Express             |
| Routing  | React Router v6               |
| HTTP     | Axios                         |

---

## 📁 Project Structure

```
Pdf-website/
├── backend/
│   ├── server.js          # Express entry point
│   ├── routes/
│   │   └── notes.js       # GET /api/notes, GET /api/notes/:id
│   └── data/
│       └── notes.json     # PDF metadata registry
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   │   └── notesApi.js       # Axios API service
│   │   ├── hooks/
│   │   │   └── useNotes.js       # Notes fetch + filter hook
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── NoteCard.jsx
│   │   │   ├── SearchBar.jsx
│   │   │   ├── CategoryFilter.jsx
│   │   │   ├── LoadingSpinner.jsx
│   │   │   └── EmptyState.jsx
│   │   ├── pages/
│   │   │   ├── HomePage.jsx
│   │   │   └── ViewerPage.jsx
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── index.html
│   ├── vite.config.js
│   └── tailwind.config.js
│
└── public/
    └── pdfs/              # ← Place your PDF files here
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js ≥ 18
- npm ≥ 9

### 1. Install Dependencies

**Backend:**
```bash
cd backend
npm install
```

**Frontend:**
```bash
cd frontend
npm install
```

### 2. Add Your PDFs

Place your PDF files in:
```
public/pdfs/
```

Then register them in `backend/data/notes.json`:
```json
{
  "id": 9,
  "title": "My New Notes",
  "category": "Java",
  "file": "my-new-notes.pdf",
  "description": "A short description.",
  "pages": 30,
  "author": "Your Name",
  "uploadedAt": "2024-01-01"
}
```

### 3. Run the App

**Terminal 1 – Backend:**
```bash
cd backend
npm run dev
# Runs at http://localhost:5000
```

**Terminal 2 – Frontend:**
```bash
cd frontend
npm run dev
# Runs at http://localhost:5173
```

Open [`http://localhost:5173`](http://localhost:5173) in your browser.

---

## 🔌 API Reference

| Method | Endpoint          | Description              |
|--------|-------------------|--------------------------|
| GET    | `/api/notes`      | Get all notes            |
| GET    | `/api/notes/:id`  | Get single note by ID    |
| GET    | `/api/health`     | Server health check      |
| GET    | `/pdfs/:filename` | Serve a PDF file         |

---

## 🎨 Features

- ✅ Hero section with live search bar
- ✅ Category pill filters (Java, DSA, Web Dev, Python, etc.)
- ✅ Responsive card grid (1–4 columns)
- ✅ PDF viewer page with inline iframe
- ✅ Download PDFs directly
- ✅ Loading spinners + empty state handling
- ✅ Error state when backend is unreachable
- ✅ Dark theme with glass morphism UI
- ✅ Smooth animations and hover effects

---

## 🔮 Future Extensions

- [ ] User authentication (JWT / OAuth)
- [ ] PDF upload feature (admin panel)
- [ ] Pagination / infinite scroll
- [ ] Favorites / bookmarks
- [ ] Search with backend database (PostgreSQL / MongoDB)

---

Built with ❤️ by StudyHub Team
