# 📰 News Portal

A full-stack news portal application with user authentication, news management, and commenting features.

## 🚀 Features

- **User Authentication**: Register and login with secure JWT-based authentication
- **News Management**: Create, read, update, and delete news articles
- **Comments**: Add comments to news articles
- **Search**: Search news by title
- **Responsive Design**: Clean and modern UI

## 🛠️ Tech Stack

### Backend
- **Node.js** with **Express.js**
- **Prisma ORM** with **PostgreSQL**
- **JWT** for authentication
- **bcryptjs** for password hashing
- **express-validator** for input validation

### Frontend
- **HTML5**, **CSS3**, **JavaScript**
- **Serve** for static file serving

## 📸 Screenshots

### Login Page
![Login Page](screenshots/login.png)

### News List
![News List](screenshots/news-list.png)

### News Detail with Comments
![News Detail](screenshots/news-detail.png)

## 📦 Installation

### Prerequisites
- Node.js (v18+)
- PostgreSQL database

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure environment variables in `.env`:
   ```env
   DATABASE_URL="postgresql://user:password@localhost:5432/newsportal"
   JWT_SECRET="your-secret-key"
   ```

4. Run database migrations:
   ```bash
   npx prisma db push
   ```

5. Seed the database:
   ```bash
   npm run seed
   ```

6. Start the server:
   ```bash
   npm start
   ```

The backend runs on **http://localhost:3000**

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   npm start
   ```

The frontend runs on **http://localhost:5500**

## 👥 Default Users

| Name  | Email               | Password     |
|-------|---------------------|--------------|
| Tarek | tarek@example.com   | password123  |
| Jamil | jamil@example.com   | password123  |
| Adnan | adnan@example.com   | password123  |

## 📁 Project Structure

```
newsPORTAL/
├── backend/
│   ├── src/
│   │   ├── app.js
│   │   ├── server.js
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── routes/
│   │   └── validators/
│   ├── prisma/
│   │   ├── schema.prisma
│   │   ├── seed.js
│   │   └── migrations/
│   └── package.json
├── frontend/
│   ├── index.html
│   ├── login.html
│   ├── news-list.html
│   ├── news-detail.html
│   ├── create-news.html
│   ├── edit-news.html
│   ├── styles.css
│   ├── app.js
│   └── package.json
└── README.md
```

## 🔗 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user

### News
- `GET /api/news` - Get all news
- `GET /api/news/:id` - Get single news
- `POST /api/news` - Create news (auth required)
- `PUT /api/news/:id` - Update news (auth required)
- `DELETE /api/news/:id` - Delete news (auth required)

### Comments
- `GET /api/comments/news/:newsId` - Get comments for a news article
- `POST /api/comments` - Add comment (auth required)

## 📄 License

MIT
