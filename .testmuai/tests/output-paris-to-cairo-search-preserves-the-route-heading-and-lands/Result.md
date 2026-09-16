---
test: ../paris-to-cairo-search-preserves-the-route-heading-and-lands_test.md
status: passed
started: 2026-09-16T17:40:55.836Z
duration_s: 304
session_id: 05e57cb0-39d7-4858-8591-c2545a26f0a6
---

# Paris to Cairo search preserves the route heading and lands on the fixed purchase details — Result

## Step 1 ✓ passed (43s)
md5: d8f96aed85173d00eadbc0f06c3d406f
Open https://blazedemo.com/ in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (44s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (25.3s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (69.5s)
md5: 4671ddcc19597dbc354a94c90f4a810f
On the BlazeDemo home page, select Paris as the departure city and Cairo as the destination city, submit the search with Find Flights, then assert the browser reaches the reserve page and the page heading includes both "Paris" and "Cairo".

## Step 5 ✓ passed (63.3s)
md5: 759837bde77ed5621f60d48912db1c63
On the reserve page for the Paris to Cairo search, inspect the available-flights table and its listed rows, then assert the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action.

## Step 6 ✓ passed (51.4s)
md5: 5eb2470c6d4751aee8f89f88992537a4
On the reserve page for the Paris to Cairo search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
