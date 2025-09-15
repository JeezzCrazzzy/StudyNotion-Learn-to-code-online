# StudyNotion Edtech Project

## Project Overview

StudyNotion is a full-stack EdTech platform that enables users to browse, enroll in, and manage online courses. The platform supports user authentication, course creation, progress tracking, secure payments, and more. It is designed for both students and instructors, providing a seamless learning and teaching experience.

## Features

- User authentication (signup, login, email verification, password reset)
- Instructor and student dashboards
- Course creation, management, and enrollment
- Video lectures and course content management
- Progress tracking for students
- Secure payments integration (Razorpay)
- Contact form and email notifications
- Ratings and reviews for courses

## Technologies Used

### Frontend
- React.js (with functional components and hooks)
- Redux Toolkit (state management)
- Tailwind CSS (styling)
- React Router (routing)

### Backend
- Node.js
- Express.js
- MongoDB (with Mongoose ODM)
- Cloudinary (image/video uploads)
- Razorpay (payment gateway)
- Nodemailer (email notifications)

### Other Tools
- Prettier (code formatting)
- ESLint (linting)
- Netlify (frontend deployment)

## Project Structure

```
edtech/
├── package.json
├── prettier.config.js
├── README.md
├── tailwind.config.js
├── public/
│   ├── index.html
│   └── ...
├── server/
│   ├── index.js                # Express server entry point
│   ├── package.json
│   ├── config/                 # Configuration files (DB, Cloudinary, Razorpay)
│   ├── controllers/            # Route controllers (Auth, Course, Payments, etc.)
│   ├── mail/                   # Email templates
│   ├── middleware/             # Custom middleware (auth, etc.)
│   ├── models/                 # Mongoose models (User, Course, etc.)
│   ├── routes/                 # Express routes
│   └── utils/                  # Utility functions (image upload, mail sender, etc.)
├── src/
│   ├── App.jsx                 # Main React component
│   ├── index.js                # React entry point
│   ├── assets/                 # Images, videos, logos
│   ├── components/             # React components (Common, core, etc.)
│   ├── data/                   # Static data (country codes, links)
│   ├── hooks/                  # Custom React hooks
│   ├── pages/                  # Page components (Home, Login, Dashboard, etc.)
│   ├── reducer/                # Redux reducers
│   ├── services/               # API connectors and service functions
│   ├── slices/                 # Redux slices
│   └── utils/                  # Utility functions
```

## How to Run Locally

1. Clone the repository and install dependencies:
	```
	git clone <repo-url>
	cd edtech
	npm install
	cd server
	npm install
	```
2. Set up environment variables for the backend (see `server/config/`).
3. Start the backend server:
	```
	node index.js
	```
4. Start the frontend React app (in a separate terminal):
	```
	cd ..
	npm start
	```

## Deployment

### Frontend (Netlify)
1. Build the React app:
	```
	npm run build
	```
2. Deploy the `build/` folder to Netlify (drag-and-drop or connect to GitHub).

### Backend
Deploy the `server/` folder to a Node.js hosting service (e.g., Render, Railway, Heroku). Set environment variables and connect your database.

---
For more details, see the code comments and configuration files in each directory.
