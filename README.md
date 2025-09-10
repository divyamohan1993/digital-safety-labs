# Digital Safety Labs

Practical, offline-first simulations that teach how common digital scams work—and how to stay safe. Built as single-file HTML demos that run entirely in the browser.

**Live:** https://dmj.one/labs/digital-safety/  
**Repo:** https://github.com/divyamohan1993/digital-safety-labs  
**Initiative:** Part of **dmj.one** — Quality Education for All.

---

## Why this exists
- **Activity-first learning:** People remember what they *do*, not what they read.
- **Zero setup:** No installs, no accounts, no servers. Works in labs, classrooms, villages, and on shared PCs.
- **Privacy by design:** No analytics, no trackers, no network calls for user data.

---

## What you get
- A hub page that links to multiple interactive scam/privacy simulations.
- Each simulation is a **single HTML page** (HTML + minimal JS/CSS), optimized for:
  - mobile + low-end hardware,
  - offline/patchy internet,
  - large buttons, clear prompts, and short sessions.

> These are **educational simulations**. They never perform real payments, logins, or data sharing.

---

## Quick start

**Open locally (recommended)**
1. Download or clone the repo.
2. Open `index.html` in a modern browser.  
   (You can also open any simulation HTML directly.)

**Serve statically (optional)**
```bash
# From the repo root
python -m http.server 8080
# visit http://localhost:8080
````

---

## Data & privacy

* Runs fully client-side; inputs remain in the browser.
* No collection of personal data; no third-party trackers.
* Some UI assets may load from public CDNs (CSS/JS only).
* Do **not** use real passwords/OTP/card numbers in workshops—use sample data.

---

## Using in classrooms / community drives

* Works with shared machines and low bandwidth.
* Clear “Reset/Clear” controls to wipe any local demo state between groups.
* Designed for 10–20 minute micro-sessions.
* Suitable for first-time internet users: minimal text, more interaction.

---

## Adding a new lab (scales without changing this README)

**Principles**

* Keep it **one self-contained HTML file**.
* No network calls that process personal data.
* Prefer Bootstrap (via CDN) or minimal CSS; avoid heavy frameworks.
* Use large, accessible controls; support keyboard and screen readers where possible.
* Add a short intro panel inside the page: *“What this teaches”* and *“Safety takeaways.”*

**Template (starter skeleton)**

```html
<!doctype html>
<html lang="en" data-bs-theme="light">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Digital Safety Lab — <Your Lab Title></title>
  <meta name="description" content="Educational simulation. No real payments/logins. Client-side only.">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.3/css/bootstrap.min.css" crossorigin="anonymous" referrerpolicy="no-referrer">
  <style>/* keep styles minimal; prefer utilities */</style>
</head>
<body class="container py-4">
  <header class="mb-4">
    <h1 class="h3">Digital Safety Lab — <Your Lab Title></h1>
    <p class="text-muted small">Simulation for education. No data is sent to any server.</p>
  </header>

  <main>
    <!-- Your interactive demo -->
  </main>

  <hr class="my-4">
  <section class="small">
    <strong>What this teaches:</strong> …  
    <strong>Safety takeaways:</strong> …  
    <button class="btn btn-outline-secondary btn-sm mt-2" onclick="localStorage.clear();sessionStorage.clear();location.reload()">Reset</button>
  </section>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.3/js/bootstrap.bundle.min.js" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
</body>
</html>
```

> The live hub automatically surfaces new labs from the `/digital-labs` directory—no README edits required.

---

## Contributing

We welcome improvements and new simulations.

1. Read the **[Contributing Guide](./CONTRIBUTING.md)** and **[Code of Conduct](./CODE_OF_CONDUCT.md)**.
2. Follow the **single-file** and **privacy-first** rules above.
3. Open a PR with:

   * a clear title and short summary,
   * screenshots or a short GIF (optional but helpful).

**Security issues:** please see our **[Security Policy](./SECURITY.md)** for responsible disclosure.

---

## License

Released under the **[MIT License](./LICENSE)**. Use, adapt, and teach freely. Just don't sue.

---

## Credits

Created and maintained by the **dmj.one** community to make cyber-safety education accessible, practical, and free.
