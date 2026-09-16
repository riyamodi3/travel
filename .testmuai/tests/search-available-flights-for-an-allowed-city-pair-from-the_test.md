---
assurance:
  id: t-1
  base: sha256:f3054792cd373d44c2ae94423536a9633e3049c6ae52f75b220bd2efa6564a1e
---
# Search available flights for an allowed city pair from the home page

> Prove that the traveler can view the exact allowed departure and destination city choices, submit one allowed route, reach the reserve page, and see the selected route reflected with the required results columns.

## Step 1

Open https://blazedemo.com/ in the browser and remain on the flight-search home page.

## Step 2 @verifies ac-4

On https://blazedemo.com/, inspect the Departure City dropdown in the flight-search form, then assert its options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 @verifies ac-5

On https://blazedemo.com/, inspect the Destination City dropdown in the flight-search form, then assert its options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 @verifies ac-1, ac-2, ac-3

On https://blazedemo.com/, in the flight-search form, choose Paris as the Departure City and Buenos Aires as the Destination City, activate Find Flights, then assert the browser reaches the flight results reserve page, the page heading reflects Paris and Buenos Aires, and the results table shows the column headers Airline, Flight #, Departure Time, Arrival Time, and Price.
