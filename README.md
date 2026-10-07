# Binance SAPI & C2C REST API Reference [![Binance SAPI Reference](https://img.shields.io/badge/Docs-Binance%20SAPI%20%26%20C2C-F0B90B?style=flat&logo=binance&logoColor=black)](https://github.com/pydevtop/binance-c2c-sapi-endpoints)

Fully indexed and structured developer reference for **Binance SAPI (Specialized API)** and **C2C / P2P endpoints**, based directly on official Binance REST API specifications with payload schemas, live examples, and Python integration guides.

🔗 **Explore Full Live Interactive Docs:** [https://py-dev.top/binance-api](https://py-dev.top/binance-api)

---

## 📌 Covered SAPI Modules & Endpoints

While standard Binance documentation primarily focuses on Spot and Futures markets, this repository structures and indexes comprehensive SAPI features hosted on [py-dev.top](https://py-dev.top/binance-api):

* **Binance C2C / P2P API**
  * Order chat automation & webhook message listeners
  * Pre-signed image upload URLs (`POST /sapi/v1/c2c/chat/image/pre-signed-url`)
  * Automated payment receipt delivery via WebSocket & binary upload
* **Capital & Fiat Operations**
  * Deposit & withdrawal records and address validation
  * Account snapshots, asset balances, and internal wallet transfers
* **Sub-Account & Margin Operations**

---

## 🚀 Quick Navigation

* **Interactive Developer Portal:** [https://py-dev.top/binance-api](https://py-dev.top/binance-api)
* **SAPI Overview & Endpoints:** [https://py-dev.top/binance-api/sapi](https://py-dev.top/binance-api/sapi)
* **C2C Chat & Order APIs:** [https://py-dev.top/binance-api/sapi/c2c](https://py-dev.top/binance-api/sapi/c2c)
* **Capital & Asset Management:** [https://py-dev.top/binance-api/sapi/capital](https://py-dev.top/binance-api/sapi/capital)
* **Python Automation Tutorials:** [https://py-dev.top/blog/crypto-exchange-development](https://py-dev.top/blog/crypto-exchange-development)

---
## 💻 Quick Python Example (Pre-Signed Upload Request)

```python
import requests

url = "https://api.binance.com/sapi/v1/c2c/chat/image/pre-signed-url"
headers = {
    "clientType": "WEB",
    "Content-Type": "application/json"
}
payload = {
    "imageName": "bank_receipt.jpg"
}

response = requests.post(url, headers=headers, json=payload)
print(response.json())
```




## 🔗 Related PyDev Ecosystem & Repositories

Explore our open-source bots, tools, and smart contracts for crypto trading and automation:

### 🤖 Binance P2P & C2C Automation
* [**binance-p2p-telegram-bot**](https://github.com/pydevtop/p2p-binance-telegram-bot) — Auto chat, order tracking & instant crypto release.
* [**binance-p2p-mpesa-payment-bot-kenya**](https://github.com/pydevtop/binance-p2p-mpesa-payment-bot-kenya) — M-PESA & Safaricom Daraja API payment automation for Kenyan P2P market.
* [**message-receipt-sending-binance-p2p-chat-websocket**](https://github.com/pydevtop/message-receipt-sending-binance-p2p-chat-websocket) — WebSocket receipt and payment notification sender for Binance P2P chat.
* [**p2p-trade-bot-binance**](https://github.com/pydevtop/p2p-trade-bot-binance) — Competitor price follower & dynamic ad repricing engine.
* [**binance-p2p-order-history-fetcher**](https://github.com/pydevtop/binance-p2p-order-history-fetcher) — Export and save P2P order histories including user counterparty details.
* [**binance_p2p_bot**](https://github.com/pydevtop/binance_p2p_bot) — Automated order purchasing bot for USDT and major crypto pairs.

### 📈 Trading & Arbitrage Systems
* [**bybit-signal-trading-bot**](https://github.com/pydevtop/bybit-signal-trading-bot) — Bybit Spot & Futures bot integrated with TradingView webhooks & risk management.
* [**interexchange-arbitrage-bot**](https://github.com/pydevtop/interexchange-arbitrage-bot) — Multi-exchange cryptocurrency arbitrage runner.

### ⛓️ DeFi & MEV Tools
* [**defi_staking_smart_contract**](https://github.com/pydevtop/defi_staking_smart_contract) — Production-ready Solidity ERC-20 staking contract.
* [**sending-bundles-flashbots**](https://github.com/pydevtop/sending-bundles-flashbots) — Python runner for constructing and submitting Flashbots bundles.
