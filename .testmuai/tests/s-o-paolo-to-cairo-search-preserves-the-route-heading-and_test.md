---
assurance:
  id: t-16
  base: sha256:b317542a4fe008fe4bb95364298886f80241a485220a9d82d5f866efc561fa17
---
# São Paolo to Cairo search preserves the route heading and lands on the fixed purchase details

> Prove a route search still works when the departure value contains a special character by searching from São Paolo to Cairo and continuing through the listed results into purchase.

## Step 1

Open https://blazedemo.com/ in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 @verifies ac-6

On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 @verifies ac-7

On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 @verifies ac-96, ac-97, ac-98, ac-102

On the BlazeDemo home page, select São Paolo as the departure city and Cairo as the destination city, submit the search with Find Flights, then assert the browser reaches the reserve page and the page heading includes both "São Paolo" and "Cairo".

## Step 5 @verifies ac-99, ac-100

On the reserve page for the São Paolo to Cairo search, inspect the available-flights table and its listed rows, then assert the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action.

## Step 6 @verifies ac-91, ac-92, ac-93, ac-94, ac-95

On the reserve page for the São Paolo to Cairo search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
