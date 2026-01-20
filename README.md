# SkySense Server 🌤️

SkySense Server is the backend service for the **SkySense IoT platform**.  
It handles device data, user authentication, and communication between IoT devices and the mobile/web application.

## 🚀 Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB / MySQL** (choose based on your setup)
- **JWT Authentication**
- **REST API**

## 📌 Features

- User registration and login
- IoT device registration
- Receive sensor data (sunlight, wind, humidity, rain, etc.)
- Store and process IoT data
- Send device status to mobile application
- Secure APIs using JWT

## 📁 Project Structure

skysense-server/
├── src/
│ ├── controllers/
│ ├── routes/
│ ├── models/
│ ├── middleware/
│ └── app.js
├── .env
├── package.json
└── server.js