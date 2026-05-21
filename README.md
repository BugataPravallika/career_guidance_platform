# Career Guidance Platform

A comprehensive full-stack web application designed to provide career guidance and support to students and professionals. The platform offers resources about colleges, companies, communities, and real-time chat functionality for discussions and mentorship.

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Installation](#installation)
- [Running the Project](#running-the-project)
- [Scripts](#scripts)
- [Environment Configuration](#environment-configuration)

## 🎯 About the Project

The Career Guidance Platform is a MERN stack application that connects students and professionals with:
- **College Information**: Detailed information about various colleges and institutions
- **Company Profiles**: Information about companies and career opportunities
- **Communities**: Join groups and communities with shared interests
- **Real-time Chat**: Live chat rooms for discussions, mentorship, and networking
- **User Authentication**: Secure login and registration system
- **Contact Forms**: Easy way to get in touch for inquiries

This platform helps students make informed decisions about their career paths and connects them with industry professionals and educational institutions.

## ✨ Features

- 🔐 **User Authentication** - Secure registration and login with JWT
- 💬 **Real-time Chat** - Socket.io powered chat rooms and group discussions
- 🏫 **College Information** - Browse and search colleges with detailed information
- 🏢 **Company Profiles** - Explore companies and career opportunities
- 👥 **Communities** - Join interest-based communities and discussion groups
- 📧 **Contact Forms** - Easy contact system for inquiries
- 🎨 **Modern UI** - Beautiful and responsive user interface with Tailwind CSS
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices

## 🛠️ Tech Stack

### Frontend
- **React 19.1.0** - UI library
- **Vite 6.3.5** - Build tool and dev server
- **React Router DOM 7.6.0** - Client-side routing
- **Tailwind CSS 4.1.7** - Styling and UI framework
- **Framer Motion 12.15.0** - Animations
- **Socket.io Client 4.8.1** - Real-time communication
- **Lucide React 0.511.0** - Icon library
- **React Icons 5.5.0** - Additional icon library
- **SweetAlert2 11.21.2** - Beautiful alerts
- **Microlink JSON View 1.26.2** - JSON visualization

### Backend
- **Node.js** - JavaScript runtime
- **Express 5.1.0** - Web framework
- **MongoDB 8.15.1** - Database (with Mongoose ODM)
- **Socket.io 4.8.1** - Real-time communication
- **JWT (jsonwebtoken 9.0.2)** - Authentication
- **Bcryptjs 3.0.2** - Password hashing
- **CORS 2.8.5** - Cross-Origin Resource Sharing
- **Zod 3.24.4** - Schema validation
- **Dotenv 16.5.0** - Environment variables

## 📁 Folder Structure

```
career_guidance_platform/
├── client/                          # Frontend React application
│   ├── src/
│   │   ├── components/              # Reusable React components
│   │   │   ├── cardsGrid.jsx
│   │   │   ├── ChatbotWidget.jsx
│   │   │   ├── ChatPage.jsx
│   │   │   ├── Collapsible.jsx
│   │   │   ├── CollegeDetails.jsx
│   │   │   ├── CollegeLeftSidebar.jsx
│   │   │   ├── Companies/
│   │   │   ├── LeftSidebar.jsx
│   │   │   ├── Navbar.jsx
│   │   │   └── RightPanel.jsx
│   │   ├── pages/                   # Page components
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── Logout.jsx
│   │   │   ├── Awareness.jsx
│   │   │   ├── AwarenessPage.jsx
│   │   │   ├── Colleges.jsx
│   │   │   ├── CollegesPage.jsx
│   │   │   ├── Companies.jsx
│   │   │   ├── CompaniesPage.jsx
│   │   │   ├── Community.jsx
│   │   │   ├── chatRoom.jsx
│   │   │   ├── GroupedChatRoom.jsx
│   │   │   ├── Contact.jsx
│   │   │   └── Error.jsx
│   │   ├── data/                    # Static data and constants
│   │   ├── store/                   # State management (Zustand/Redux)
│   │   ├── assets/                  # Images and static assets
│   │   ├── App.jsx                  # Main App component
│   │   ├── main.jsx                 # React entry point
│   │   └── index.css                # Global styles
│   ├── public/                      # Static public assets
│   ├── index.html                   # HTML template
│   ├── vite.config.js              # Vite configuration
│   ├── package.json
│   ├── package-lock.json
│   └── .eslintrc.js                # ESLint configuration
│
├── server/                          # Backend Express application
│   ├── models/                      # MongoDB schemas (Mongoose)
│   │   └── ChatMessage.js
│   ├── controllers/                 # Route controllers
│   ├── router/                      # API routes
│   │   ├── auth-router.js
│   │   ├── contact-router.js
│   │   ├── postRoutes.js
│   │   └── chatRoutes.js
│   ├── mildlewares/                 # Express middlewares
│   │   └── err-middleware.js
│   ├── validators/                  # Input validation
│   ├── utils/                       # Utility functions
│   │   └── db.js                    # Database connection
│   ├── server.js                    # Main server file
│   ├── .env                         # Environment variables (not in git)
│   ├── package.json
│   └── package-lock.json
│
├── .git/                            # Git version control
├── .gitignore                       # Git ignore file
├── vite.config.js                   # Root Vite configuration
└── README.md                        # This file
```

## 🚀 Installation

### Prerequisites
- **Node.js** (v14 or higher)
- **npm** (comes with Node.js)
- **MongoDB** (local or MongoDB Atlas)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/BugataPravallika/career_guidance_platform.git
   cd career_guidance_platform
   ```

2. **Install server dependencies**
   ```bash
   cd server
   npm install
   ```

3. **Install client dependencies**
   ```bash
   cd ../client
   npm install
   ```

4. **Configure environment variables**
   
   Create a `.env` file in the `server` directory:
   ```env
   PORT=5000
   MONGO_URI=mongodb://localhost:27017/career_guidance
   FRONTEND_URL=http://localhost:3000
   BACKEND_URL=http://localhost:5000
   JWT_SECRET=your_secret_key_here
   ```
   
   For **MongoDB Atlas** (cloud):
   ```env
   MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/career_guidance?retryWrites=true&w=majority
   ```

## ▶️ Running the Project

### Option 1: Run Both Servers Separately

**Terminal 1 - Start Backend Server:**
```bash
cd server
node server.js
```
Backend will run on: `http://localhost:5000`

**Terminal 2 - Start Frontend Dev Server:**
```bash
cd client
npm run dev
```
Frontend will run on: `http://localhost:3000` or `http://localhost:5173`

### Option 2: Use Multiple Terminals

In the project root directory, open two terminals:

**Terminal 1:**
```bash
cd server
npm install --force
node server.js
```

**Terminal 2:**
```bash
cd client
npm install
npm run dev
```

## 📜 Scripts

### Frontend Scripts (from `client/` directory)
```bash
npm run dev        # Start development server
npm run build      # Build for production
npm run lint       # Run ESLint
npm run preview    # Preview production build
```

### Backend Scripts (from `server/` directory)
```bash
node server.js     # Start the server
npm test           # Run tests (currently not set up)
```

## 🔧 Environment Configuration

### Server `.env` file
Create a `.env` file in the `server` directory with the following variables:

```env
# Server Configuration
PORT=5000
BACKEND_URL=http://localhost:5000

# Client Configuration
FRONTEND_URL=http://localhost:3000

# Database Configuration
MONGO_URI=mongodb://localhost:27017/career_guidance
# OR for MongoDB Atlas:
# MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/career_guidance?retryWrites=true&w=majority

# JWT Configuration
JWT_SECRET=your_secret_key_here
JWT_EXPIRE=7d

# Email Configuration (if needed)
# EMAIL_SERVICE=gmail
# EMAIL_USER=your_email@gmail.com
# EMAIL_PASS=your_app_password
```

## 🔐 MongoDB Setup

### Local MongoDB
1. Install MongoDB Community Edition
2. Start the MongoDB service:
   ```bash
   # Windows
   mongod
   
   # macOS
   brew services start mongodb-community
   
   # Linux
   sudo systemctl start mongod
   ```

### MongoDB Atlas (Cloud)
1. Create an account at https://www.mongodb.com/cloud/atlas
2. Create a cluster
3. Create a database user
4. Whitelist your IP address
5. Get your connection string and add it to `.env`

## 🌐 API Endpoints

### Authentication Routes (`/api/auth`)
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Contact Routes (`/api/form`)
- `POST /api/form/contact` - Submit contact form

### Posts Routes (`/api/posts`)
- `GET /api/posts` - Get all posts
- `POST /api/posts` - Create new post

### Chat Routes (`/api/chat`)
- `GET /api/chat/:room` - Get chat messages from a room
- `POST /api/chat` - Send message

## 🤝 Contributing

This project was developed by a team. To contribute:

1. Create a new branch for your feature
2. Make your changes
3. Test thoroughly
4. Push to your branch
5. Create a Pull Request

## 📝 License

This project is licensed under the ISC License.

## 👥 Team

This project was developed collaboratively as a team project. All team members contributed to different aspects including:
- Frontend development (React, UI/UX)
- Backend development (Express, MongoDB)
- Database design and management
- Feature implementation
- Testing and debugging

## 🎓 Learning Outcomes

Through this project, the team learned:
- Full-stack MERN development
- Real-time communication with Socket.io
- Authentication and authorization with JWT
- MongoDB database design and queries
- Responsive UI design with Tailwind CSS
- Git and GitHub collaboration

## 📞 Support

For questions or issues, please contact through the Contact form in the application or create an issue in the repository.

---

**Last Updated:** May 21, 2026

Developed with ❤️ by the Career Guidance Platform Team
