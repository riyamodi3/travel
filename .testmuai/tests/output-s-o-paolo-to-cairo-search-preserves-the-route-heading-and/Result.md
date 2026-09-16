---
test: ../s-o-paolo-to-cairo-search-preserves-the-route-heading-and_test.md
status: failed
started: 2026-09-16T17:52:20.614Z
duration_s: 263
session_id: e2924edd-3947-4ebf-82d6-d353dd783fb7
---

# São Paolo to Cairo search preserves the route heading and lands on the fixed purchase details — Result

## Step 1 ✓ passed (25.3s)
md5: d8f96aed85173d00eadbc0f06c3d406f
Open https://blazedemo.com/ in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (55.8s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (39.8s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (66.3s)
md5: 0ac3a9f0d8bc34630cacc3ad0ad3ed96
On the BlazeDemo home page, select São Paolo as the departure city and Cairo as the destination city, submit the search with Find Flights, then assert the browser reaches the reserve page and the page heading includes both "São Paolo" and "Cairo".

## Step 5 ✗ failed (70.8s)
md5: e2ce25436fd020e448238b8b8966efea
Reason: Final verification failed: "the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action" — bug verdict: Flight-results table uses unexpected column headers [application_issue/ui_data_defect, confidence 0.97]
On the reserve page for the São Paolo to Cairo search, inspect the available-flights table and its listed rows, then assert the table columns are Airline, Flight #, Departure Time, Arrival Time, and Price, and each listed result row offers a "Choose This Flight" action.

## Step 6 ⏭ skipped
