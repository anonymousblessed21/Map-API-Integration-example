# Responsive Location Directory & Automated Data Pipeline

A live, interactive full-stack prototype demonstrating an end-to-end data pipeline. This project combines high-performance automated data extraction with a dynamic, mobile-optimized split-pane geospatial interface.

## 🚀 Live Demo
Experience the production deployment live in your browser:
👉 [Live Web Application](https://anonymousblessed21.github.io/Map-API-Integration-example/)

---

## 🛠️ System Architecture

The application is engineered in two completely decoupled layers to ensure maximum performance, speed, and structural flexibility:

### 1. The Backend Automation Pipeline (`scraper.py`)
Instead of relying on brittle DOM-based scrapers that fail during visual frontend redesigns, this architecture focuses on **Network Interception Mechanics**.
* **Engine:** Built using Python.
* **Strategy:** Intercepts internal XHR/API endpoints directly from target sources to pull raw, unthrottled data streams.
* **Resilience:** Ready for headless browser integration via Playwright/Selenium to maintain session contexts and execute complex JavaScript widgets or reactive user interactions.
* **Output:** Normalizes messy frontend data into a clean, standardized, and production-ready `scraped_events.json` schema.

### 2. The Interactive Geospatial Frontend UI
A beautifully responsive split-pane interface engineered for immediate user engagement and seamless state management.
* **Mapping Layer:** Integrated Map API displaying dynamic, precise interactive geolocation plot nodes.
* **Dynamic Filtering:** On-the-fly category filtering (e.g., Music, Food & Drink, Art) with instant rendering state updates.
* **Mobile Optimization:** Fully fluid breakpoints designed specifically to maintain viewport integrity on mobile, tablet, and desktop viewports.

---

## 📁 Repository Structure

```text
├── scraper.py            # Custom Python data engineering & API interception logic
├── scraped_events.json   # Normalized, structured target database payload
├── index.html            # Main viewport structure (Split-pane canvas configuration)
├── css/                  # Mobile-first responsive layouts and presentation layers
└── js/                   # Mapping API integration and dynamic state filtering logic
