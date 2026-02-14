# Library MERN Application

<p>
  <a href="https://twitter.com/AlphaOmondi" target="_blank">
    <img alt="Twitter: AlphaOmondi" src="https://img.shields.io/twitter/follow/AlphaOmondi.svg?style=social" />
  </a>
</p>

A modern, full-stack Library Book Management application built with the **MERN stack** (MongoDB, Express, React, Node.js) and containerized with Docker and NGINX. This project demonstrates best practices for building production-ready web applications.

## 🚀 Features

- **Book Management**: Create, read, update, and delete books
- **Responsive UI**: Modern React 18 with Bootstrap styling
- **State Management**: Redux with Redux-Thunk for async operations
- **REST API**: Express.js backend with comprehensive error handling
- **Database**: MongoDB with Mongoose ODM
- **Containerization**: Docker and Docker Compose for easy deployment
- **Reverse Proxy**: NGINX for production-grade request handling
- **Database Admin**: Mongo Express for development database management

## 📋 Tech Stack

### Frontend
- **React 18.2.0** - UI library
- **React Router 6.20.1** - Client-side routing
- **Redux 4.2.1** - State management
- **React-Bootstrap 2.10.1** - UI components
- **Axios 1.6.5** - HTTP client

### Backend
- **Node.js 20+** - Runtime
- **Express.js 4.18.2** - Web framework
- **Mongoose 8.0.3** - MongoDB ODM
- **Dotenv 16.3.1** - Environment configuration

### Infrastructure
- **MongoDB 7.0** - Database
- **Docker** - Containerization
- **NGINX 1.25** - Reverse proxy
- **Docker Compose** - Container orchestration

## 📦 Prerequisites

- Docker and Docker Compose installed
- Git
- Environment variables configured

## 🛠️ Installation & Setup

### Using Docker Compose (Recommended)

```bash
git clone https://github.com/API-Imperfect/mern_library_nginx.git
cd mern_library_nginx
docker-compose up --build --remove-orphans
```

Navigate to `http://localhost:8080` in your browser.

### Using Make (if available)

```bash
git clone https://github.com/API-Imperfect/mern_library_nginx.git
cd mern_library_nginx
cd server
make build
```

Then navigate to `http://localhost:8080`

## 🔧 Configuration

Create a `.env` file in the root directory with the following variables:

```env
NODE_ENV=development
MONGO_ROOT_USERNAME=admin
MONGO_ROOT_PASSWORD=password123
DB_NAME=library
PORT=5000
```

## 📁 Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # Reusable React components
│   │   ├── pages/         # Page components
│   │   ├── actions/       # Redux actions
│   │   ├── reducers/      # Redux reducers
│   │   └── App.js         # Main App component
│   └── Dockerfile
├── server/                # Express backend
│   ├── controllers/       # Route handlers
│   ├── models/           # MongoDB schemas
│   ├── routes/           # API routes
│   ├── middleware/       # Custom middleware
│   ├── database/         # Database connection
│   └── Dockerfile
├── nginx/                 # NGINX configuration
│   └── Dockerfile
├── docker-compose.yml     # Container orchestration
└── README.md

```

## 🌐 API Endpoints

### Books
- `GET /api/v1/books` - Get all books
- `GET /api/v1/books/:id` - Get book details
- `POST /api/v1/books` - Create new book
- `DELETE /api/v1/books/:id` - Delete book

## 🐳 Docker Services

The application runs four services:

1. **library-api** (Port 5000) - Express server
2. **mongodb** (Port 27017) - MongoDB database
3. **mongo-express** (Port 8081) - Database admin interface
4. **nginx** (Port 8080) - Reverse proxy & static file server

## 📝 Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `NODE_ENV` | Application environment | development |
| `MONGO_ROOT_USERNAME` | MongoDB admin username | admin |
| `MONGO_ROOT_PASSWORD` | MongoDB admin password | password123 |
| `DB_NAME` | Database name | library |
| `PORT` | Server port | 5000 |

## 🔄 What's New in v2.0

- ✅ Upgraded to React 18 with latest hooks
- ✅ React Router 6 with new routing paradigm
- ✅ Mongoose 8 with simplified configuration
- ✅ Node.js 20 LTS base images
- ✅ NGINX 1.25 with latest security patches
- ✅ MongoDB 7.0 for better performance
- ✅ Updated all dependencies to latest stable versions
- ✅ Improved error handling and middleware

## 🤝 Contributing

Contributions are welcome! Feel free to submit pull requests or open issues.

## 📄 License

MIT

Copyright (c) 2024-2026 API-Imperfect
