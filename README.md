# Shamba AI

Shamba AI is a clickable mobile-first prototype designed for Kenyan farmers to estimate their farm size, calculate ploughing cost, and simulate a payment flow using M-Pesa-style UX.

## Project Summary

The app is built as a front-end prototype to demonstrate the user journey for:

- logging in or creating an account
- onboarding with farmer profile details
- measuring a farm boundary by tapping points on a map canvas
- viewing the estimated area in acres
- calculating ploughing cost based on a rate-per-acre slider
- paying using an M-Pesa simulation flow
- reviewing records, insights, and payment history

## Current Status

This repository currently contains a static prototype with no backend, database, or real payment integration. It is a UI/UX proof of concept intended to validate the product flow and business logic.

## Core Features

### 1. Splash and Authentication
- Splash screen introduction
- Login screen with phone number and PIN entry
- New-user onboarding flow

### 2. Farmer Profile Management
- Name, county, town, farm name, and size estimate
- Editable profile details
- Farm record snapshots

### 3. Boundary Measurement Simulation
- Farmers tap corner points on a boundary map
- The prototype calculates a preview area using a Shoelace-based polygon area formula
- Area is shown in acres

### 4. Cost Estimation
- Users adjust a rate-per-acre slider
- Estimated total cost updates instantly
- Results can be saved to the dashboard

### 5. M-Pesa Payment Simulation
- Phone input validation for M-Pesa-style number entry
- Simulated STK push process using timeouts
- Payment receipt generation and payment history listing

### 6. Insights and Records
- Payment trail
- Farm measurement records
- Savings/season cost comparison summary

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript
- SVG for map and boundary visualization
- Google Fonts for typography

## File Structure

- [index.html](index.html) — all UI, styling, and app logic in one static file

## How to Run

Because the project is a static HTML prototype, you can run it in either of the following ways:

1. Open [index.html](index.html) directly in a browser.
2. Serve it locally using a simple static server.

Example:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## User Journey

1. Launch the app from the splash screen.
2. Enter a phone number and a 4-digit PIN.
3. Complete onboarding with farmer details.
4. Tap corners to measure the farm boundary.
5. Review the measured area in acres.
6. Choose the ploughing cost and save it to the dashboard.
7. Simulate the M-Pesa payment flow.
8. Review payment and farm records in profile and payments sections.

## Business Model (Prototype Direction)

The prototype suggests a practical monetization model for deployment:

- Commission on tractor bookings
- Convenience fee for booking and payment handling
- Premium subscription for advanced insights and unlimited records
- B2B partnerships with cooperatives, lenders, and input suppliers

## APIs and External Services

At the moment, the prototype does not call a real backend API.

Current external dependency:

- Google Fonts stylesheet for typography

Planned real-world integrations after deployment:

- M-Pesa Daraja API for STK Push
- geospatial/location APIs for improved field mapping
- farmer authentication backend
- payments and booking service backend
- analytics and reporting services

## Limitations of the Current Prototype

- No real authentication system
- No persistent database
- No production-grade payment processing
- No real geolocation or GPS triangulation
- No backend for user and record persistence
- No deployment configuration or server-side security

## Recommended Next Steps

1. Replace the simulated flow with a real backend.
2. Integrate secure user authentication.
3. Add a real database for farmer profiles and records.
4. Integrate M-Pesa Daraja for actual transaction flow.
5. Add geospatial mapping support and real farm boundary capture.
6. Build provider and booking workflows for tractor owners.
7. Prepare an analytics and reporting layer for farmers and operators.

## Documentation Note

This repository is currently documentation-light. This README provides a practical starting point for understanding the application, its user flow, and the next technical build steps.
