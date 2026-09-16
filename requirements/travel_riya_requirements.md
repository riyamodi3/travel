# BlazeDemo — Airline / Travel Booking Requirements

Base URL: https://blazedemo.com/
Source: public site content (home page, flight search results, purchase, and confirmation pages) captured 2026-09-16.

## Home Page — Flight Search

- The home page displays the heading "Welcome to the Simple Travel Agency!" and promotes a "destination of the week" offer.
- A Departure City dropdown offers: Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, São Paolo.
- A Destination City dropdown offers: Buenos Aires, Rome, London, Berlin, New York, Dublin, Cairo.
- A "Find Flights" button submits the selected departure and destination cities and navigates to the flight results (reserve) page.

## Flight Results Page

- The reserve page lists available flights in a table with columns: Airline, Flight #, Departure Time, Arrival Time, and Price.
- Each row has a "Choose This Flight" button that proceeds to the purchase page for that specific flight.
- The selected departure and destination cities from the home page are reflected in the page heading.

## Purchase Page

- The purchase page displays a summary table of the chosen flight: departure city, destination city, flight number, airline, and price.
- The purchase form collects: Name on Card, Address, City, State, Zip Code, Card Type (Visa or American Express), Credit Card Number, Credit Card Month, Credit Card Year.
- A "Remember me" checkbox is present on the purchase form.
- A "Purchase Flight" button submits the form and navigates to the purchase confirmation page.

## Purchase Confirmation Page

- The confirmation page displays the message "Thank you for your purchase today!"
- A unique numeric Order ID is generated and shown for each completed purchase.
- The confirmation page shows the total amount paid, matching the price of the chosen flight.
- The confirmation page displays a summary table of the purchaser's submitted information (name, address, city, state, zip) and the payment details entered (card type, card number, expiration).
- A "Home" link/button returns the user to the home page.

## Navigation

- The "home" link in the top navigation is available on every page and returns the user to the flight search home page.
