# Bus_Reservation_System
Developed a bus reservation system project by using C programming language, it is a command line application helps the user to login and book ticket for available bus for a smooth ride.
Step-by-Step Explanation of the code:

1. Initialization of Structures and Variables:
The code starts by defining three structures: `struct Bus` to store bus information, `struct Passenger` for passenger details, and `struct User` to store user login information.
It also includes necessary libraries and declares functions for displaying menus, user login, booking tickets, canceling tickets, and checking bus status.
Three arrays are initialized:
`struct User users[5]` stores user login credentials for five users.
`struct Bus buses[3]` stores information about three different buses.
`struct Passenger passengers[500]` is an array to store passenger details.
`numUsers`, `numBuses`, and `numPassengers` are variables to keep track of the number of users, buses, and passengers.
`loggedInUserId` is initially set to -1, indicating that no user is logged in.

2. Main Function and Program Loop:
The `main` function is the entry point of the program.
It initializes the user data, bus data, passenger data, and the `loggedInUserId` variable.
The program enters a `while (1)` loop, which serves as the main program loop and runs until the user chooses to exit.

3. Main Menu (displayMainMenu):
If no user is logged in (`loggedInUserId == -1`), the program displays the main menu with options to “Login” or “Exit.”

4. User Login (loginUser):
If the user selects “Login” (choosing option 1), the program prompts the user to enter their username and password.
The `loginUser` function is called, which checks if the provided username and password match any of the predefined users in the `users` array.
If a match is found, the `loggedInUserId` is set to the index of the logged-in user, and a welcome message is displayed.
If no match is found, a login failed message is shown, and the user can try again or choose to exit.

5. User Menu (displayUserMenu):
If a user is logged in (`loggedInUserId >= 0`), the program displays the user menu with options to “Book a Ticket,” “Cancel a Ticket,” “Check Bus Status,” or “Logout.”

6. Booking a Ticket (bookTicket):
If the user selects “Book a Ticket” (option 1 from the user menu), the program asks for the bus number they want to book a ticket for.
It then searches for the selected bus in the `buses` array and checks if there are available seats.
If there are available seats, the program prompts the user to enter their name and age. It assigns a seat number, records the passenger’s bus number, and updates the available seats.
A success message is displayed, and the number of passengers (`numPassengers`) is incremented.

7. Canceling a Ticket (cancelTicket):
If the user selects “Cancel a Ticket” (option 2 from the user menu), the program asks for the passenger’s name.
It then searches for the passenger in the `passengers` array, ensuring that the passenger is on the bus of the currently logged-in user. If found, the ticket is canceled, the available seats are increased, and the passenger entry is removed.
8. Checking Bus Status (checkBusStatus):

If the user selects “Check Bus Status” (option 3 from the user menu), the program displays information about the bus the user is currently booked on. This includes the bus number, source, destination, total seats, available seats, and fare.
9. Logging Out:

If the user selects “Logout” (option 4 from the user menu), they are logged out, and `loggedInUserId` is set back to -1.
10. Exiting the Program:

If the user selects “Exit” from the main menu (option 2), the program exits the `while (1)` loop and ends.
This code simulates a basic bus reservation system, allowing users to log in, book and cancel tickets, check bus status, and log out. Note that this code is a simplified example and lacks error handling and data persistence features commonly found in production systems.
