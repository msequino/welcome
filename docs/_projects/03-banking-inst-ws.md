---
title: Public site for Italian banks
subtitle: Institutional access point for the bank's customer-facing web experience
tech:
  - Scala
  - Play Framework
  - Mongo
  - Angular Js
---

## Overview

A single-page application built in AngularJS that consumed a Play Framework REST API. This institutional portal was developed for a major Italian bank, using a client-side SPA architecture with JWT-based authentication and MongoDB/GridFS persistence.

## Key Features

- **AngularJS SPA** — a client-side single-page application with dynamic routing, interactive views, and a responsive user experience.
- **Play REST API** — Scala/Play endpoints serving JSON to the AngularJS frontend for data access and business operations.
- **JWT authentication** — self-managed authentication using JWT access tokens and refresh tokens for secure session handling.
- **MongoDB + GridFS** — persistence layer using MongoDB and GridFS for both structured data and large binary assets.
- **Secure API flow** — token renewal, expiration handling, and protected REST routes to secure the client-server communication.

## Technical Highlights

- Fully decoupled frontend and backend, with AngularJS handling UI state and Play delivering RESTful resources.
- Play Framework controllers and services implemented API endpoints, auth checks, and JSON serialization.
- JWT access and refresh token model enabled stateless authentication and smoother SPA session management.
- MongoDB and GridFS provided flexible storage for application data, configuration, and document assets.
- A maintainable architecture with clear module boundaries between UI, business logic, and persistence.

## Lessons & Notes

- JWT tokens work well for SPAs but require robust refresh and expiration handling to avoid stale sessions.
- A fully client-driven SPA architecture made the application feel more responsive while still allowing the backend API to evolve independently.
- MongoDB GridFS was a good fit for storing larger binary assets alongside structured application data.
- Decoupling the AngularJS frontend from the Play backend simplified long-term maintenance and future updates.