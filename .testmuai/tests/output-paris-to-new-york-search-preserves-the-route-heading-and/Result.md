---
test: ../paris-to-new-york-search-preserves-the-route-heading-and_test.md
status: failed
started: 2026-09-16T17:46:22.294Z
duration_s: 344
session_id: f5f51579-f81f-4608-be2a-ab9aa0581b2a
---

# Paris to New York search preserves the route heading and lands on the fixed purchase details — Result

## Step 1 ✓ passed (21.1s)
md5: d8f96aed85173d00eadbc0f06c3d406f
Open https://blazedemo.com/ in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (49.8s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (40.2s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (58.2s)
md5: 0d91297bb957919fe3406f79a5b0a9de
On the BlazeDemo home page, select Paris as the departure city and New York as the destination city, submit the search with Find Flights, then assert the browser reaches the reserve page and the page heading includes both "Paris" and "New York".

## Step 5 ✗ failed (169.7s)
md5: 66d9c20ab54ce2f8aa8e0eaf7d01f20c
Reason: Final verification failed: "the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action"
On the reserve page for the Paris to New York search, inspect the available-flights table and its listed rows, then assert the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action.

## Step 6 ⏭ skipped
