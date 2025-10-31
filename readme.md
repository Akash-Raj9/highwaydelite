🌄 HighwayDelite

HighwayDelite is a full-stack adventure experience booking web application.
It allows users to explore curated highway experiences (like kayaking, coffee trails, bungee jumping, and more), view detailed descriptions, and complete bookings through a smooth checkout process.

🧭 Table of Contents

Overview

Features

Tech Stack

Project Structure

Installation & Setup

1. Clone the Repository

2. Backend Setup

3. Frontend Setup

Environment Variables

Running the App

API Endpoints

Available Scripts

Screenshots (Optional)

License

🏝️ Overview

HighwayDelite provides a seamless interface for discovering, viewing, and booking real-world experiences.
Users can:

Browse curated adventure listings.

View details such as price, duration, and description.

Add bookings and review them at checkout.

Confirm and complete bookings through an intuitive flow.

⚙️ Features
Frontend

Built using React + TypeScript + Vite for lightning-fast performance.

Organized and modular UI components (Header, ExperienceCard, OrderSummary).

Dynamic pages:

/ → Home

/experience/:id → Experience details

/checkout → Booking & summary

/confirmation → Final booking confirmation.

Fully responsive, image-rich design.

Axios client for API communication.

Backend

Built using Node.js + Express + MongoDB (Mongoose).

RESTful API for experiences, promotions, and bookings.

MongoDB seeding support (seed.js) to populate demo data.

Middleware-based error handling.

CORS-enabled for cross-origin requests from frontend.

💻 Tech Stack

Frontend:

React (Vite + TypeScript)

Axios

Tailwind / CSS modules

React Router DOM

Backend:

Node.js

Express.js

MongoDB + Mongoose

dotenv

CORS

🗂 Project Structure
highwaydelite/
├── backend/
│   ├── models/
│   │   ├── Booking.js
│   │   ├── Experience.js
│   │   └── Promo.js
│   ├── routes/
│   │   ├── bookings.js
│   │   ├── experiences.js
│   │   └── promo.js
│   ├── middleware/
│   │   └── errorHandler.js
│   ├── seed.js
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── public/
│   │   ├── *.png (experience images)
│   ├── src/
│   │   ├── api/axiosClient.ts
│   │   ├── components/
│   │   │   ├── ExperienceCard.tsx
│   │   │   ├── Header.tsx
│   │   │   └── OrderSummary.tsx
│   │   ├── pages/
│   │   │   ├── Home.tsx
│   │   │   ├── ExperienceDetails.tsx
│   │   │   ├── Checkout.tsx
│   │   │   └── Confirmation.tsx
│   │   ├── App.tsx
│   │   ├── main.tsx
│   │   └── types/
│   └── package.json
│
├── .gitignore
└── README.md

⚙️ Installation & Setup
🪞 1. Clone the Repository
git clone https://github.com/Akash-Raj9/highwaydelite.git
cd highwaydelite

🧩 2. Backend Setup

Navigate to the backend folder:

cd backend


Install dependencies:

npm install


Create a .env file in the backend directory:

PORT=5000
MONGO_URI=your_mongodb_connection_string

To seed the database with demo experiences:

node seed.js


Run the backend server:

npm start
# or for auto-reload in dev mode:
npx nodemon server.js


The backend will start at
👉 http://localhost:5000

💠 3. Frontend Setup

Navigate to the frontend folder:

cd ../frontend


Install dependencies:

npm install


Create a .env file in frontend directory (optional):

VITE_API_BASE_URL=http://localhost:5000


Run the development server:

npm run dev


Frontend will be available at
👉 http://localhost:5173

🔐 Environment Variables
Variable	Location	Description
PORT	backend	Port for backend server
MONGO_URI	backend	MongoDB connection string
VITE_API_BASE_URL	frontend	Backend base URL for API requests
🚀 Running the App

Run both servers concurrently:

Terminal 1:

cd backend
npm start


Terminal 2:

cd frontend
npm run dev


Then open:
👉 Frontend: http://localhost:5173
👉 Backend API: http://localhost:5000/api

📡 API Endpoints
Experiences
Method	Endpoint	Description
GET	/api/experiences	Fetch all experiences
GET	/api/experiences/:id	Get experience by ID
Bookings
Method	Endpoint	Description
GET	/api/bookings	Get all bookings
POST	/api/bookings	Create a new booking
PUT	/api/bookings/:id	Update a booking
DELETE	/api/bookings/:id	Delete a booking
Promos
Method	Endpoint	Description
GET	/api/promo	Get all promotions
POST	/api/promo	Add new promo
DELETE	/api/promo/:id	Delete promo
🧠 Available Scripts
Frontend
Command	Description
npm run dev	Start Vite dev server
npm run build	Build for production
npm run preview	Preview built app
Backend
Command	Description
npm start	Start server
node seed.js	Seed the database
npx nodemon server.js	Auto-reload in dev mode

	
	
📜 License

This project is licensed under the MIT License.
Feel free to use, modify, and distribute it for educational or personal purposes.

👨‍💻 Author

Akash Raj
