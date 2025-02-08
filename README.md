# SkyRocket

## Description
Sky-Rocket is a RESTful flight booking backend with three microservices for secure user
authentication, flight management, and concurrency-controlled booking using Node.js, Express,
MySQL, and Sequelize ORM.

### API Gateway

- Responsible for user authentication and authorization, using JWT for
secure token-based authentication and Bcrypt for password encryption.
- Implemented role-based access control for three user types and integrated express-rate-limit
for enhanced security with effective rate limiting.

### Flights Service

- Responsible for handling CRUD operations on flights, airplanes, airport
and city models.
- Implemented sorting and filtering functionality for flights based on parameters such as price,
date, and travelers.

### Booking Service 

- Responsible for concurrent flight bookings and Payment Service for transaction
simulation, implementing locks and transactions for concurrency management.
- Implemented Node Cron for automatic deletion of old bookings 10 minutes after creation if
payment fails.
