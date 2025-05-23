# 🖼️ React Frontend – Blogging Platform

## ✅ Approach

The React frontend was designed with scalability and user experience in mind. Here's a breakdown of the approach:

### 1. 🧱 Component-Based Architecture
- Modular components like `Navbar`, `PostCard`, `Login`, `Signup`, `Dashboard`, and `PostEditor` make the UI maintainable and reusable.
- Page-level components handle specific views like Home, Dashboard, Create Post, etc.

### 2. 🧭 Client-Side Routing with React Router
- Implemented using `react-router-dom`.
- Routes:
  - `/` – Home (public blog feed)
  - `/login` – Login page
  - `/signup` – Signup page
  - `/dashboard` – User’s posts (protected)
  - `/create` – New blog post (protected)
  - `/edit/:id` – Edit existing post (protected)
  - `/post/:id` – View single post

### 3. 🔒 Private Routes
- `PrivateRoute` component restricts access to authenticated users.
- Relies on presence of JWT token in `localStorage`.

### 4. ✍️ Rich Text Editing
- Integrated **CKEditor 5** for creating and editing blog content with formatting options (bold, italic, lists, etc.).

### 5. 📡 API Communication
- Used `axios` for HTTP requests to the backend.
- Authenticated requests include `Authorization: Bearer <token>` header.
- API base URL configured via environment variables.

### 6. 💻 Form Handling
- Controlled form components using `useState`.
- Prevented default behavior with `e.preventDefault()` and submitted data through axios.

### 7. 🎨 UI Design
- Styled using **Bootstrap** for responsiveness and layout.
- Clean, user-friendly interface with a focus on clarity and readability.

### 8. 🌐 Environment Config
- `.env` file used to configure the backend API base URL.

---

## 🛠️ Setup Instructions

### Prerequisites
- Node.js v18+
- Backend API running (Node.js + MySQL)

---

### 🔧 Installation

```bash
# 1. Clone the frontend repo
git clone https://github.com/akshayjallewar/blog-frontend.git
cd blog-frontend

# 2. Install dependencies
npm install

# 3. Create a .env file
touch .env
```

#### .env file
```env
REACT_APP_API_URL=http://localhost:5000
```

---

### ▶️ Run the App

```bash
npm start
```

The app will start on: `http://localhost:3000`

---

## 🤝 Integration

This frontend connects to the [Node.js + Express backend](https://github.com/your-username/blog-backend) via RESTful APIs.

---

## 🧠 AI Assistance

Throughout development I've used **ChatGPT** to:
- Design and plan component structure
- Resolve issues related to React Router, form handling, and token-based auth
- Integrate CKEditor with React
- Improve code quality and best practices

---
