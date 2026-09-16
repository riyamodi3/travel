---
test: ../multi-word-destination-search-reaches-results-and-carries_test.md
status: failed
started: 2026-09-16T16:49:32.169Z
duration_s: 298
session_id: b6930756-6871-4617-b34a-1d7dc28d4a41
---

# Multi-word destination search reaches results and carries the chosen flight into purchase — Result

## Step 1 ✓ passed (58s)
md5: 20017afc60dac1d5f50d62ece86c312e
Open https://blazedemo.com/ in the browser and review the flight-search form on the home page, then assert the Departure City dropdown offers exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo, and the Destination City dropdown offers exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 2 ✓ passed (68.1s)
md5: 80de3f7f9a44633997f9308cb143ac4f
On the BlazeDemo home page, set Departure City to Paris and Destination City to New York and submit Find Flights, then assert the browser reaches the flight results page.

## Step 3 ✓ passed (43.4s)
md5: ea374a8626d0f62ac7de0acca7a6511e
On the flight results page for Paris to New York, review the heading and the flights table, then assert the heading includes Paris and New York, the table shows Airline, Flight #, Departure Time, Arrival Time, and Price columns, and every displayed flight row includes a Choose This Flight action.

## Step 4 ✗ failed (122.5s)
md5: c71481d2bf31141d1a64f539296f3fdf
Reason: Final verification failed: "The purchase page shows {{chosen_departure_city}}, {{chosen_destination_city}}, {{chosen_flight_number}}, {{chosen_airline}}, and {{chosen_price}} for the selected flight." — bug verdict: Selected Paris–New York flight opens an unrelated reservation [application_issue/functional_defect, confidence 0.98]
On the Paris to New York results page, store the first listed flight row's departure city, destination city, flight number, airline, and price as chosen_departure_city, chosen_destination_city, chosen_flight_number, chosen_airline, and chosen_price, choose that row's Choose This Flight action, then assert the purchase page shows the same departure city, destination city, flight number, airline, and price for the selected flight.
