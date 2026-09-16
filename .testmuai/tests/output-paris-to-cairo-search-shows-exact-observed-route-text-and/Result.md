---
test: ../paris-to-cairo-search-shows-exact-observed-route-text-and_test.md
status: passed
started: 2026-09-16T18:31:14.944Z
duration_s: 292
session_id: a0c192a1-99f3-4ec9-b13c-2171869c68cf
---

# Paris to Cairo search shows exact observed route text and reaches the fixed purchase details — Result

## Step 1 ✓ passed (28.1s)
md5: efb8f4c62a73cd194302f0790a81f32e
Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (65.2s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (27.8s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (49.7s)
md5: 8959c4958373946f0a2411e742f47b8b
On the BlazeDemo home page, select Paris as the departure city and Cairo as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from Paris to Cairo:".

## Step 5 ✓ passed (43.5s)
md5: c7147130c18f4fe2dfe2a1163ac8a355
On the results page for the Paris to Cairo search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: Paris", "Arrives: Cairo", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 ✓ passed (71.5s)
md5: a2591ab926675be683e278f60b4e13bf
On the results page for the Paris to Cairo search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
