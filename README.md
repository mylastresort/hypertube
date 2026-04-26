# Hypertube

Hypertube is a full-stack web application that allows users to search, discover, and stream movies directly from the browser.  
The platform supports real-time torrent-based video streaming using **HLS**, secure authentication, and a modern responsive interface.

---

## 🎥 Demo

[![Hypertube Demo](https://img.youtube.com/vi/L0X-5HPQMko/maxresdefault.jpg)](https://www.youtube.com/watch?v=L0X-5HPQMko)

---

## 🧱 Tech Stack

### Frontend
- **Next.js**
- **TypeScript**
- **React**
- **HLS.js** (HTTP Live Streaming)
- **WebSockets** (real-time updates)
- Responsive UI (Desktop & Mobile)

### Backend
- **Go (Golang)**
- RESTful API
- OAuth2 Authentication
- **HLS stream generation**
- **WebSocket server**

### Database
- **PostgreSQL**

### Infrastructure & DevOps
- **Docker & Docker Compose**
- **Nginx** (Reverse Proxy & HLS delivery)
- Environment-based configuration (`.env`)

---

## ✨ Features

### Authentication & Users
- User registration with:
  - Email
  - Username
  - First name
  - Last name
  - Password (securely hashed)
- OAuth authentication:
  - **42**
  - **Google**
  - **GitHub**
- Login / Logout
- Password reset via email
- User profile management (avatar, personal information)
- Public user profiles (email remains private)
- Preferred language selection (default: English)

---

### Library & Search
- Accessible only to authenticated users
- Movie search using **at least two external video sources**
- Display results as thumbnails
- Display popular movies when no search is performed
- Infinite scroll pagination (asynchronous loading)
- Sorting & filtering:
  - Name
  - Genre
  - IMDb rating
  - Production year
- Watched vs unwatched movie distinction

---

### 🎬 Video Streaming (HLS)
- Integrated video player
- Server-side torrent handling
- **Progressive streaming via HLS**
- Playback starts before full download
- Automatic HLS segment generation (`.m3u8`)
- Browser-compatible streaming
- On-the-fly video format conversion when required (MKV support)
- Cached movies stored on server
- Automatic cleanup of unwatched movies after 30 days

---

### 📝 Comments
- Authenticated users can post comments on movies
- Real-time comment updates via **WebSockets**
- Edit and delete own comments
- Display comment history per movie

---

### 🔌 Real-Time Features (WebSockets)
- Live streaming status updates
- Torrent download progress
- Real-time comment updates
- Non-blocking background processing

---

### 🔗 REST API
- OAuth2-secured REST API
- Public access to front-page movies
- Authenticated access to:
  - Users
  - Movies
  - Comments
- Strict HTTP method handling
- Fully RESTful architecture

### 🔗 PROJECT STRUCTURE
├── frontend/              # Next.js application
│   ├── src/
│   ├── public/
│   └── package.json
│
├── backend/               # Go API & streaming server
│   ├── cmd/
│   ├── internal/
│   ├── streaming/         # Torrent + HLS logic
│   ├── websocket/         # WebSocket handlers
│   └── main.go
│
├── nginx/
│   └── nginx.conf         # HLS & reverse proxy config
│
├── docker-compose.yml
├── .env.example
└── README.md


### 🔗 PROJECT STRUCTURE
- HLS streaming
- Multiple OAuth providers
- Web Sockets
- Background processing optimizations









