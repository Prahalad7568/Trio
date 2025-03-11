# 🚖 Trio - Ride Sharing Application

## 📌 Overview

The Trio project is a comprehensive ride-hailing application built using a microservices architecture. It consists of three main services: **User Service**, **Captain Service**, and **Ride Service**, along with a **Gateway** that acts as a reverse proxy to route requests to the appropriate service. The frontend is developed using **React** and **Vite**, providing a responsive and interactive user experience.

## 🏗️ Architecture

### Microservices

1. **User Service**:
   - Manages user registration, login, and profile management.
   - Handles user authentication and authorization using JWT.
   - Interacts with a MongoDB database to store user data.

2. **Captain Service**:
   - Manages captain registration, login, and profile management.
   - Handles ride requests and availability status.
   - Uses JWT for authentication and maintains a blacklist of tokens for security.

3. **Ride Service**:
   - Manages ride creation, acceptance, and completion.
   - Calculates fares based on pickup and destination.
   - Uses RabbitMQ for real-time communication between services, allowing captains to receive ride requests.

4. **Gateway**:
   - Acts as a single entry point for all client requests.
   - Routes requests to the appropriate microservice based on the URL path.
   - Provides a layer of security and load balancing.

### Frontend

- Built using **React** and **Vite**, the frontend provides a seamless user experience with features such as:
  - User and captain registration and login forms.
  - Real-time ride tracking and notifications.
  - Interactive maps for pickup and destination selection.
  - Responsive design for mobile and desktop users.

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
 
  
