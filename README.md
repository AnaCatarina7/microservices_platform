# FitLife

FitLife is a fitness platform designed to help users manage their workouts, nutrition, and class participation in one place. It is built around five microservices, each responsible for a specific part of the system.

## Features

- **User Profiles:** Manage accounts, body metrics, and fitness goals.
- **Workouts:** Manage exercises, create workout plans, and track completed workouts.
- **Nutrition:** Manage foods, meals, and meal plans based on user goals.
- **Class Bookings:** View available classes, make or cancel bookings, and manage instructors and class capacity.
- **Notifications:** Send updates about bookings, cancellations, and other relevant activity.

## Microservices

- **Users Service:** Handles user profiles, authentication, and access control.
- **Workouts Service:** Manages exercises, workout plans, workout history, and calories burned.
- **Nutrition Service:** Manages nutritional data, meals, and meal plans.
- **Sessions Service:** Manages classes, schedules, bookings, and instructors.
- **Notifications Service:** Handles user notifications, including booking-related updates.

## Architecture

An **API Gateway** provides a central entry point to the services and routes requests to the appropriate microservice. Services communicate synchronously through REST or GraphQL and asynchronously through RabbitMQ, which is used for booking-related notifications.

The project follows a **database-per-service** approach. The Users and Sessions services use MySQL, while the Workouts and Nutrition services use MongoDB. Protected endpoints use JWT authentication, with role-based restrictions for certain operations.

## Technology Stack

- **Architecture:** Microservices, API Gateway
- **APIs:** REST, GraphQL
- **Databases:** MySQL, MongoDB
- **Messaging:** RabbitMQ
- **Authentication:** JWT
- **Containers:** Docker
- **API Documentation:** Swagger

## API Documentation

The microservice APIs are documented with Swagger, including their endpoints, request parameters, responses, and authentication requirements.
