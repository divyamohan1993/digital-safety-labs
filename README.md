# Digital Safety Labs

Lightweight, **offline-first** demos to teach digital safety: cookie consent,
email subscriptions, phone-for-discounts, “partner” data sharing, and how these
fuel common scams. Each demo is a single static page (Bootstrap 5.3 via CDN)
that runs entirely in the browser using `localStorage`.

> Purpose-built for schools, NGOs, rural trainings, CSR, and community sessions.

---

## What’s inside

- **demos/cookies/** – Accept/Reject/Customize consent; mock tracker pings; event log  
- **demos/email/** – Subscribe/Unsubscribe; local inbox (no network); audit log  
- **demos/phone/** – Discount flow; SMS/e-bill/partner-sharing toggles; leak feed  
- **demos/scam-simulator/** – Uses provided data to generate likely scam scenarios  
- **assets/** – Minimal shared utilities (`core.js`, `i18n.json`, optional `style.css`)  
- **index.html** – Hub page listing all demos  
- **vm/** – (Optional) one-shot GCP VM script for connected classrooms

All demo data is stored under a **unique, namespaced key**:
`localStorage["DSL_<demoSlug>_V1"]` to keep modules isolated.

---

## Why this works in the field

- **Runs offline** on old hardware and 1 vCPU / ~0.6–1 GB RAM VMs.
- **Show, don’t tell:** live logs, leak feed, and scam predictions from *their* inputs.
- **Rural-ready UI:** large buttons, short lines, EN/HI labels, minimal text.
- **Privacy-first:** no analytics, no backends, no data leaves the browser.

---

## Quick start

### A) Totally offline (recommended)
1. Download the repo (or just a demo subfolder).
2. Open any `index.html` in a modern browser.
3. Use **Reset** between groups to clear `localStorage`.

### B) Cloud (Nginx on a tiny VM)
```bash
sudo apt update && sudo apt -y install nginx
sudo cp -r demos /var/www/html/
sudo cp index.html /var/www/html/index.html
# Open http://<VM_IP>/
