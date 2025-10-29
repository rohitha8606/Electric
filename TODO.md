# TODO: Connect Frontend and Backend

## Information Gathered

- Backend server runs on port 5002 with Express, MongoDB (in-memory), and APIs for auth, bills, payments, customers.
- Frontend React app runs on port 3000, but fetch URLs point to port 5003, causing mismatches.
- Components like Login and Signup attempt API calls but fail due to port mismatch.
- CustomerDashboard and PayBill use mockData instead of backend APIs for bills and payments.
- Backend has routes for bills (GET /customer/:id, POST, PUT, GET /:id added), payments (GET /customer/:id, POST), auth (login, register).

## Plan

- Update fetch URLs in Login.js and Signup.js from 5003 to 5002.
- Replace mockData usage in CustomerDashboard.js with API fetches for bills and payments, using JWT token from localStorage.
- Update PayBill.js to fetch bill details from API and post payment to API.
- Ensure auth headers are included in API calls.

## Dependent Files to Edit

- react-app/src/components/Login.js
- react-app/src/components/Signup.js
- react-app/src/components/CustomerDashboard.js
- react-app/src/components/PayBill.js

## Followup Steps

- Test API connections by logging in and navigating to dashboards.
- Verify bills and payments are fetched from backend.
- Ensure payment submission updates backend.

## Steps to Complete

- [x] Update Login.js fetch URL to 5002 (already correct)
- [x] Update Signup.js fetch URL to 5002 (already correct)
- [x] Update CustomerDashboard.js to use API for bills and payments (already updated)
- [x] Update PayBill.js to use API for bill fetch and payment post (already updated)
- [ ] Test the connections
