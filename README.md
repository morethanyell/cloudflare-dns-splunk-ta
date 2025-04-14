# Splunk Technology Add-on (TA) for Cloudflare DNS & Zones

## 📌 Overview

This Splunk Technology Add-on (TA) collects **Cloudflare Zones** and **DNS records** via the Cloudflare API and indexes them into Splunk under dedicated sourcetypes for easy searching, alerting, and dashboarding.

It’s designed for environments where you need real-time or scheduled visibility into your Cloudflare domain configurations — directly from the source.

---

## 🔐 Requirements

- A **Cloudflare API Bearer Token** with **Zone** and **DNS read permissions**.

**Minimum Required API Scopes:**
- `Zone:Read`
- `DNS:Read`

You can generate this token via your Cloudflare dashboard under **My Profile > API Tokens**.

---

## 🎯 What This TA Does

1. **Collects all available Cloudflare Zones**  
   - Retrieves all zones (domains) accessible by the provided API token.
   - Indexes these into Splunk with the sourcetype: `cloudflare:zone`.

2. **Collects all DNS records for each Zone**  
   - Loops through the list of Zones.
   - Fetches all DNS records within each zone.
   - Indexes these into Splunk with the sourcetype: `cloudflare:dns`.

Both collections handle pagination automatically to ensure no records are missed.

---

## 🗄️ Indexed Sourcetypes

| Sourcetype       | Description                          |
|:----------------|:--------------------------------------|
| `cloudflare:zone` | Metadata and configuration of Zones   |
| `cloudflare:dns`  | DNS records for each Zone             |

---

## 🚀 Installation

1. Install this TA on your **Heavy Forwarder**, **Search Head**, or **Indexer** (as appropriate for your Splunk architecture).
2. Configure your Cloudflare **Bearer Token** in the TA’s configuration page.
3. Set up inputs and schedule collections as needed.

---

## 📖 Example Use Cases

- Monitor DNS records for unauthorized changes.
- Track new Zones added to your Cloudflare account.
- Build dashboards showing your Cloudflare DNS infrastructure.
- Alert on unexpected or risky DNS entries.

---

## 📜 License

MIT License — open to the world.

---

## 🤝 Contributing

Pull requests and issue reports are welcome. Let’s make this better together.

---

## ✨ Beer donations accepted by

daniel.l.astillero@gmail.com

