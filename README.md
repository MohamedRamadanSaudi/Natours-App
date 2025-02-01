# Natours Application

Welcome to the Natours application! This is a comprehensive tour booking platform built with modern web technologies. The application allows users to explore various tours, book them, leave reviews, and manage their accounts. It also provides administrative features for managing tours, users, and bookings.

## Features

- **User Authentication and Authorization**: Secure user authentication with JWT (JSON Web Tokens) and role-based access control.
- **Tour Management**: Create, read, update, and delete tours with detailed information such as duration, difficulty, price, and more.
- **Booking System**: Users can book tours and manage their bookings.
- **Reviews and Ratings**: Users can leave reviews and ratings for tours they have booked.
- **Email Notifications**: Send welcome emails and password reset emails using Nodemailer.
- **Payment Integration**: Secure payment processing using Stripe.
- **Advanced Filtering and Sorting**: Users can filter and sort tours based on various criteria.
- **Geospatial Queries**: Find tours within a certain distance from a given location.
- **Error Handling**: Comprehensive error handling with custom error messages and logging.
- **Security**: Implemented security best practices such as rate limiting, data sanitization, and secure headers.

## Technologies Used

- **Backend**: Node.js, Express.js
- **Database**: MongoDB (with Mongoose for schema modeling)
- **Authentication**: JSON Web Tokens (JWT)
- **Payment Processing**: Stripe
- **Email Notifications**: Nodemailer with Sendinblue (for production) and Mailtrap (for development)
- **Frontend**: Pug templates for server-side rendering
- **Security**: Helmet, express-rate-limit, express-mongo-sanitize, xss-clean, hpp
- **Other Libraries**: bcryptjs, sharp, multer, axios, and more

## Installation

To get started with the Natours application, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/MohamedRamadanSaudi/Natours-App.git
   cd natours-app
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Set up environment variables**:
   Create a `.env` file in the root directory and add the following variables:
   ```env
   NODE_ENV=development
   PORT=3000
   DATABASE=mongodb+srv://<username>:<password>@cluster0.xiwhcjy.mongodb.net/natours?retryWrites=true&w=majority
   DATABASE_PASSWORD=<your_database_password>
   JWT_SECRET=<your_jwt_secret>
   JWT_EXPIRES_IN=90d
   JWT_COOKIE_EXPIRES_IN=90
   EMAIL_USERNAME=<your_email_username>
   EMAIL_PASSWORD=<your_email_password>
   EMAIL_HOST=sandbox.smtp.mailtrap.io
   EMAIL_PORT=587
   EMAIL_FROM=<your_email_address>
   STRIPE_SECRET_KEY=<your_stripe_secret_key>
   ```

4. **Start the application**:
   ```bash
   npm start
   ```

5. **Access the application**:
   Open your browser and navigate to `http://localhost:3000`.

## API Endpoints

### Tours
- **GET /api/v1/tours**: Get all tours.
- **GET /api/v1/tours/:id**: Get a specific tour by ID.
- **POST /api/v1/tours**: Create a new tour (admin/lead-guide only).
- **PATCH /api/v1/tours/:id**: Update a tour (admin/lead-guide only).
- **DELETE /api/v1/tours/:id**: Delete a tour (admin/lead-guide only).

### Users
- **POST /api/v1/users/signup**: Sign up a new user.
- **POST /api/v1/users/login**: Log in a user.
- **GET /api/v1/users/logout**: Log out a user.
- **POST /api/v1/users/forgotPassword**: Request a password reset.
- **PATCH /api/v1/users/resetPassword/:token**: Reset a user's password.
- **PATCH /api/v1/users/updateMyPassword**: Update the current user's password.
- **GET /api/v1/users/me**: Get the current user's profile.
- **PATCH /api/v1/users/updateMe**: Update the current user's profile.
- **DELETE /api/v1/users/deleteMe**: Delete the current user's account.

### Reviews
- **GET /api/v1/reviews**: Get all reviews.
- **GET /api/v1/reviews/:id**: Get a specific review by ID.
- **POST /api/v1/reviews**: Create a new review (user only).
- **PATCH /api/v1/reviews/:id**: Update a review (user/admin only).
- **DELETE /api/v1/reviews/:id**: Delete a review (user/admin only).

### Bookings
- **GET /api/v1/bookings**: Get all bookings (admin/lead-guide only).
- **GET /api/v1/bookings/:id**: Get a specific booking by ID.
- **POST /api/v1/bookings**: Create a new booking (admin/lead-guide only).
- **PATCH /api/v1/bookings/:id**: Update a booking (admin/lead-guide only).
- **DELETE /api/v1/bookings/:id**: Delete a booking (admin/lead-guide only).

## Contributing

Contributions are welcome!

## Acknowledgments

- Special thanks to Jonas Schmedtmann for his excellent Node.js course, which inspired this project.
- Thanks to the open-source community for providing the libraries and tools used in this project.

## Contact

If you have any questions or feedback, feel free to reach out:

- **Mohamed Ramadan**
- Email: [MohamedRamadanSaudi@gmail.com](mailto:MohamedRamadanSaudi@gmail.com)
- GitHub: [Mohamed Ramadan](https://github.com/MohamedRamadanSaudi)
