---
test: ../visa-purchase-completes-and-echoes-submitted-billing-and_test.md
status: failed
started: 2026-09-16T16:54:42.255Z
duration_s: 165
session_id: 10f08773-293e-4ff6-a43b-24ef981a13c7
---

# Visa purchase completes and echoes submitted billing and payment details — Result

## Step 1 ✓ passed (39.9s)
md5: 099c081360769b2fa6dfa60954b7c85f
Open https://blazedemo.com/ in the browser, search for flights from Paris to Cairo, and reach the flight results page.

## Step 2 ✗ failed (120.1s)
md5: 23a0bda457a7d48d33c1b73499e10f1d
Reason: AP determined agent is stuck — no viable actions remain — bug verdict: Purchase summary shows an unrelated reserved flight [application_issue/ui_data_defect, confidence 0.98]
On the BlazeDemo flight results page for Paris to Cairo, store the first listed flight row's departure city, destination city, flight number, airline, and price as chosen_departure_city, chosen_destination_city, chosen_flight_number, chosen_airline, and chosen_price, choose that row's Choose This Flight action, then assert the purchase page shows the same departure city, destination city, flight number, airline, and price in the chosen-flight summary.

## Step 3 ⏭ skipped

## Step 4 ⏭ skipped

## Step 5 ⏭ skipped

## Step 6 ⏭ skipped
