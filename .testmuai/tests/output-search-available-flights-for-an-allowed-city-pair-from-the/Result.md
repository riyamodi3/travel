---
test: ../search-available-flights-for-an-allowed-city-pair-from-the_test.md
status: failed
started: 2026-09-16T16:44:58.328Z
duration_s: 230
session_id: 5811894d-2a9c-4839-a1bf-0b32687a90a3
---

# Standard route search reaches results and carries the chosen flight into purchase — Result

## Step 1 ✓ passed (42.1s)
md5: 20017afc60dac1d5f50d62ece86c312e
Open https://blazedemo.com/ in the browser and review the flight-search form on the home page, then assert the Departure City dropdown offers exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo, and the Destination City dropdown offers exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 2 ✓ passed (46.8s)
md5: d1f6944b75870910dfddc4cf4f8fec18
On the BlazeDemo home page, set Departure City to Paris and Destination City to Cairo and submit Find Flights, then assert the browser reaches the flight results page.

## Step 3 ✓ passed (36.1s)
md5: 4bba9d3cbc479f7901a48b9ddd2c70ef
On the flight results page for Paris to Cairo, review the heading and the flights table, then assert the heading includes Paris and Cairo, the table shows Airline, Flight #, Departure Time, Arrival Time, and Price columns, and every displayed flight row includes a Choose This Flight action.

## Step 4 ✗ failed (90.1s)
md5: ba175b3bf8cebc8c6e02fe8d90d3cc87
Reason: Final verification failed: "the purchase page shows {{chosen_departure_city}}, {{chosen_destination_city}}, {{chosen_flight_number}}, {{chosen_airline}}, and {{chosen_price}} for the selected flight" — bug verdict: Selected Paris–Cairo flight opens unrelated reservation [application_issue/functional_defect, confidence 0.96]
On the Paris to Cairo results page, store the first listed flight row's departure city, destination city, flight number, airline, and price as chosen_departure_city, chosen_destination_city, chosen_flight_number, chosen_airline, and chosen_price, choose that row's Choose This Flight action, then assert the purchase page shows the same departure city, destination city, flight number, airline, and price for the selected flight.
