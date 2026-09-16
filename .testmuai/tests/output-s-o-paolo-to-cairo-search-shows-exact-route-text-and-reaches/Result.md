---
test: ../s-o-paolo-to-cairo-search-shows-exact-route-text-and-reaches_test.md
status: passed
started: 2026-09-16T18:41:13.118Z
duration_s: 432
session_id: 739d6f46-88c8-428e-8cca-cd18bc999ad8
---

# São Paolo to Cairo search shows exact route text and reaches the fixed purchase details — Result

## Step 1 ✓ passed (17.9s)
md5: efb8f4c62a73cd194302f0790a81f32e
Open {{start_url}} in a browser and wait for the BlazeDemo home page with the flight-search form.

## Step 2 ✓ passed (65.2s)
md5: 7c9a6f1ec8406ef8ba1e9da0d21877ed
On the BlazeDemo home page, inspect the Departure City dropdown options, then assert the options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (32s)
md5: 87a85e816d7ac1ea55fe453d3cb24513
On the BlazeDemo home page, inspect the Destination City dropdown options, then assert the options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (73s)
md5: 33b3eb240b89dfa3147adca60a49cacd
On the BlazeDemo home page, select São Paolo as the departure city and Cairo as the destination city, submit the search with Find Flights, then assert the browser reaches the flight results page and the results-page heading is exactly "Flights from São Paolo to Cairo:".

## Step 5 ✓ passed (161.1s)
md5: fa04d86ab51db624e427b583c0979113
On the results page for the São Paolo to Cairo search, inspect the available-flights table and its listed rows, then assert a results table is shown with the headers "Choose", "Flight #", "Airline", "Departs: São Paolo", "Arrives: Cairo", and "Price", and each listed row exposes a "Choose This Flight" action.

## Step 6 ✓ passed (77.5s)
md5: caaf4f1af97da0dea49406961548f565
On the results page for the São Paolo to Cairo search, choose the first listed flight, then assert the browser reaches /purchase.php, the purchase-page heading is exactly "Your flight from TLV to SFO has been reserved.", and the reservation details show Airline "United", Flight Number "UA954", and Price "400".
