# DeckWatch
Scanner for Steam Deck Availability

We are building a system called DeckWatch that monitors the availability of Steam Deck models from Valve and notifies users in real time.

The system has two main components:
Web Application (Frontend + Backend)
Discord Integration (Notification System)

System Architecture:
1. Web Application
The web app will retrieve data from a backend service that continuously monitors stock availability.
The web application serves as the main interface for users and includes:
1) A dashboard displaying real-time Steam Deck availability 
2) Status updates for each model and region
3) Direct links to the official purchase pages
4) A link/invite to the Discord server
5) Optional user settings (e.g., sound alerts, themes)

2. Discord Server
The Discord server will:
1) Receive automated notifications when stock becomes available
2) Organize notifications into channels (e.g., by region or product type)
3) Optionally support role-based notifications (users subscribe to specific regions or products)


Core Feature: Steam Deck Stock Monitoring
The system will poll the official Valve Steam Deck store page at a regular interval (target: every 15 seconds; may be adjusted to 10–30 seconds depending on reliability and rate limits). It will detect stock availability per model and per region. Results will be displayed on the website dashboard and updated in near real time. When a product transitions from out of stock → in stock: trigger a website sound alert and send a Discord notification (optionally role-specific). Each product entry should include: Model name, Region, Availability status (in stock / out of stock / unknown), Price (if available), Direct purchase link and Last checked timestamp. 

Secondary Features:
1. Third-Party Marketplace Monitoring
The system will monitor selected third-party marketplaces for Steam Deck listings, including: Mercari, eBay, Amazon. For each listing: display on the website and in Discord channels and include price comparison against official retail pricing. Flag listings based on pricing: 1) ≥ 25% above retail → label as “Likely Scalper” 2) ≥ 50% below retail → label as “Possible Scam or Damaged Item”
2. Accessories and Parts Tracking
The system will also track listings for: Steam Deck accessories (e.g., docks, cases, chargers), Steam Deck parts (e.g., replacement components). These will be displayed in dedicated sections on the website or posted to separate channels in the Discord server.


