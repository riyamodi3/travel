---
assurance:
  id: t-26
  base: sha256:4d0af7d2473227527a16f09de69bba168f6b2edc96aa2efd1afb8dde9dee842b
---
# Accented-route purchase reaches confirmation while keeping the fixed TLV-to-SFO heading

> Prove that after choosing a route with accented and multi-word city names, the purchase page still shows the fixed TLV to SFO heading and fixed reservation details before the purchase completes to confirmation.

## Step 1

Open BlazeDemo at {{start_url}} and search for flights from São Paolo to New York so the browser reaches the flight results page for that route.

## Step 2 @verifies ac-89, ac-90, ac-74, ac-75, ac-76, ac-77, ac-78

On the flight results page for São Paolo to New York, choose any listed flight so the browser reaches the purchase page, then assert the heading reads `Your flight from TLV to SFO has been reserved.`, the heading does not display `São Paolo` or `New York`, and the reservation details show exactly these labels in order: `Airline`, `Flight Number`, `Price`, `Arbitrary Fees and Taxes`, `Total Cost`, with `United` as the Airline value, `UA954` as the Flight Number value, and `400` as the Price value.

## Step 3 @verifies ac-79, ac-80, ac-81

On the purchase page, inspect the billing form before submitting it, then assert the fields appear in this order: `Name`, `Address`, `City`, `State`, `Zip Code`, `Card Type`, `Credit Card Number`, `Month`, `Year`, `Name on Card`, the Card Type control offers only `Visa` and `American Express`, and a `Remember me` checkbox is present after `Name on Card`.

## Step 4 @verifies ac-67, ac-82

On the same purchase page, submit the form with Name {{purchase_name}}, Address {{purchase_address}}, City {{purchase_city}}, State {{purchase_state}}, Zip Code {{purchase_zip_code}}, Card Type `Visa`, Credit Card Number {{purchase_card_number_visa}}, Month {{purchase_card_month}}, Year {{purchase_card_year}}, Name on Card {{purchase_name_on_card}}, leaving `Remember me` unchecked, then assert the browser navigates to `/confirmation.php` and the page displays `Thank you for your purchase today!`.

## Step 5 @verifies ac-68, ac-69, ac-70, ac-71, ac-72, ac-73, ac-83, ac-84, ac-85, ac-86, ac-87, ac-88

On the confirmation page from that submission, inspect the transaction summary and the rest of the visible page, then assert the rows are exactly `Id`, `Status`, `Amount`, `Card Number`, `Expiration`, `Auth Code`, `Date` in order, the generated identifier row is labelled `Id`, the Id value contains digits only, the Status value is `PendingCapture`, the Auth Code value is `888888`, the Card Number value shows {{purchase_card_number_visa}} masked to only its last four digits, and the page does not display {{purchase_name}}, {{purchase_address}}, {{purchase_city}}, {{purchase_state}}, {{purchase_zip_code}}, or the selected Card Type value `Visa`.
