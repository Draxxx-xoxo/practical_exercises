# Task 1: Movie Ticket Booking System

You are tasked to create a Ticket Booking System for a movie theatre that requires users to book tickets to watch their movies. The booking system uses classes such as 'Movie' and 'Booking' to store details on the movies and booking slots. It ensures that there are no over booking of movies and that all customers have a good time.
---

## Task 1.1

Create a class called 'Movie' containing the following attributes:
- 'Title': A string representing the name of the movie.
- 'Duration': An integer representing the duration of the movie in minutes.
- 'Rating': A float representing the rating of a movie. It should not exceed 10
- 'Screening_timings': a list of strings representing available screening times in the format '1:00 PM'.
- 'Max_seats': An integer representing the maximum number of seats available per screening. This should default to 50 unless stated otherwise.
- 'Price': A float representing the price of a ticket. The base price for a ticket is $10

Do *not* write any methods for the class yet

There can be many kinds of movies such as IMAX movies or 3D Movies. However, IMAX tickets are $15 and also have a smaller maximum seat capacity of 30 compared to the normal 50

Create a subclass called 'IMAX' that follows the requirements above.

Test your program by creating these two movies:
- 'Venom' is a IMAX movie, has a rating of 6.6, a duration of 112 minutes and screens at 3 hour intervals from 11:00 AM to 11:00 PM
- 'The Dark Knight' has a rating of 9.0, duration of 152 minutes and screens at 4 hour intervals from 8:00 AM to 8:00 PMM

---

## Task 1.2

Create a new attribute 'Seats_available': A dictionary containing number of available seats for each screening
Write program code for the methods:
- reduce_seating(time, number_of_seats): Reduces number of seats available for a given screening if enough seats are available. Otherwise, return an appropriate output.
- display_info(): displays movie title, duration, rating, screening times and their respective available seats

Test your code by reducing number of seats of 'The Dark Knight' by 3 for the 8:00 AM slot and printing the number of seats remaining.

---

## Task 1.3

Create a new class 'Booking' that stores the user's name, movie title and number of seats purchased
The class should include the methods:
- 'confirm_booking()': Returns 'True' if booking is valid and removes seats purchased from seats available. Otherwise, return False. Prints appropriate messages for success or failure
- 'cal_price()': Calculates the total price of the seats purchased. 
Number of bookings should not be negative or exceed the number of available seats for each given screening time.

Test your program using 4 appropriate test cases for 'confirm_booking()'

---

## Task 1.4

Write a function called 'movie_booking_system()'. When called, it:
- displays the information for 'Venom' and 'The Dark Knight'.
- promts user for a name, title, screening time and number of seats requested.
- converts this information into a 'Booking'.
- updates movie information.
- provides a confirmation on whether your booking was successful or not.
