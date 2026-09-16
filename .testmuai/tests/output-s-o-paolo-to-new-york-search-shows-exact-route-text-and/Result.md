---
test: ../s-o-paolo-to-new-york-search-shows-exact-route-text-and_test.md
status: passed
started: 2026-09-16T18:48:47.396Z
duration_s: 316
session_id: 383c9bba-3111-4b21-a533-dfaa339adfce
---

# São Paolo to New York search shows exact route text and reaches the fixed purchase details — Result

## Step 1 ✓ passed (29.4s)
md5: efb8f4c62a73cd194302f0790a81f32e
Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (41.1s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (45.4s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (86.4s)
md5: d9426cf34037a648e1847915dc051a25
On the BlazeDemo home page, select São Paolo as the departure city and New York as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from São Paolo to New York:".

## Step 5 ✓ passed (55.1s)
md5: a2bb344ef740107bf88102a220d5ae8a
On the results page for the São Paolo to New York search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: São Paolo", "Arrives: New York", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 ✓ passed (52.8s)
md5: 529fa30a4e5bff32db4e42b107b7a3e7
On the results page for the São Paolo to New York search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
