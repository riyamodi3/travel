---
assurance:
  id: t-1
  base: sha256:ebe1bff680edfb7f3eb461356f328abaddba25ffd2f5d3e562441a6bd105fa26
---
# Standard route search reaches results and carries the chosen flight into purchase

> Prove a site visitor can choose a standard valid departure city and destination city, reach the reserve page, review the required flight table structure, and continue to purchase from one listed flight.

## Step 1 @verifies ac-6, ac-7

Open https://blazedemo.com/ in the browser and review the flight-search form on the home page, then assert the Departure City dropdown offers exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo, and the Destination City dropdown offers exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 2 @verifies ac-2

On the BlazeDemo home page, set Departure City to Paris and Destination City to Cairo and submit Find Flights, then assert the browser reaches the flight results page.

## Step 3 @verifies ac-3, ac-4, ac-5

On the flight results page for Paris to Cairo, review the heading and the flights table, then assert the heading includes Paris and Cairo, the table shows Airline, Flight #, Departure Time, Arrival Time, and Price columns, and every displayed flight row includes a Choose This Flight action.

## Step 4 @verifies ac-1

On the Paris to Cairo results page, store the first listed flight row's departure city, destination city, flight number, airline, and price as chosen_departure_city, chosen_destination_city, chosen_flight_number, chosen_airline, and chosen_price, choose that row's Choose This Flight action, then assert the purchase page shows the same departure city, destination city, flight number, airline, and price for the selected flight.
