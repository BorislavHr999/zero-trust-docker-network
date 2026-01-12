# 🛡️ Zero-Trust Docker Network Lab

This project simulates a secure, multi-tier enterprise infrastructure running locally via Docker Compose. unlike standard setups, it uses **Manual IPAM** (IP Address Management) to assign static IPs across three isolated subnets: **DMZ** (Gateway), **App Net**, and **Data Net**.

* **Architecture:** Nginx (Zone A) -> Node.js (Zone B) -> PostgreSQL (Zone C).
* **Security:** Direct access to the backend and database is blocked. Traffic is strictly routed via the Nginx Reverse Proxy using internal static IPs (`192.168.201.x`).
* **Networking:** Features custom subnet definitions (`/24`) and bridge drivers to prevent authorized access.

### 🚀 Quick Start
Run `docker compose up -d` and visit `http://localhost` to verify the secure connection chain.
