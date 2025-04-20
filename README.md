# Bus Ticket Booking System (Java CLI Application)

This is a simple command-line interface (CLI) application written in Java for booking and managing bus tickets. It allows users to view available bus types and names, book seats, cancel bookings, and access help and developer information.

## Features

* **Login:** Basic username and password authentication to access the system.
* **View Bus Ticket List:** Displays available bus categories (Business Class, AC, Non-AC) and the bus names within each category.
* **Book Bus Tickets:** Allows users to select a bus, enter their name, specify the number of seats, and make a simulated payment with OTP verification.
* **Cancel Booking:** Enables users to cancel their booking by entering the name used during booking. A refund amount is displayed (currently a fixed return of the total amount).
* **Help Line:** Provides a contact email and phone number for support.
* **Developer Information:** Shows the developer's name, ID, and academic background.
* **Basic Input Validation:** Limited input validation is present (e.g., OTP verification).

## How to Run

1.  **Prerequisites:** Ensure you have Java Development Kit (JDK) installed on your system.
2.  **Compilation:** Save all the `.java` files (`Bus_List.java`, `Cancel.java`, `Devloper.java`, `Login_info.java`, `Main.java`, `Payment.java`, `Seat_Book.java`) in the same directory. Open a terminal or command prompt in that directory and compile the Java files using the following command:
    ```bash
    javac *.java
    ```
3.  **Execution:** After successful compilation, run the `Main` class using:
    ```bash
    java Main
    ```
    This will start the application in your terminal.

## Usage

1.  **Login:** The application will first prompt you to enter a username and password. The default credentials are:
    * Username: `Junayed`
    * Password: `123`
    Enter these credentials to access the main menu.

2.  **Main Menu:** Once logged in, you will see the following options:
    ```
            1.View Bus Ticket List
            2.Book Bus Tickets
            3.Cancel Booking
            4.Exit
            5.Help Line
            6.Devloper Information
    ```
    Enter the number corresponding to the action you want to perform.

3.  **View Bus Ticket List (Option 1):**
    * Displays the available bus categories (1. business class, 2. AC, 3. non Ac).
    * Prompts you to choose a bus category.
    * Shows the list of bus names within the selected category.
    * Press `1` to return to the main menu.

4.  **Book Bus Tickets (Option 2):**
    * Prompts you to choose a bus category (1, 2, or 3).
    * Asks for your name.
    * Requests the number of seats you want to book.
    * Displays the cost per ticket (fixed at 150).
    * Shows the total amount.
    * Prompts for confirmation to proceed with payment (Press `1`).
    * Asks for an OTP (fixed at `1234`). Enter the correct OTP to complete the booking.
    * Displays "Booking Complete" upon successful OTP verification.
    * Press any key to return to the main menu.

5.  **Cancel Booking (Option 3):**
    * Prompts you to enter the name used during the booking.
    * If the entered name matches the last booked name, it displays a "Returned Money" message with the total amount and "Cancel Completed".
    * If the name is invalid, it shows "Invalid Name".
    * Press any key to return to the main menu.

6.  **Help Line (Option 5):**
    * Displays the help email (`help.public@gmail.com`) and phone number (`Number_ 888`).
    * Press `1` to return to the main menu.

7.  **Developer Information (Option 6):**
    * Shows the developer's name (`Mithun Kumar das`), ID (`213-35-796`), and educational background (`b.sc in SWE At Diu`).
    * Press `1` to return to the main menu.

8.  **Exit (Option 4):** Closes the application.

## Code Structure

The application is organized into the following Java classes:

* `Bus_List`: Manages the display of bus categories and names.
* `Cancel`: Handles the cancellation of booked tickets.
* `Devloper`: Provides developer and help information.
* `Login_info`: Stores the login username and password.
* `Main`: The entry point of the application, containing the main menu and login logic.
* `Payment`: Simulates the payment process and stores the OTP.
* `Seat_Book`: Extends `Bus_List` and handles the seat booking process, including payment and calling the `Cancel` class.

## Potential Improvements

This is a basic implementation and can be further enhanced with the following features:

* **Data Persistence:** Store bus details, booking information, and user credentials in a file or database instead of hardcoding them.
* **More Realistic Booking:** Allow users to select specific buses and seats.
* **Advanced Payment System:** Integrate with actual payment gateways.
* **Better Input Validation:** Implement more robust error handling for user input.
* **User Management:** Allow registration of new users and management of user accounts.
* **Date and Time:** Include functionality for selecting travel dates and times.
* **Error Handling:** Implement try-catch blocks to handle potential exceptions.
* **User Interface:** Consider developing a graphical user interface (GUI) for a more user-friendly experience.
