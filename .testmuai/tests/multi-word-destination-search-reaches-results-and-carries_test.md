---
assurance:
  id: t-4
  base: sha256:545375501c7ab9d1a2212096b659eae2d3e9b01e399ae9a128d604b517c73f49
---
# Multi-word destination search reaches results and carries the chosen flight into purchase

> Prove a route search still works when the destination value is multi-word by searching from Paris to New York and continuing from the results table into purchase.

## Step 1 @verifies ac-6, ac-7

Open https://blazedemo.com/ in the browser and review the flight-search form on the home page, then assert the Departure City dropdown offers exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo, and the Destination City dropdown offers exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 2 @verifies ac-2

On the BlazeDemo home page, set Departure City to Paris and Destination City to New York and submit Find Flights, then assert the browser reaches the flight results page.

## Step 3 @verifies ac-3, ac-4, ac-5

On the flight results page for Paris to New York, review the heading and the flights table, then assert the heading includes Paris and New York, the table shows Airline, Flight #, Departure Time, Arrival Time, and Price columns, and every displayed flight row includes a Choose This Flight action.

## Step 4 @verifies ac-1

On the Paris to New York results page, store the first listed flight row's departure city, destination city, flight number, airline, and price as chosen_departure_city, chosen_destination_city, chosen_flight_number, chosen_airline, and chosen_price, choose that row's Choose This Flight action, then assert the purchase page shows the same departure city, destination city, flight number, airline, and price for the selected flight.
