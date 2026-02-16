\# Implementation Plan – Product Monitor (Walmart)



\## What does this repo do in plain language?

This project repeatedly checks product pages (including Walmart pages) and detects when a product is available (not "Sold Out"). When availability changes, it sends an automated alert to a Discord channel using a webhook.



\## What would need to change to use it for a real company?

\- Compliance \& reliability: Prefer official retailer APIs or approved data feeds over HTML scraping; add clear rate limiting and retry logic.

\- Security: Remove hard-coded webhook URLs from code and store secrets in environment variables.

\- Data storage: Write results to a database table (product\_id, timestamp, in\_stock, price) instead of printing to console.

\- Operations: Add scheduling (cron/Airflow) and monitoring/alerting for failures.

\- Engineering quality: Add unit tests, structured logging, and configuration files so links and alert targets are not hard-coded.



