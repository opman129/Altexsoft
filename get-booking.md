# Get Booking

## Description

**Get Booking** provides a normalized view of reservations by combining both PNRs and orders.

This is achieved by executing internal calls to the PNR and Order domains, respectively, and then consolidating the information into a single normalized response.
Additionally, this API sources extra content from other Sabre internal domains (Ticketing, Pricing, etc.) to provide a holistic view of Sabre reservations and to support traveler-oriented use cases (for example, "can I change my ticket?").

## Reasons to Use it

Simplifies the booking retrieval process by removing the need to use individual/granular APIs to retrieve a reservation.
Retrieves a normalized view of the reservation regardless of the content sources (PNR, NDC Order).
Provides additional data relevant for travelers (e.g., fare rules) as well as data elements that are not stored in the Sabre PNR (e.g., ticket details and more).
Retrieves reservation in a stateless way.

## Steps

## Requests and Responses

### Request

```
{
  "confirmationId": "GLEBNY",
  "bookingSource": "SABRE",
  "givenName": "John",
  "middleName": "W",
  "surname": "Smith",
  "returnOnly": [
    "FLIGHTS"
  ],
  "extraFeatures": {
    "returnFrequentRenter": false,
    "returnFiscalId": false
  },
  "unmaskPaymentCardNumbers": false
}
```

### Response




