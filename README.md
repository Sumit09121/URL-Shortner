# 🔗 ZippyLinks – URL Shortener Web Application

ZippyLinks is a production-ready URL Shortener web application built using Next.js and MongoDB.  
It converts long URLs into short, easy-to-share links and tracks real-time click analytics.

The application is deployed on Vercel and designed with scalability, clean architecture, and future enhancements in mind.

---

## 🚀 Live Project

https://url-shortner-eight-xi.vercel.app

---

## ✨ Features

- Generate short URLs instantly
- Click counter for each shortened link
- Fast and secure redirection
- Separate landing page
- MongoDB-based persistent storage
- Deployed on Vercel
- Authentication-ready structure (future scope)

---

## 🛠️ Tech Stack

Frontend   : Next.js, React, HTML, CSS, JavaScript  
Backend    : Next.js API Routes (Serverless)  
Database   : MongoDB  
Deployment : Vercel  

---

## 🧠 System Design

### High-Level Architecture

User  
→ Frontend (Next.js)  
→ Backend (API Routes)  
→ MongoDB  
→ Backend  
→ Frontend  
→ Original URL  

---

### URL Shortening Flow

User enters long URL  
→ Generate unique short code  
→ Store mapping in MongoDB  
→ Return short URL  

---

### Redirection & Click Tracking Flow

Short URL accessed  
→ Fetch original URL from database  
→ Increment click counter  
→ Redirect to original URL  

---

## 🗄️ Database Schema (MongoDB)

```js
{
  _id: ObjectId,
  originalUrl: String,
  shortCode: String,
  clicks: Number,
  createdAt: Date
}
