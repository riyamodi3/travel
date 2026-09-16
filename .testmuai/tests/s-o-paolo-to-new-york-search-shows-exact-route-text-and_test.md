---
assurance:
  id: t-19
  base: sha256:64aa93dc9c67d5ebff86096a2971f2d479eee42cc5fa4bf278ee41e9506f46c8
---
# São Paolo to New York search shows exact route text and reaches the fixed purchase details

> Prove the search flow preserves special-character and multi-word city values by searching from São Paolo to New York, showing that route in the results heading, and continuing to purchase from a listed flight.

## Step 1

Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 @verifies ac-6

On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 @verifies ac-7

On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 @verifies ac-105, ac-107, ac-114

On the BlazeDemo home page, select São Paolo as the departure city and New York as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from São Paolo to New York:".

## Step 5 @verifies ac-106, ac-108, ac-115

On the results page for the São Paolo to New York search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: São Paolo", "Arrives: New York", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 @verifies ac-109, ac-110, ac-111, ac-112, ac-113

On the results page for the São Paolo to New York search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
