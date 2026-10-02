# Lyra wallet backend, TESTNET

Backend of the Lyra browser extension (testnet build). Networks: Plasma Testnet, Ethereum Sepolia,
Base Sepolia, Polygon Amoy, Arc Testnet, Hyperliquid Testnet. Test coins only.

No secrets in this repository: keys are environment variables (see `.env.example` and `render.yaml`).

    npm install
    npm start        # listens on PORT (default 3001)

- Needs at least one AI provider key (OPENROUTER_API_KEY, MISTRAL_API_KEY or ANTHROPIC_API_KEY).
- No database and no MPC key: the 2-of-2 "Extra protection" is off on testnet, its routes are not loaded.
- Per-IP rate limits protect the AI keys: 20 chat requests/min, 240 other API requests/min.
- Health check: `GET /` returns `{"status":"ok"}`.
