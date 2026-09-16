---
test: ../search-available-flights-for-an-allowed-city-pair-from-the_test.md
status: passed
started: 2026-09-16T15:05:09.619Z
duration_s: 0
session_id: 2745dfe7-f12d-4184-8355-39aa2bd9c1dd
---

# Search available flights for an allowed city pair from the home page — Result

## Step 1 ✓ passed (—)
md5: 022739e71540bef0c4f79ef3b4483339
Open https://blazedemo.com/ in the browser and remain on the flight-search home page.

## Step 2 ✓ passed (—)
md5: b4222e54621bf3e14e0a73228b47b39a
On https://blazedemo.com/, inspect the Departure City dropdown in the flight-search form, then assert its options are exactly Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, and São Paolo.

## Step 3 ✓ passed (—)
md5: bdf41e9a20f485742f83c0f9547c38a0
On https://blazedemo.com/, inspect the Destination City dropdown in the flight-search form, then assert its options are exactly Buenos Aires, Rome, London, Berlin, New York, Dublin, and Cairo.

## Step 4 ✓ passed (—)
md5: 0831e64c0e2bf1655f6012797476c51e
On https://blazedemo.com/, in the flight-search form, choose Paris as the Departure City and Buenos Aires as the Destination City, activate Find Flights, then assert the browser reaches the flight results reserve page, the page heading reflects Paris and Buenos Aires, and the results table shows the column headers Airline, Flight #, Departure Time, Arrival Time, and Price.
