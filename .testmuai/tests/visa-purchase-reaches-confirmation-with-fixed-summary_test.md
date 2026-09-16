---
assurance:
  id: t-13
  base: sha256:ff047ace1ccb85062dfb14d86e314ff78e96e2fba208f1effb58996bb1c8beb8
---
# Visa purchase reaches confirmation with fixed summary structure and masked card number

> Prove a site visitor can submit billing details with Card Type Visa and complete the purchase flow to a confirmation page that shows the fixed confirmation structure, fixed Status and Auth Code values, and a masked card number, without asserting unsettled Amount or Expiration values.

## Step 1

Open {{start_url}} in the browser, search for flights from Paris to Cairo, choose the first listed flight's Choose This Flight action, and stop on the purchase page for that selection.

## Step 2 @verifies ac-74, ac-75, ac-76, ac-77, ac-78

On the BlazeDemo purchase page reached from the Paris to Cairo search, review the reserved-flight heading and reservation details section, then assert the heading is exactly "Your flight from TLV to SFO has been reserved.", the reservation details labels are exactly Airline, Flight Number, Price, Arbitrary Fees and Taxes, and Total Cost, the Airline value is United, the Flight Number value is UA954, and the Price value is 400.

## Step 3 @verifies ac-79, ac-80, ac-81

On the purchase page, review the billing and payment form from top to bottom, then assert the fields appear in this order: Name, Address, City, State, Zip Code, Card Type, Credit Card Number, Month, Year, Name on Card, the Card Type options are exactly Visa and American Express, and a Remember me checkbox appears after the Name on Card field.

## Step 4

On the purchase page, complete the form with Name {{purchase_name}}, Address {{purchase_address}}, City {{purchase_city}}, State {{purchase_state}}, Zip Code {{purchase_zip_code}}, Card Type Visa, Credit Card Number {{purchase_card_number_visa}}, Month {{purchase_card_month}}, Year {{purchase_card_year}}, Name on Card {{purchase_name_on_card}}, and leave Remember me unchecked.

## Step 5 @verifies ac-67, ac-82

On the completed purchase page, submit Purchase Flight, then assert the browser reaches /confirmation.php and the page shows the message "Thank you for your purchase today!".

## Step 6 @verifies ac-69, ac-70, ac-71, ac-68, ac-72, ac-73, ac-83, ac-84, ac-85, ac-86, ac-87, ac-88

On the BlazeDemo confirmation page, review the transaction summary table and surrounding confirmation content, then assert the row labels are exactly Id, Status, Amount, Card Number, Expiration, Auth Code, and Date, the purchase-identifier label is Id, the Id row value contains only digits, the Card Number row shows the submitted card number masked so only the last four digits of {{purchase_card_number_visa}} remain visible and the full unmasked {{purchase_card_number_visa}} does not appear, the Status row is PendingCapture, the Auth Code row is 888888, and the page does not display {{purchase_name}}, {{purchase_address}}, {{purchase_city}}, {{purchase_state}}, {{purchase_zip_code}}, or the selected card-type text Visa.
