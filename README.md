# Hotel Reservation System

## Overview

The **Hotel Reservation System** is a Java-based application designed to manage hotel room reservations. This system connects to a MySQL database, allowing users to reserve rooms, view reservations, update reservations, and delete reservations. It provides an easy-to-use command-line interface for hotel management.

## Features

- **Reserve a Room:** Allows users to reserve a room by entering the guest's name, room number, and contact number.
- **View Reservations:** Displays all current reservations, including reservation ID, guest name, room number, contact number, and reservation date.
- **Get Room Number:** Retrieves the room number based on the reservation ID and guest name.
- **Update Reservations:** Allows users to update an existing reservation's guest name, room number, and contact number.
- **Delete Reservations:** Deletes a reservation based on the reservation ID.
- **Exit System:** Exits the application safely with a countdown message.

## Database Structure

The system uses a MySQL database named `hotel_db` with a table `reservations`. The structure of the `reservations` table is as follows:

| Field            | Type         | Null | Key | Default           | Extra             |
|------------------|--------------|------|-----|-------------------|-------------------|
| reservation_id   | int          | NO   | PRI | NULL              | auto_increment    |
| guest_name       | varchar(255) | NO   |     | NULL              |                   |
| room_number      | int          | NO   |     | NULL              |                   |
| contact_number   | varchar(10)  | NO   |     | NULL              |                   |
| reservation_date | timestamp    | YES  |     | CURRENT_TIMESTAMP | DEFAULT_GENERATED |

## Prerequisites

- Java Development Kit (JDK) 8 or higher
- MySQL database
- MySQL Connector/J (JDBC Driver)

## Installation and Setup

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Jameel-25/HotelReservationSystem.git
   cd HotelReservationSystem
   ```

2. **Set Up the MySQL Database:**

   - Create a MySQL database named `hotel_db`.
   - Create the `reservations` table using the following SQL command:

     ```sql
     CREATE TABLE reservations (
         reservation_id INT NOT NULL AUTO_INCREMENT,
         guest_name VARCHAR(255) NOT NULL,
         room_number INT NOT NULL,
         contact_number VARCHAR(10) NOT NULL,
         reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
         PRIMARY KEY (reservation_id)
     );
     ```

3. **Configure Database Credentials:**

   - Update the `url`, `username`, and `password` variables in the `HotelReservationSystem` class with your MySQL database credentials.

4. **Compile and Run the Application:**

   - Compile the Java code:
     ```bash
     javac -d . src/hotelReservation/HotelReservationSystem.java
     ```
   - Run the application:
     ```bash
     java hotelReservation.HotelReservationSystem
     ```

## Usage

1. Run the application, and you'll be greeted with a menu where you can choose to reserve a room, view reservations, get room numbers, update reservations, delete reservations, or exit the system.
2. Follow the prompts to perform various actions.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

## Contact

For any queries or issues, please reach out to [mohammed.jameel.cs@gmail.com](mailto:mohammed.jameel.cs@gmail.com).
