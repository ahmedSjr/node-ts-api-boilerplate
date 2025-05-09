# Node.js + TypeScript Boilerplate

A modern, production-ready boilerplate for building **Node.js APIs** using **TypeScript**, **Express**, **MongoDB**, **Winston logging**, and **Morgan HTTP logging**. This template follows best practices for scalability, security, and maintainability.

---

## 🚀 Features

- ⚙️ **TypeScript 5.3+** — Latest TypeScript features with strict typing
- 🌐 **Express 5.x** — Modern, fast, unopinionated web framework
- 📦 **Node.js 22 Ready** — Configured for the latest LTS features
- 🛡️ **Security First** — Built-in protection with `helmet`, `cors`, and environment configs
- 📜 **Advanced Logging** — Structured logging with `winston` and HTTP logging via `morgan`
- 🧹 **Code Quality** — ESLint + Prettier setup for consistent code style
- 📁 **Clean Architecture** — Modular design with clear separation of concerns
- 🔄 **Hot Reload** — Fast development with `nodemon`
- 🗃️ **MongoDB Integration** — Ready-to-use MongoDB setup with Mongoose
- 🎯 **Type Safety** — Full TypeScript support with custom type definitions

---

## 📁 Project Structure

```
project-root/
├── src/
│   ├── app.ts              # Express app configuration
│   ├── server.ts           # Server entry point
│   ├── config/            # Configuration files
│   ├── controllers/       # Request handlers
│   ├── middleware/        # Custom Express middlewares
│   ├── models/           # Mongoose models
│   ├── routes/           # API routes
│   ├── services/         # Business logic
│   ├── templates/        # Email or view templates
│   ├── types/           # TypeScript type definitions
│   └── utils/           # Utility functions and helpers
├── logs/                # Application logs (git-ignored)
├── .env.example         # Environment variables template
├── package.json         # Dependencies and scripts
├── tsconfig.json       # TypeScript configuration
├── eslint.config.js    # ESLint configuration
└── .gitignore         # Git ignore rules
```

---

## 🛠️ Getting Started

### Prerequisites

- Node.js 22.x or later
- npm 10.x or later
- MongoDB 7.x or later

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd <project-directory>
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Setup

Copy the example environment file:

```bash
cp .env.example .env
```

Configure your `.env` file with appropriate values.

---

## 🚧 Development

Start the development server with hot reload:

```bash
npm run dev
```

The server will restart automatically when files change.

---

## 🏁 Production Build

Build and run for production:

```bash
npm run build
npm start
```

---

## 📦 Environment Variables

Required variables in `.env`:

```env
PORT=3000
NODE_ENV=development
MONGO_URI=mongodb://localhost:27017/your-db
```

---

## 📝 Logging Setup

This project uses Winston for structured logging. Logs are written to files in the `logs` directory:

```bash
mkdir logs  # Create the logs directory
```

The following log files will be automatically created:

- `logs/error.log` - For error level logs
- `logs/combined.log` - For all logs (info, warn, error)

Note: The `logs` directory is included in `.gitignore` to prevent log files from being committed to version control.

Directory structure for logs:

```
project-root/
└── logs/
    ├── error.log
    └── combined.log
```

---

## 🧹 Code Quality

This project uses ESLint and Prettier for code quality and formatting:

```bash
# Run ESLint
npm run lint

# Format code with Prettier
npm run format
```

---

## 🔍 API Documentation

### Health Check

```
GET /api/health
```

Returns server status information.

Response:

```json
{
  "status": "ok",
  "timestamp": "2024-xx-xx..."
}
```

---
