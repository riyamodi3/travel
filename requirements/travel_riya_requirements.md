# BlazeDemo — Airline / Travel Booking Requirements

Base URL: https://blazedemo.com/
Source: public site content (home page, flight search results, purchase, and confirmation pages) captured 2026-09-16.

This document describes BlazeDemo's **observed** behaviour, verified by direct browser
execution on 2026-09-16. BlazeDemo is a deliberately simplistic demo application: the
purchase and confirmation pages do not carry the selected flight through, and the
confirmation page does not echo submitted billing details. Those behaviours are recorded
below as they actually are, not as a conventional booking flow would define them.

## Home Page — Flight Search

- The home page displays the heading "Welcome to the Simple Travel Agency!" and promotes a "destination of the week" offer.
- A Departure City dropdown offers: Paris, Philadelphia, Boston, Portland, San Diego, Mexico City, São Paolo.
- A Destination City dropdown offers: Buenos Aires, Rome, London, Berlin, New York, Dublin, Cairo.
- A "Find Flights" button submits the selected departure and destination cities and navigates to the flight results (reserve) page.

## Flight Results Page

- The reserve page lists available flights in a table whose column headers are, left to
  right: "Choose", "Flight #", "Airline", "Departs: <departure city>", "Arrives:
  <destination city>", and "Price". The two middle headers are route-dependent — a Paris to
  Cairo search renders them as "Departs: Paris" and "Arrives: Cairo" — rather than static
  "Departure Time" / "Arrival Time" labels. Observed for the Paris to Cairo route; the
  substitution pattern is inferred from that single observation.
- The page heading reads "Flights from <departure city> to <destination city>:" (observed as
  "Flights from Paris to Cairo:").
- Each row has a "Choose This Flight" button that proceeds to the purchase page. The purchase
  page does not carry that row's flight details through — see the Purchase Page section.

## Purchase Page

- Choosing a flight navigates to the purchase page at `/purchase.php`.
- The purchase page heading reads "Your flight from TLV to SFO has been reserved." This text
  is fixed: it does not reflect the departure and destination cities selected on the home
  page. Selecting Paris to Cairo still produces the TLV to SFO heading.
- The reservation details show Airline, Flight Number, Price, Arbitrary Fees and Taxes, and
  Total Cost. These values are also fixed — Airline "United", Flight Number "UA954", Price
  "400" — and do not reflect the airline, flight number, or price of the flight chosen on the
  results page.
- The purchase form collects, in order: Name, Address, City, State, Zip Code, Card Type
  (Visa or American Express), Credit Card Number, Month, Year, Name on Card.
- A "Remember me" checkbox is present on the purchase form, after the "Name on Card" field.
- A "Purchase Flight" button submits the form and navigates to the purchase confirmation page.

## Purchase Confirmation Page

- Submitting the purchase form navigates to the confirmation page at `/confirmation.php`.
- The confirmation page displays the message "Thank you for your purchase today!"
- The confirmation page displays a transaction summary table with exactly these rows: Id,
  Status, Amount, Card Number, Expiration, Auth Code, Date.
- The Id row holds a numeric value generated per purchase (for example `1789578423526`). The
  row is labelled "Id", not "Order ID".
- The Amount row showed "555 USD" in the observed purchase. It did not correspond to the price
  of the chosen flight ($472.56), nor to the Total Cost shown on the purchase page (914.76).
  Observed once; whether the value is constant across purchases is not yet established.
- The Card Number row shows the submitted card number masked to its last four digits (for
  example `xxxxxxxxxxxx1111` for a card ending 1111).
- The Expiration row showed "11 /2018" for a purchase submitting Month 12 and Year 2030, so it
  does not echo the submitted expiry. Observed once; whether the value is constant across
  purchases is not yet established.
- The Status row shows "PendingCapture" and the Auth Code row shows "888888".
- The confirmation page does **not** display the purchaser's submitted Name, Address, City,
  State, or Zip Code, and does not display the selected Card Type.
- A "Home" link/button returns the user to the home page.

## Navigation

- The "home" link in the top navigation is available on every page and returns the user to the flight search home page.
