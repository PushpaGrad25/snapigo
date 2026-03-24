# Snapigo

Snapigo is a location-aware coupon management application that helps users make better use of their saved offers. It allows users to scan or upload coupons, extract relevant details, and receive notifications when they are near stores where those coupons can be used.

## Overview

Users often collect coupons but forget to use them or miss opportunities when they are physically near a store. Snapigo addresses this by combining OCR-based data extraction with real-time geolocation to provide timely and context-aware reminders.

The application focuses on bridging the gap between digital coupon storage and real-world usage.

## Features

- Scan or upload coupon images
- Extract details such as store name, discount, and expiration date
- Store and organize coupons in a structured format
- Monitor user location and match it with nearby stores
- Trigger notifications based on proximity
- Track expiration dates and send reminders

## Tech Stack

Frontend:
- React Native (Expo with Dev Client)
- Expo APIs (Camera, Location, Notifications)
- Axios

Backend:
- Node.js
- Express.js

Database:
- Supabase (PostgreSQL)

Core Integrations:
- OCR (Tesseract or Google Vision API)
- Geolocation services
- Push notifications

## System Flow

1. The user scans or uploads a coupon using the mobile app.
2. OCR extracts structured information from the image.
3. The backend processes and stores the coupon data in Supabase.
4. The app tracks user location (with permission).
5. When the user is near a relevant store, a notification is triggered.

## Project Structure


snapigo/
├── mobile/ # React Native (Expo) app
├── server/ # Backend (Node.js / Express)
├── services/ # OCR and location logic
├── models/ # Data handling / schemas
├── routes/ # API endpoints
└── README.md


## Installation

Clone the repository:


git clone https://github.com/your-username/snapigo.git

cd snapigo


Install dependencies:

Mobile app:

cd mobile
npm install --legacy-peer-deps


Backend:

cd ../server
npm install --legacy-peer-deps


## Environment Variables

Create a `.env` file in the server directory:


PORT=5000
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
GOOGLE_MAPS_API_KEY=your_key
OCR_API_KEY=your_key
JWT_SECRET=your_secret


## Running the Application

Start backend:

cd server
npm start


Start mobile app:

cd mobile
npx expo start --dev-client


## Future Improvements

- Smarter coupon matching using machine learning
- Integration with retailer APIs for validation
- Automatic coupon extraction from emails or receipts
- Analytics for tracking savings and usage patterns
