# AquaShield Server 

AquaShield Server is the backend service for the **AquaShield IoT platform**.  
It handles device data, user authentication, and communication between IoT devices and the mobile/web application.

##  Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB** 
- **JWT Authentication**
- **REST API**

##  Features

- User registration and login
- IoT device registration
- Receive sensor data (sunlight, wind, humidity, rain, etc.)
- Store and process IoT data
- Send device status to mobile application
- Secure APIs using JWT

##  Project Structure

```
server/
 app.js                  # Express application setup and middleware configuration
 server.js               # Server entry point - HTTP server initialization
 package.json            # Project dependencies and scripts
 README.md              # Project documentation
 src/                   # Source code directory
     config/            # Configuration files (database, environment variables)
     controllers/       # Request handlers and business logic
     middlewares/       # Custom middleware (authentication, error handling, etc.)
     models/            # MongoDB/Mongoose data models and schemas
     routes/            # API route definitions and endpoints
     services/          # Business logic and external service integrations
     utils/             # Utility functions and helper modules
```

### Directory Details

#### Root Files
- **app.js**: Configures the Express application, sets up middleware, and integrates routes
- **server.js**: Initializes and starts the HTTP server, connects to the database
- **package.json**: Manages dependencies (Express, Mongoose, JWT, CORS, dotenv, etc.)

#### src/ Directory

**config/**: Application configuration
- Database connection settings
- Environment variable management
- Application constants and settings

**controllers/**: Business logic handlers
- User authentication controller
- Device management controller
- Sensor data processing controller
- Request validation and response formatting

**middlewares/**: Custom Express middleware
- JWT authentication middleware
- Error handling middleware
- Request logging
- Input validation middleware

**models/**: MongoDB data models
- User model (authentication, profiles)
- Device model (IoT device registration)
- Sensor data model (sunlight, wind, humidity, rain)
- Data relationships and schemas

**routes/**: API endpoint definitions
- ```/api/auth``` - User registration and login
- ```/api/devices``` - Device management
- ```/api/data``` - Sensor data endpoints
- Route-to-controller mappings

**services/**: Business logic and integrations
- Data processing services
- IoT device communication logic
- Third-party API integrations
- Background job handlers

**utils/**: Helper functions
- Token generation and verification
- Data formatters and validators
- Common utility functions
- Logger utilities

##  Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- MongoDB instance
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/binojmadhuranga/AquaShield-server.git
cd server
```

2. Install dependencies:
```bash
npm install
```

3. Create a ```.env``` file in the root directory:
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/AquaShield
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
```

4. Start the server:
```bash
# Development mode with nodemon
npm run dev

# Production mode
npm start
```

##  API Endpoints

### Authentication
- ```POST /api/auth/register``` - Register a new user
- ```POST /api/auth/login``` - User login

### Devices
- ```GET /api/devices``` - Get all registered devices
- ```POST /api/devices``` - Register a new IoT device
- ```GET /api/devices/:id``` - Get device details
- ```PUT /api/devices/:id``` - Update device information
- ```DELETE /api/devices/:id``` - Remove a device

### Sensor Data
- ```POST /api/data``` - Receive sensor data from IoT devices
- ```GET /api/data/:deviceId``` - Get sensor data for a specific device
- ```GET /api/data``` - Get all sensor data with filters

##  Environment Variables

Create a ```.env``` file with the following variables:

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/AquaShield
JWT_SECRET=your_secure_secret_key
JWT_EXPIRE=7d
NODE_ENV=development
```

##  Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

##  License

ISC

##  Author

GitHub: [@binojmadhuranga](https://github.com/binojmadhuranga)
