# MockHub — Spin Up Realistic Mock APIs in Minutes ⚡

MockHub lets developers create production-ready REST & SOAP mock APIs fast — complete with scenarios, dynamic variables, rate limits, stats, and optional authentication. Perfect for UI prototyping, integration testing, partner sandboxes, and demos.

<p align="center">
  <img src="https://mockhub.ovh/api-generator/images/logo_new.PNG" alt="MockHub" width="140" />
</p>

## 🚀 Highlights
- 🧪 **Real endpoints**: Hosted URLs you can call immediately.
- 🔁 **Scenario engine**: Status codes, delays, error rate, and alternate bodies.
- 📄 **OpenAPI import**: Parse a spec and auto-generate routes.
- 🧠 **AI assist**: Draft JSON bodies from short prompts.
- 🔒 **Auth options**: REST via Bearer; SOAP via `X-API-Key`.
- 📊 **Daily stats**: Per-endpoint aggregates and usage awareness.
- ♻️ **Auto‑extend expiry**: Active mocks keep working while you build.

## ✨ What You Can Build
- Frontend prototypes against stable contracts
- Integration tests with controlled failures
- Partner sandbox environments
- Demo backends for workshops

## 🧰 Feature Overview
- **REST mocks**
  - Methods: `GET`, `POST`
  - JSON body builder + required headers validation
  - Per‑endpoint scenarios (status, delay, error rate)
- **SOAP mocks (WSDL)**
  - Parse WSDL and generate operations automatically
  - Public router under `/soap/...` with optional API key protection
  - WSDL served at `/soap/<ServiceName>` (configurable)
- **Ownership & limits**
  - Free: up to 5 items; 40 calls/day
  - Premium: up to 100 items; 15,000 calls/day
- **Folders & sharing**
  - Group APIs with folders, share/import via one‑time codes

## 🖥️ Quick Start
1. Sign up and log in.
2. Create a REST mock via the generator.
3. Add a Scenario for failures or latency.
4. Call the endpoint from your app.
5. Scale with OpenAPI import or SOAP.

## 🔑 SOAP + API Keys
- Enable "Require Authorization header (API Key)" to protect operations.
- Generate a secure key once (visible, read‑only in UI), then call:

```bash
curl -X POST "https://mockhub.ovh/soap/Service/Operation_xyz" \
  -H "Content-Type: text/xml" \
  -H "X-API-Key: <YOUR_KEY>" \
  --data-binary @body.xml
```

## 📚 Learn More
- Guide: How to Create a Mock API (REST)
- Guide: Add & Switch Scenarios
- Guide: Generate Body with AI
- Guide: Create a SOAP API from WSDL

## 🏗️ Tech Stack
- **Backend**: Flask + SQLAlchemy, MySQL, Redis (limits), Firebase Admin
- **Frontend**: Static HTML/JS + Bootstrap; Nginx for prod
- **Infra**: Docker Compose

## 💬 Community & Support
- Join our Discord: https://discord.gg/mockhub
- Updates & announcements: https://mockhub.ovh/

---

Made with 💙 by developers, for developers.
