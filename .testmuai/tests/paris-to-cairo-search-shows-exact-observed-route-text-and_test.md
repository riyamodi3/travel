---
assurance:
  id: t-22
  base: sha256:88564b88ece510324a4658942a2dcd20c675a8c46c780dc2dff4afeb306c1b36
---
# Paris to Cairo search shows exact observed route text and reaches the fixed purchase details

> Prove a site visitor can choose a standard valid departure city and destination city, reach the reserve page, review the required flight table structure, and continue to purchase from one listed flight.

## Step 1

Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 @verifies ac-6

On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 @verifies ac-7

On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 @verifies ac-105, ac-107, ac-120

On the BlazeDemo home page, select Paris as the departure city and Cairo as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from Paris to Cairo:".

## Step 5 @verifies ac-106, ac-108, ac-121

On the results page for the Paris to Cairo search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: Paris", "Arrives: Cairo", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 @verifies ac-109, ac-110, ac-111, ac-112, ac-113

On the results page for the Paris to Cairo search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
