# 🛡️ Eco Proxy

### Secure Cloudflare Worker & AI Gateway for Ecological Telemetry

A high-performance **Cloudflare Worker** built in TypeScript that serves as a secure CORS proxy for the **[Movebank API](https://www.movebank.org/)** and an intelligent AI agent gateway powered by the **Groq API**.

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Cloudflare Workers](https://img.shields.io/badge/Cloudflare-Workers-F38020?logo=cloudflare&logoColor=white)](https://workers.cloudflare.com/)
[![Groq API](https://img.shields.io/badge/Groq_API-Enabled-F55036?style=flat&logo=groq&logoColor=white)](https://groq.com/)
[![Movebank API](https://img.shields.io/badge/Movebank-API_Live-2ea44f?style=flat&logo=databricks&logoColor=white)](https://www.movebank.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📌 About the Project

**Eco-Proxy** acts as the serverless middleware and security boundary for the ecological research infrastructure. It solves cross-origin resource sharing (CORS) limitations, securely injects authentication credentials for upstream scientific data sources and provides a natural language query parser using high-speed LLM inference.

---

## ✨ Key Features

- **Secure CORS Proxy:** Safely proxies direct-read requests to the official Movebank API, bypassing browser CORS restrictions.
- **Credential Management:** Securely injects Basic Authentication credentials for upstream scientific endpoints using Cloudflare environment secrets.
- **AI Agent Gateway:** Integrates with the Groq API to translate natural language prompts (e.g., _"find studies about white storks"_) into structured query parameters.
- **Edge Performance:** Deployed globally on Cloudflare's serverless edge infrastructure for minimal latency.

---

## 🛠️ Technology Stack

- **Runtime:** Cloudflare Workers (TypeScript, Fetch API)
- **AI & LLM:** Groq API (High-performance inference for natural language parsing)
- **External API:** Movebank Direct-Read Endpoint (`www.movebank.org`)

---

## 🚀 Getting Started & Deployment

### Prerequisites

- Node.js (v18+ recommended)
- Cloudflare Wrangler CLI (`npm install -g wrangler`)

### Local Development

1. Clone the repository:

```bash
   git clone git@github.com:wixhub/ecoproxy.git
   cd eco-proxy
```

2. Install dependencies:

```bash
   npm install
```

3. Run local development server:

```bash
   npm run dev
```

## Configuration & Deployment

1. Configure your environment secrets in Cloudflare:

```bash
npx wrangler secret put MOVEBANK_USERNAME
npx wrangler secret put MOVEBANK_PASSWORD
npx wrangler secret put GROQ_API_KEY
```

2. Deploy the worker to your Cloudflare account:

```bash
npm run deploy
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/wixhub/ecoproxy/issues).

## 📬 Contact & Support

Author: [@wixhub](https://github.com/wixhub)

Telegram: [@typeweb](https://t.me/typeweb)

GitHub Repository: [ecoproxy](https://github.com/wixhub/ecoproxy)

## 📄 License

This project is open-source and available under the [MIT License](./LICENSE).
