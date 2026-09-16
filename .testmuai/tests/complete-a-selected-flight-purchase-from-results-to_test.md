---
assurance:
  id: t-2
  base: sha256:8d57dc047724780794170580adf37fe58669a18d17d0024f59f2182d10f1e4ee
---
# Complete a selected flight purchase from results to confirmation and return home

> Prove that a traveler can choose a specific flight from the results page, reach that flight's purchase page, review the chosen-flight summary and purchase form, submit the booking successfully, see the sourced confirmation details, and return to the home page from the confirmation page.

## Import: t-1

@import ./search-available-flights-for-an-allowed-city-pair-from-the_test.md

## Step 1 @verifies ac-6

On the flight results reserve page reached from the imported search setup at https://blazedemo.com/, store one available row's Airline as selected_airline and Flight # as selected_flight_number, then choose that row's Choose This Flight control and assert the browser reaches the purchase page for that same flight.

## Step 2 @verifies ac-20, ac-21, ac-22, ac-23, ac-24

On the purchase page for the selected flight, inspect the chosen-flight summary table and store its displayed price as selected_price, then assert the summary displays a departure city, a destination city, the stored selected_flight_number, the stored selected_airline, and a price.

## Step 3 @verifies ac-25, ac-26, ac-27, ac-28, ac-29, ac-30, ac-31, ac-32, ac-33, ac-34, ac-35

On the same purchase page, inspect the purchase form, then assert it contains Name on Card, Address, City, State, Zip Code, Card Type, Credit Card Number, Credit Card Month, and Credit Card Year; the Card Type options are exactly Visa and American Express; and a Remember me checkbox is present.

## Step 4 @verifies ac-7, ac-8, ac-9, ac-10, ac-12, ac-13, ac-14, ac-15, ac-16, ac-17, ac-18, ac-19

On the same purchase page, complete the purchase form with Name on Card {{purchase_name_on_card}}, Address {{purchase_address}}, City {{purchase_city}}, State {{purchase_state}}, Zip Code {{purchase_zip_code}}, Card Type Visa, Credit Card Number {{purchase_card_number_visa}}, Credit Card Month {{purchase_card_month}}, and Credit Card Year {{purchase_card_year}}, submit Purchase Flight, then assert the browser reaches the purchase confirmation page, the page shows the exact message "Thank you for your purchase today!", a numeric Order ID, the total amount paid equals the stored selected_price, and the confirmation summary displays {{purchase_name_on_card}}, {{purchase_address}}, {{purchase_city}}, {{purchase_state}}, {{purchase_zip_code}}, Visa, {{purchase_card_number_visa}}, and the entered expiration from {{purchase_card_month}} and {{purchase_card_year}}.

## Step 5 @verifies ac-36

On the purchase confirmation page, use the Home link or button, then assert the browser returns to https://blazedemo.com/ and shows the flight-search home page heading "Welcome to the Simple Travel Agency!".
