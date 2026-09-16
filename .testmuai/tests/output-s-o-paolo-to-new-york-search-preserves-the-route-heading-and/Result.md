---
test: ../s-o-paolo-to-new-york-search-preserves-the-route-heading-and_test.md
status: passed
started: 2026-09-16T17:56:58.833Z
duration_s: 243
session_id: d06fbe59-ba12-43d8-94d6-b29e08251caf
---

# São Paolo to New York search preserves the route heading and lands on the fixed purchase details — Result

## Step 1 ✓ passed (28.6s)
md5: d8f96aed85173d00eadbc0f06c3d406f
Open https://blazedemo.com/ in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (35s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (23s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (48.4s)
md5: 30a91d8da3c07375d4749c9847490bdf
On the BlazeDemo home page, select São Paolo as the departure city and New York as the destination city, submit the search with Find Flights, then assert the browser reaches the reserve page and the page heading includes both "São Paolo" and "New York".

## Step 5 ✓ passed (49.1s)
md5: cb0f6c01621b8dbf74acda552112b3af
On the reserve page for the São Paolo to New York search, inspect the available-flights table and its listed rows, then assert the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action.

## Step 6 ✓ passed (53s)
md5: 95f097fef9038e1b5b4ba9f8ab8257d7
On the reserve page for the São Paolo to New York search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
