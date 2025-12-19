# 🔗 ZippyLinks – URL Shortener Web Application

ZippyLinks is a production-ready URL Shortener web application built using Next.js and MongoDB.
It converts long URLs into short, easy-to-share links and tracks real-time click analytics.

The application is deployed on Vercel and designed with scalability, clean architecture,
and future enhancements in mind.

----------------------------------------------------------------

## 🚀 Live Project

https://url-shortner-eight-xi.vercel.app

----------------------------------------------------------------

## ✨ Features

- Generate short URLs instantly
- Click counter for each shortened link
- Fast and secure redirection
- Separate landing page
- MongoDB-based persistent storage
- Deployed on Vercel
- Authentication-ready structure (future scope)

----------------------------------------------------------------

## 🛠️ Tech Stack

Frontend   : Next.js, React, HTML, CSS, JavaScript  
Backend    : Next.js API Routes (Serverless)  
Database   : MongoDB  
Deployment : Vercel  

----------------------------------------------------------------

## 🧠 System Design

### High-Level Architecture

User  
↓  
Frontend (Next.js)  
↓  
Backend (API Routes)  
↓  
MongoDB  
↓  
Backend  
↓  
Frontend  
↓  
Original URL  

----------------------------------------------------------------

### URL Shortening Flow

User enters long URL  
↓  
Generate unique short code  
↓  
Store mapping in MongoDB  
↓  
Return short URL  

----------------------------------------------------------------

### Redirection & Click Tracking Flow

Short URL accessed  
↓  
Fetch original URL from database  
↓  
Increment click counter  
↓  
Redirect to original URL  

----------------------------------------------------------------

## 🗄️ Database Schema (MongoDB)

{
  _id: ObjectId,
  originalUrl: String,
  shortCode: String,
  clicks: Number,
  createdAt: Date
}

----------------------------------------------------------------

## 📁 Project Structure

ZippyLinks/
│
├── app/
│   │
│   └── page.js
│
├── app/api/
│   │
│   └── shorturl/
│       │
│       └── route.js
│
├── components/
│   │
│   └── UrlForm.js
│
├── lib/
│   │
│   └── mongodb.js
│
├── public/
│
├── styles/
│
├── .env.local
├── package.json
└── README.md

----------------------------------------------------------------

## ⚙️ Installation & Setup

Step 1: Clone Repository  
git clone https://github.com/your-username/zippylinks.git  
cd zippylinks  

Step 2: Install Dependencies  
npm install  

Step 3: Configure Environment Variables  

Create a .env.local file in the root directory:

MONGODB_URI=your_mongodb_connection_string  

Step 4: Run Development Server  
npm run dev  

Step 5: Open in Browser  
http://localhost:3000  

----------------------------------------------------------------

## 🔄 API Endpoint

POST /api/shorturl  

Request Body:

{
  "url": "https://example.com"
}

Response:

{
  "shortUrl": "https://url-shortner-eight-xi.vercel.app/abc123"
}

----------------------------------------------------------------

## 🔮 Future Enhancements

- User Authentication (Login / Signup)
- Custom short URLs
- URL expiry feature
- Analytics dashboard
- QR code generation
- Private URLs

----------------------------------------------------------------

## 👨‍💻 Author

Sumit Lakhera  
B.Tech – Information Technology  
Aspiring Full Stack Developer  

----------------------------------------------------------------

## ⭐ Support

If you find this project useful, give it a ⭐ on GitHub.
Contributions and suggestions are welcome.
