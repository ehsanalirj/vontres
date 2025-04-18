# Vontres Ordering Ecosystem

## Overview

Vontres Ordering is an AI-powered food ordering ecosystem designed to unite restaurants and provide them with full control over their operations. This platform offers a range of features including menu management, branch control, integrations, payments, branding, and automation.

## Features

### Customer-Facing Landing Page

-   **Purpose**: Sales funnel and onboarding interface for restaurants.
-   **Technology**: Next.js
-   **Key Components**:
    -   Feature showcases (realtime menu updates, branch control, AI-powered backend)
    -   Interactive demos (live menu simulator)
    -   Explainers on integrations with websites, Foodpanda, Careem, etc.
    -   Signup for early access or account creation

### Global Admin Panel

-   **Purpose**: Centralized system for managing the entire ecosystem.
-   **Key Features**:
    -   Role-based admin users with granular permissions
    -   View and manage all restaurants, plans, users, usage metrics
    -   Global analytics dashboard: orders, growth, top cities, sync issues
    -   Feature toggles: enable/disable features per restaurant
    -   AI Debug Tool: run or fix code snippets inside the admin panel
    -   AI Code Prototyper: prompt AI to add features to specific restaurants

### Restaurant Subdomains

-   **Purpose**: Each restaurant gets its own subdomain with a self-contained dashboard and live storefront.
-   **Example**: `burgerplace.vontres.com`
-   **Key Features**:
    -   Setup flow: add country, cities, branches
    -   Branch hours, dine-in/takeout toggle, kitchen prep time
    -   Realtime menu editor: add/remove items, modifiers, categories, allergens
    -   One-click menu sync with Foodpanda, Careem, and their website
    -   Visual designer for storefront (drag & drop UI builder for themes, fonts, colors, layout)
    -   Toggle item availability live (e.g., "Karahi sold out")
    -   Set branch-level pricing and delivery zones
    -   Assign staff, roles, devices per branch

### Restaurant Feature Flexibility

-   **Purpose**: Allow restaurants to customize their feature set.
-   **Key Features**:
    -   Assign or restrict features per restaurant
    -   Invoice generation
    -   Payment options: JazzCash, Stripe, COD, BNPL
    -   Menu-level permissions for staff
    -   Delivery handled by own fleet or 3rd party
    -   Upload custom scripts (tracking, ads)
    -   Add discount campaigns (BOGO, cart %)
    -   Sync inventory with supplier APIs (optional)
    -   Define SLA rules (auto-cancel if late, alert if prep time > X)

### Restaurant Onboarding Assistant (AI-Aided)

-   **Purpose**: Streamline the onboarding process for new restaurants.
-   **Key Features**:
    -   Upload PDF/image menus → AI extracts structured items
    -   Use Google Maps API to autofill branches
    -   AI recommends pricing based on city and cuisine category
    -   AI Setup Checklist (automated): menu uploaded, payment method added, first order test, integration test passed

### Order Taking Assistant (OTA) — Voice AI System

-   **Purpose**: AI-powered voice call system that takes orders on phone calls.
-   **Key Features**:
    -   Customers call a number, hear an AI voice (natural, friendly Urdu/English)
    -   System uses conversational AI to greet user, ask what they want, confirm items, collect info, and confirm ETA
    -   Backend has Live Agents panel: agent monitors calls in real-time and can intervene or take over manually
-   **Technology**:
    -   Twilio for voice infra
    -   Whisper for transcription
    -   Urdu+English TTS (text-to-speech)
    -   Vontres AI NLP pipeline for intent + entity extraction

### Customer Experience Module

-   **Purpose**: Enhance the customer ordering experience.
-   **Key Features**:
    -   Web, mobile, WhatsApp support
    -   Realtime cart, multi-city order support
    -   Predictive search ("Biryani in Gulberg")
    -   Suggested addons + combo deals
    -   Loyalty wallets + cashback options
    -   Arabic, Urdu, English UI
    -   Crypto and traditional payment support

### Multi-Tenant API Layer

-   **Purpose**: Expose all data and features via secure APIs.
-   **Key Features**:
    -   All data and features exposed via secure REST + GraphQL APIs
    -   Rate-limited, token-based developer access
    -   Support headless frontend models (e.g., restaurants building custom ordering apps)

### AI & Automation Everywhere

-   **Purpose**: Leverage AI to automate and optimize various aspects of the ecosystem.
-   **Key Features**:
    -   Use LLMs + Firebase AI to:
        -   Suggest promotions (e.g., "try 20% off on slowest items")
        -   Highlight anomalies (order drops, delays, bugs)
        -   Enable live-debugging of code in admin & subdomains
        -   Auto-generate dashboards, SEO content, menu descriptions
        -   Forecast demand by branch

### Backend & Infra Architecture

-   **Backend**: Node.js with NestJS
-   **Frontend**: Flutter (app), Next.js (web), React + Tailwind (dashboards)
-   **Infra**:
    -   Firebase Auth + Firestore
    -   PostgreSQL for structured data
    -   Redis for real-time menu & cart sync
    -   Docker + GKE + Cloudflare
-   **Security**: End-to-End encryption, device binding, IP restriction for admins
-   **DevOps**: CI/CD with GitHub Actions, staging environment, error logging via Sentry

## Getting Started

### Prerequisites

-   Node.js
-   npm or yarn
-   Next.js CLI

### Installation

1.  Clone the repository:

    ```bash
    git clone [repository_url]
    cd vontres-ordering
    ```

2.  Install dependencies:

    ```bash
    npm install
    # or
    yarn install
    ```

### Development

1.  Start the development server:

    ```bash
    npm run dev
    # or
    yarn dev
    ```

2.  Open your browser and navigate to `http://localhost:3000`.

## Contributing

We welcome contributions to the Vontres Ordering ecosystem. Please follow these guidelines:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Commit your changes with descriptive commit messages.
4.  Push your changes to your fork.
5.  Submit a pull request.

## License

This project is licensed under the [License Name] License.
