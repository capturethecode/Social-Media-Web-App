# 🚀 Full-Stack Social Media Website

A modern, full-stack social media platform built from scratch using the **MERN Stack**,
**Socket.IO**, **Cloudinary**, and **JWT Authentication**. The application provides an 
engaging social experience with posts, reels, stories, real-time chat, notifications, and user interactions.

## 🌟 Features

### 👤 User Authentication

* Secure user registration and login
* JWT-based authentication
* Protected routes
* Persistent user sessions
* Secure password handling

### 📝 Posts

* Create and publish posts
* Upload images and videos
* Like and unlike posts
* Comment on posts
* View posts from followed users
* Delete/manage your own posts

### 🎬 Reels

* Upload short-form videos
* Watch reels in an interactive feed
* Like and interact with reels
* Video uploads handled through Cloudinary

### 📖 Stories

* Create and upload stories
* Stories automatically disappear after **24 hours**
* View stories from other users
* Interactive story experience

### 💬 Real-Time Chat

* One-to-one real-time messaging
* Powered by **Socket.IO**
* Instant message delivery
* Online/offline user status
* Real-time communication without refreshing the page

### 🔔 Real-Time Notifications

* Live notifications for user interactions
* Like notifications
* Comment notifications
* Follow notifications
* Real-time updates using Socket.IO

### 👥 Follow System

* Follow and unfollow users
* View followers and following
* Personalized social feed based on connections

### 📸 Media Upload

* Image and video uploads
* Cloudinary integration
* Optimized cloud-based media storage

### 🎨 Responsive UI

* Modern and clean interface
* Fully responsive design
* Built using React.js and Tailwind CSS
* Works across desktop, tablet, and mobile devices

---

## 🛠️ Tech Stack

### Frontend

* **React.js**
* **Tailwind CSS**
* JavaScript
* Axios

### Backend

* **Node.js**
* **Express.js**
* REST APIs
* Socket.IO

### Database

* **MongoDB**
* Mongoose

### Authentication & Security

* **JWT (JSON Web Token)**
* Password hashing

### Media Storage

* **Cloudinary**

### Development Tools

* Git
* GitHub
* VS Code
* Postman

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │       Client        │
                    │      React.js       │
                    │    Tailwind CSS     │
                    └──────────┬──────────┘
                               │
                    REST API / Socket.IO
                               │
                               ▼
                    ┌─────────────────────┐
                    │       Server        │
                    │   Node.js + Express  │
                    └──────┬────────┬─────┘
                           │        │
                    ┌──────▼───┐ ┌──▼──────────┐
                    │ MongoDB  │ │  Cloudinary │
                    │ Database │ │ Image/Video │
                    └──────────┘ └─────────────┘
```

---

## 📂 Project Structure

```text
Social-Media-Website/
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── context/
│   │   ├── services/
│   │   └── App.jsx
│   │
│   └── package.json
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── socket/
│   ├── config/
│   └── server.js
│
├── .gitignore
└── README.md
```

> The exact folder structure may vary depending on your implementation.

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/capturethecode/Social-Media-Website.git

cd Social-Media-Website
```

### 2. Install Dependencies

Install frontend dependencies:

```bash
cd client
npm install
```

Install backend dependencies:

```bash
cd ../server
npm install
```

### 3. Configure Environment Variables

Create a `.env` file inside the `server` directory:

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

Never commit your `.env` file to GitHub.

### 4. Start the Backend

```bash
cd server
npm run dev
```

### 5. Start the Frontend

Open another terminal:

```bash
cd client
npm run dev
```

The application will be available at:

```text
http://localhost:5173
```

---

## 🔄 Application Flow

```text
User
 │
 ▼
React Frontend
 │
 ├── Authentication ──────► JWT
 │
 ├── Posts ───────────────► Express API ─────► MongoDB
 │
 ├── Stories ─────────────► Express API ─────► MongoDB
 │
 ├── Reels ───────────────► Express API ─────► MongoDB
 │
 ├── Media Upload ────────► Cloudinary
 │
 └── Chat/Notifications ──► Socket.IO
```

---

## 🔐 Authentication Flow

```text
User Registration/Login
          │
          ▼
    Backend Validation
          │
          ▼
     Password Hashing
          │
          ▼
     JWT Generation
          │
          ▼
     Authenticated User
          │
          ▼
    Protected API Routes
```

---

## ⚡ Real-Time Communication

The application uses **Socket.IO** to provide real-time functionality.

```text
User A
  │
  │ Send Message
  ▼
Socket.IO Server
  │
  │ Real-Time Event
  ▼
User B
  │
  ▼
Message Appears Instantly
```

The same real-time architecture is used for notifications and other live interactions.

---

## ☁️ Cloudinary Integration

Images and videos are uploaded to Cloudinary instead of storing large media files directly inside MongoDB.

```text
User
 │
 ▼
React Application
 │
 ▼
Backend API
 │
 ▼
Cloudinary
 │
 ▼
Media URL
 │
 ▼
MongoDB
```

MongoDB stores the media URL and associated metadata.

---

## 📱 Core Modules

| Module          | Technology           |
| --------------- | -------------------- |
| Authentication  | JWT                  |
| User Management | MongoDB + Express    |
| Posts           | MERN                 |
| Reels           | React + Cloudinary   |
| Stories         | React + MongoDB      |
| Chat            | Socket.IO            |
| Notifications   | Socket.IO            |
| Media Upload    | Cloudinary           |
| Database        | MongoDB              |
| UI              | React + Tailwind CSS |

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

* Full-stack MERN application development
* REST API design
* Authentication and authorization
* MongoDB database modeling
* Real-time communication with Socket.IO
* Cloud media management using Cloudinary
* React component architecture
* Responsive UI development
* Frontend-backend integration
* Real-time notification systems
* Deploying production-ready web applications

---

## 🚀 Future Improvements

* [ ] Group chat
* [ ] Video calling
* [ ] Advanced search
* [ ] Hashtags and trending posts
* [ ] Recommendation system
* [ ] Infinite scrolling
* [ ] Content moderation
* [ ] Push notifications
* [ ] Dark/light theme
* [ ] AI-powered content recommendations

---

## 📸 Screenshots

Add screenshots of the major features here:

```text
Home Feed
├── Posts
├── Stories
└── Reels

Chat
├── Conversations
└── Real-Time Messages

Profile
├── Posts
├── Followers
└── Following
```

You can add screenshots using:

```markdown
![Home Page](screenshots/home.png)
![Chat](screenshots/chat.png)
![Profile](screenshots/profile.png)
```

---

## 👨‍💻 Author

**Abhishek Kumar**

Computer Science & Engineering
National Institute of Technology, Patna

### Connect With Me

* GitHub: `https://github.com/capturethecode`


---

## ⭐ Show Your Support

If you found this project useful or interesting, consider giving it a **⭐ star** on GitHub!

---

## 📄 License

This project is developed for educational and portfolio purposes.
