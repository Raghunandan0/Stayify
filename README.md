# 🏡 Stayify Full-Stack Web Application  

[![MERN Stack](https://img.shields.io/badge/Stack-MERN-green)](#-tech-stack)  
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)  
[![Deployed on Render](https://img.shields.io/badge/Deployed-Render-purple)](https://your-render-url.com)  
[![Mapbox](https://img.shields.io/badge/Maps-Mapbox-blue)](#-map-integration)  



![GitHub stars](https://img.shields.io/github/stars/Raghunandan0/Stayify?style=social)
![GitHub forks](https://img.shields.io/github/forks/Raghunandan0/Stayify?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/Raghunandan0/Stayify?style=social)
![GitHub issues](https://img.shields.io/github/issues/Raghunandan0/Stayify)
![GitHub license](https://img.shields.io/github/license/Raghunandan0/Stayify)

A **full-stack Airbnb-like platform** built with the **MERN stack** using **MVC architecture**.  
It enables users to **browse, create, update, and delete property listings** with secure authentication, interactive maps, and **cloud-based media storage**.  

---

## 📑 Table of Contents
- [🚀 Features](#-features)
- [🛠 Tech Stack](#-tech-stack)
- [📷 Screenshots](#-screenshots)
- [⚙ Installation](#-installation--setup)
- [🌐 Deployment](#-deployment)
- [📜 License](#-license)

---

## 🚀 Features  

✅ **Secure Authentication & Authorization**  
- Implemented using **Passport.js** with session-based login.  
- Role-based access control for protected routes.  
- Real-time notifications via **Flash messages**.  

✅ **Map Integration**  
- Geocoding for property addresses.  
- Interactive map markers using **Mapbox API**.  

✅ **Listings Management**  
- Full **CRUD** for property listings.  
- Attributes: title, description, location, price, images.  
- Cloud uploads via **Multer** + **Cloudinary**.  

✅ **MVC Architecture**  
- Clear separation of concerns for scalability & maintainability.  

✅ **Deployment**  
- Hosted on **Render** with responsive, scalable performance.  

---

## 🛠 Tech Stack  

**Frontend:** EJS, HTML, CSS, JavaScript  
**Backend:** Node.js, Express.js  
**Database:** MongoDB, Mongoose  
**Authentication:** Passport.js (session-based)  
**Maps & Geocoding:** Mapbox API  
**File Uploads:** Multer  
**Image Hosting:** Cloudinary  
**Architecture:** MVC Pattern  

---

## 📷 Screenshots  

| Home Page | Property Listing | Map View |
|-----------|-----------------|----------|
| *(screenshot)* | *(screenshot)* | *(screenshot)* |

---

## ⚙ Installation & Setup  

```bash
# 1️⃣ Clone the repository
git clone https://github.com/your-username/airbnb-clone.git

# 2️⃣ Navigate into the folder
cd airbnb-clone

# 3️⃣ Install dependencies
npm install

# 4️⃣ Create a .env file with:
# CLOUDINARY_CLOUD_NAME=your_cloud_name
# CLOUDINARY_KEY=your_api_key
# CLOUDINARY_SECRET=your_api_secret
# MAPBOX_TOKEN=your_mapbox_token
# SESSION_SECRET=your_secret
# MONGO_URI=your_mongodb_connection_string

# 5️⃣ Start the app
npm start
```

## 🌐 Deployment

🚀 Live Demo: https://stayify-1.onrender.com

## 🗂 Project Architecture
flowchart LR
    subgraph Client[Client Side]
        UI[User Interface - EJS Templates] --> Browser
    end

    subgraph Server[Server Side - MVC]
        Controller[Controllers] --> Model[Models - MongoDB]
        UI -->|HTTP Request| Router[Express Router]
        Router --> Controller
        Controller --> View[Views - EJS]
        Controller --> Service[Services - Mapbox, Cloudinary]
    end

    subgraph External[External Services]
        Mapbox[Mapbox API - Geocoding & Maps]
        Cloudinary[Cloudinary - Image Storage]
    end

    Browser -->|CRUD Requests| Router
    Model <--> MongoDB[(MongoDB Database)]
    Service --> Mapbox
    Service --> Cloudinary

    Server -->|Deployed to| Render[Render Hosting]

 
