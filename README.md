
# Hotel Management System

## Frameworks and Language Used


- Database: MongoDB
- Language: Java

## Data Flow

### Controller
The controller layer of our application is responsible for handling incoming HTTP requests, processing them, and sending appropriate responses. It utilizes the following functions:

- `createReservation`: Handles the creation of new hotel reservations.
- `getReservation`: Retrieves information about a specific reservation.
- `updateReservation`: Allows for updating reservation details.
- `deleteReservation`: Deletes a reservation from the system.
- `getAllReservations`: Fetches a list of all reservations.

### Services
The services layer acts as an intermediary between the controller and the repository. It encapsulates the business logic and performs data validation. It includes the following functions:

- `validateReservationData`: Validates the reservation data before saving it.
- `calculateReservationTotal`: Computes the total cost of a reservation.
- `sendConfirmationEmail`: Sends a confirmation email to the guest after a successful reservation.

### Repository
The repository layer handles database operations and interactions with our MongoDB database. It provides the following functions:

- `createReservation`: Saves reservation data to the database.
- `findReservationById`: Retrieves a reservation by its unique ID.
- `updateReservationData`: Updates reservation details in the database.
- `deleteReservationById`: Deletes a reservation from the database.
- `findAllReservations`: Retrieves all reservations from the database.

## Database Design

We use MongoDB as our database, and the data is organized into two main collections:

1. `hotels`: Contains information about various hotels, including their name, location, and room types.
2. `reservations`: Stores reservation details, such as guest information, check-in and check-out dates, and total cost.


## Project Summary

This hotel management system utilizes a MongoDB database to store hotel and reservation data. The system provides a set of APIs for creating, managing, and querying hotel reservations. The application ensures data integrity through a multi-layer architecture that separates concerns between the controller, services, and repository. It also incorporates email notifications to confirm reservations. Overall, the project aims to streamline hotel management and enhance the guest experience.
