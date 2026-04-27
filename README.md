# UBER Clone Project

## Description

This is a full-stack ride-sharing application inspired by Uber, built with modern web technologies. The project consists of a backend API server and a frontend user interface that allows users to book rides and captains to accept and manage rides.

## Features

### User Features
- User registration and login
- Ride booking with location search
- Real-time ride tracking
- Payment integration (placeholder)
- Ride history

### Captain Features
- Captain registration and login
- Accept ride requests
- Real-time location updates
- Ride management (start, finish)
- Earnings tracking

### General Features
- Real-time communication using WebSockets
- Map integration for location services
- Authentication and authorization
- Secure token-based sessions

## Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Socket.io** - Real-time communication
- **JWT** - Authentication
- **bcrypt** - Password hashing

### Frontend
- **React** - UI library
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **Context API** - State management
- **Socket.io-client** - Real-time communication

## Installation

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Backend Setup
1. Navigate to the backend directory:
   ```
   cd uber-video/Backend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a `.env` file in the Backend directory with the following variables:
   ```
   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/uber
   JWT_SECRET=your_jwt_secret
   MAPS_API_KEY=your_maps_api_key
   ```

4. Start the backend server:
   ```
   npm start
   ```

### Frontend Setup
1. Navigate to the frontend directory:
   ```
   cd uber-video/frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the development server:
   ```
   npm run dev
   ```

## Usage

1. Start the backend server (as described above).
2. Start the frontend development server.
3. Open your browser and navigate to `http://localhost:5173` (default Vite port).
4. Register as a user or captain.
5. Book rides or accept ride requests.

## API Endpoints

### User Routes
- `POST /users/register` - Register a new user
- `POST /users/login` - Login user
- `GET /users/profile` - Get user profile
- `POST /users/logout` - Logout user

### Captain Routes
- `POST /captains/register` - Register a new captain
- `POST /captains/login` - Login captain
- `GET /captains/profile` - Get captain profile
- `POST /captains/logout` - Logout captain

### Ride Routes
- `POST /rides/create` - Create a new ride
- `GET /rides/:id` - Get ride details
- `PUT /rides/:id/accept` - Accept a ride (captain)
- `PUT /rides/:id/start` - Start a ride
- `PUT /rides/:id/end` - End a ride

### Maps Routes
- `GET /maps/get-coordinates` - Get coordinates for an address
- `GET /maps/get-distance-time` - Get distance and time between locations
- `GET /maps/get-suggestions` - Get location suggestions

## Project Structure

```
uber-video/
├── Backend/
│   ├── controllers/     # Route handlers
│   ├── db/             # Database connection
│   ├── middlewares/    # Authentication middleware
│   ├── models/         # MongoDB schemas
│   ├── routes/         # API routes
│   ├── services/       # Business logic
│   ├── app.js          # Express app setup
│   ├── server.js       # Server startup
│   └── socket.js       # WebSocket handling
├── frontend/
│   ├── public/         # Static assets
│   ├── src/
│   │   ├── components/ # React components
│   │   ├── context/    # React context providers
│   │   ├── pages/      # Page components
│   │   ├── App.jsx     # Main app component
│   │   └── main.jsx    # App entry point
│   └── vite.config.js  # Vite configuration
└── README.md
```

## Screenshots

### Landing Page
![Landing Page](screenshots/landing-page.png)

### Login Page
![Login Page](screenshots/login-page.png)

### Home / Map View
![Home Page](screenshots/home-page.png)

### Ride Search Form
![Ride Search](screenshots/ride-search.png)

### Vehicle Selection
![Vehicle Selection](screenshots/vehicle-selection.png)

> Add the above images to the `screenshots/` folder in the repo to display them in the README.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by Uber's ride-sharing platform
- Built for educational purposes
- Uses open-source libraries and frameworks