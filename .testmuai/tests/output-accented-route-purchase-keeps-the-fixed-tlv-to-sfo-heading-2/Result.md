---
test: ../accented-route-purchase-keeps-the-fixed-tlv-to-sfo-heading-2_test.md
status: failed
started: 2026-09-16T18:13:41.591Z
duration_s: 190
session_id: 46b33e6d-da51-48a8-807a-a7ae1a05e183
---

# Accented-route purchase keeps the fixed TLV-to-SFO heading through confirmation — Result

## Step 1 ✓ passed (60.4s)
md5: 115ce690bb13df8d33cdcd3941f4775f
Open {{start_url}} in the browser, search for flights from São Paolo to New York, choose the first listed flight's Choose This Flight action, and stop on the purchase page for that selection.

## Step 2 ✓ passed (49.3s)
md5: 54036d7b9d8b8c91e6c2a11d34f8eb10
On the BlazeDemo purchase page reached from the São Paolo to New York search, review the reserved-flight heading and reservation details section, then assert the heading is exactly "Your flight from TLV to SFO has been reserved.", the heading does not display São Paolo or New York, the reservation details labels are exactly Airline, Flight Number, Price, Arbitrary Fees and Taxes, and Total Cost, the Airline value is United, the Flight Number value is UA954, and the Price value is 400.

## Step 3 ✗ failed (75.7s)
md5: dce947f54a9edbc6786ec070ec81c58d
Reason: Final verification failed: "the fields appear in this order: Name, Address, City, State, Zip Code, Card Type, Credit Card Number, Month, Year, Name on Card, the Card Type options are exactly Visa and American Express, and a Remember me checkbox appears after the Name on Card field." — bug verdict: Purchase-form verification did not inspect below-fold fields [automation_bug/agent_misstep, confidence 0.93]
On the purchase page, review the billing and payment form from top to bottom, then assert the fields appear in this order: Name, Address, City, State, Zip Code, Card Type, Credit Card Number, Month, Year, Name on Card, the Card Type options are exactly Visa and American Express, and a Remember me checkbox appears after the Name on Card field.

## Step 4 ⏭ skipped

## Step 5 ⏭ skipped

## Step 6 ⏭ skipped
