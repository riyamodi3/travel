---
assurance:
  id: t-21
  base: sha256:b2073feae64af147e701ff16e816c1a39e1daae950c7bffb738aefce0b4c734b
---
# Paris to New York search shows exact route text and reaches the fixed purchase details

> Prove a route search still works when the destination value is multi-word by searching from Paris to New York and continuing from the results table into purchase.

## Step 1

Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 @verifies ac-6

On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 @verifies ac-7

On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 @verifies ac-105, ac-107, ac-118

On the BlazeDemo home page, select Paris as the departure city and New York as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from Paris to New York:".

## Step 5 @verifies ac-106, ac-108, ac-119

On the results page for the Paris to New York search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: Paris", "Arrives: New York", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 @verifies ac-109, ac-110, ac-111, ac-112, ac-113

On the results page for the Paris to New York search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
