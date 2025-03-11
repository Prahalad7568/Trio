# 🚖 Trio - Ride Sharing Application

## 📌 Overview
Trio is a ride-hailing platform that connects passengers with drivers, enabling seamless ride bookings, real-time tracking, and secure transactions. The system is designed with a monolithic architecture, ensuring simplicity, centralized control, and easy deployment.

## 🚀 Features

### User Features
- **User Registration**: Users can create an account by providing their name, email, and password.
- **User Login**: Users can log in to their accounts using their email and password.
- **Profile Management**: Users can view and update their profile information.
- **Ride Booking**: Users can book rides by selecting pickup and destination locations.

### Captain Features
- **Captain Registration**: Captains can register by providing their details, including vehicle information.
- **Ride Acceptance**: Captains can accept ride requests in real-time.
- **Availability Toggle**: Captains can toggle their availability status to accept or decline rides.

### Ride Management
- **Ride Creation**: Users can create rides, which are then broadcasted to available captains.
- **Real-time Notifications**: Captains receive notifications for new ride requests via WebSocket.
- **Fare Calculation**: The system calculates fares based on the distance between pickup and destination.

## 🛠️  Technologies Used

- **Backend**:
  - Node.js with Express for building RESTful APIs.
  - MongoDB for data storage.
  - RabbitMQ for message brokering between services.
  - JWT for authentication and authorization.
  - Express Validator for input validation.

- **Frontend**:
  - React for building user interfaces.
  - Vite for fast development and build processes.
  - Tailwind CSS for styling and responsive design.
  - Axios for making HTTP requests to the backend.
 
 ## Instructions to Run the Trio Project

## Running the Backend

1. **Navigate to the Backend Directory**:
   ```bash
   cd /Users/nikhilsingh/Downloads/Trio/trio-Backend
   ```

2. **Install Dependencies**:
   Run the following command to install the required packages:
   ```bash
   npm install
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the `trio-Backend` directory and add the following variables:
   ```plaintext
   DB_CONNECT=<your_mongodb_connection_string>
   JWT_SECRET=<your_jwt_secret>
   GOOGLE_MAPS_API=<your_google_maps_api_key>
   PORT=3000
   ```

   Replace `<your_mongodb_connection_string>`, `<your_jwt_secret>`, and `<your_google_maps_api_key>` with your actual values.

4. **Start the Server**:
   Run the following command to start the backend server:
   ```bash
   node server.js
   ```

   The server should now be running on `http://localhost:3000`.

## Running the Frontend

1. **Navigate to the Frontend Directory**:
   ```bash
   cd /Users/nikhilsingh/Downloads/Trio/trio-frontend
   ```

2. **Install Dependencies**:
   Run the following command to install the required packages:
   ```bash
   npm install
   ```

3. **Start the Development Server**:
   Run the following command to start the frontend development server:
   ```bash
   npm run dev
   ```

   The frontend should now be running on `http://localhost:5173` (or another port if specified).

## Accessing the Application

- Open your web browser and navigate to `http://localhost:5173` to access the frontend of the Trio application.
- The backend API will be accessible at `http://localhost:3000`.
