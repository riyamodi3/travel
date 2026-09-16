---
assurance:
  id: t-6
  base: sha256:80ddecce2425464077161b7f9f995ddb0cd0fb4ff0d1929febd74cbbfd8cd9ee
---
# Visa purchase completes and echoes submitted billing and payment details

> Prove a site visitor can review a selected flight on the purchase page, enter billing and Visa payment details, submit the purchase, and receive a confirmation showing the paid amount and echoed submitted details.

## Step 1

Open https://blazedemo.com/ in the browser, search for flights from Paris to Cairo, and reach the flight results page.

## Step 2 @verifies ac-22, ac-23, ac-24, ac-25, ac-26

On the BlazeDemo flight results page for Paris to Cairo, store the first listed flight row's departure city, destination city, flight number, airline, and price as chosen_departure_city, chosen_destination_city, chosen_flight_number, chosen_airline, and chosen_price, choose that row's Choose This Flight action, then assert the purchase page shows the same departure city, destination city, flight number, airline, and price in the chosen-flight summary.

## Step 3 @verifies ac-27, ac-28, ac-29, ac-30, ac-31, ac-32, ac-33, ac-34, ac-35, ac-36, ac-37

On the BlazeDemo purchase page for the selected flight, review the purchase form, then assert fields labeled Name on Card, Address, City, State, Zip Code, Card Type, Credit Card Number, Credit Card Month, and Credit Card Year are present, the Card Type field offers only Visa and American Express, and a Remember me checkbox is present.

## Step 4

Capture baseline: the browser is on the BlazeDemo purchase page for the selected flight before submitting the purchase form.

## Step 5 @verifies ac-8, ac-9, ac-10, ac-11, ac-12

On the BlazeDemo purchase page, enter Name on Card {{purchase_name_on_card}}, Address {{purchase_address}}, City {{purchase_city}}, State {{purchase_state}}, Zip Code {{purchase_zip_code}}, set Card Type to Visa, enter Credit Card Number {{purchase_card_number_visa}}, Credit Card Month {{purchase_card_month}}, Credit Card Year {{purchase_card_year}}, leave Remember me unchecked, submit Purchase Flight, then assert the browser reaches the purchase confirmation page, the page contains "Thank you for your purchase today!", the total amount paid equals chosen_price, and an Order ID is shown using digits only.

## Step 6 @verifies ac-14, ac-15, ac-16, ac-17, ac-18, ac-19, ac-20, ac-21

On the BlazeDemo purchase confirmation page, review the submitted-information and payment-details summary table, then assert it displays {{purchase_name_on_card}}, {{purchase_address}}, {{purchase_city}}, {{purchase_state}}, {{purchase_zip_code}}, Card Type Visa, Credit Card Number {{purchase_card_number_visa}}, and expiration {{purchase_card_month}} / {{purchase_card_year}}.
