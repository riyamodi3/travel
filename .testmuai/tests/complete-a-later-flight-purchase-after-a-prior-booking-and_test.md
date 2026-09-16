---
assurance:
  id: t-3
  base: sha256:9932e0bb59dd18a34b1a6e3baf7049b47bb59cd43191b7119e81c2879a06c526
---
# Complete a later flight purchase after a prior booking and receive a different Order ID

> Prove that after one completed flight booking already exists, a later completed booking produces a different numeric Order ID while still reaching the confirmation page and showing the sourced confirmation contract for the later purchase.

## Import: t-1

@import ./search-available-flights-for-an-allowed-city-pair-from-the_test.md

## Step 1

On the flight results reserve page reached from the imported search setup at https://blazedemo.com/, choose one available flight row and reach its purchase page.

## Step 2

On that first purchase page, complete the purchase form with Name on Card {{purchase_name_on_card}}, Address {{purchase_address}}, City {{purchase_city}}, State {{purchase_state}}, Zip Code {{purchase_zip_code}}, Card Type Visa, Credit Card Number {{purchase_card_number_visa}}, Credit Card Month {{purchase_card_month}}, and Credit Card Year {{purchase_card_year}}, submit Purchase Flight, and remain on the first purchase confirmation page.

## Step 3

Capture baseline: on the first purchase confirmation page, store the shown numeric Order ID as prior_order_id and use the Home link or button to return to https://blazedemo.com/.

## Step 4

On https://blazedemo.com/, in the flight-search form, choose Paris as the Departure City and Buenos Aires as the Destination City, then open the flight results reserve page again.

## Step 5 @verifies ac-6

On the second flight results reserve page, store one available row's Airline as later_airline and Flight # as later_flight_number, then choose that row's Choose This Flight control and assert the browser reaches the purchase page for that same flight.

## Step 6 @verifies ac-20, ac-21, ac-22, ac-23, ac-24

On the later purchase page, inspect the chosen-flight summary table and store its displayed price as later_price, then assert the summary displays a departure city, a destination city, the stored later_flight_number, the stored later_airline, and a price.

## Step 7 @verifies ac-25, ac-26, ac-27, ac-28, ac-29, ac-30, ac-31, ac-32, ac-33, ac-34, ac-35

On the same later purchase page, inspect the purchase form, then assert it contains Name on Card, Address, City, State, Zip Code, Card Type, Credit Card Number, Credit Card Month, and Credit Card Year; the Card Type options are exactly Visa and American Express; and a Remember me checkbox is present.

## Step 8 @verifies ac-7, ac-8, ac-9, ac-10, ac-11, ac-12, ac-13, ac-14, ac-15, ac-16, ac-17, ac-18, ac-19

On the same later purchase page, complete the purchase form with Name on Card {{purchase_name_on_card}}, Address {{purchase_address}}, City {{purchase_city}}, State {{purchase_state}}, Zip Code {{purchase_zip_code}}, Card Type American Express, Credit Card Number {{purchase_card_number_amex}}, Credit Card Month {{purchase_card_month}}, and Credit Card Year {{purchase_card_year}}, submit Purchase Flight, then assert the browser reaches the purchase confirmation page, the page shows the exact message "Thank you for your purchase today!", the shown Order ID is numeric and different from the stored prior_order_id, the total amount paid equals the stored later_price, and the confirmation summary displays {{purchase_name_on_card}}, {{purchase_address}}, {{purchase_city}}, {{purchase_state}}, {{purchase_zip_code}}, American Express, {{purchase_card_number_amex}}, and the entered expiration from {{purchase_card_month}} and {{purchase_card_year}}.

## Step 9 @verifies ac-36

On the later purchase confirmation page, use the Home link or button, then assert the browser returns to https://blazedemo.com/ and shows the flight-search home page heading "Welcome to the Simple Travel Agency!".
