---
test: ../paris-to-new-york-search-shows-exact-route-text-and-reaches_test.md
status: passed
started: 2026-09-16T18:36:29.740Z
duration_s: 261
session_id: af691450-369b-4faa-9a6d-6e92ca0b70e8
---

# Paris to New York search shows exact route text and reaches the fixed purchase details — Result

## Step 1 ✓ passed (35s)
md5: efb8f4c62a73cd194302f0790a81f32e
Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (55.6s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (36s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (44.4s)
md5: c307c46ffdf81975d7ba8ac3e7b3c68a
On the BlazeDemo home page, select Paris as the departure city and New York as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from Paris to New York:".

## Step 5 ✓ passed (37.7s)
md5: ae45ebff452ac5f83cf84ba123a7fb90
On the results page for the Paris to New York search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: Paris", "Arrives: New York", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 ✓ passed (46.3s)
md5: 17b4981634da8677711940153e28e7b4
On the results page for the Paris to New York search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
