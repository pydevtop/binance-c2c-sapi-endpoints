# Binance SAPI & C2C REST API Reference

Fully indexed and structured developer reference for **Binance SAPI (Specialized API)** and **C2C / P2P endpoints**, based directly on official Binance REST API specifications with payload schemas, live examples, and Python integration guides.

🔗 **Explore Full Live Interactive Docs:** [https://py-dev.top/binance-api/](https://py-dev.top/binance-api/)

---

## 📌 Covered SAPI Modules & Endpoints

While standard Binance documentation primarily focuses on Spot and Futures markets, this repository structures and indexes comprehensive SAPI features hosted on [py-dev.top](https://py-dev.top/binance-api/):

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

* **Interactive Developer Portal:** [https://py-dev.top/binance-api/](https://py-dev.top/binance-api/)
* **SAPI Overview & Endpoints:** [https://py-dev.top/binance-api/sapi/](https://py-dev.top/binance-api/sapi/)
* **C2C Chat & Order APIs:** [https://py-dev.top/binance-api/sapi/c2c/](https://py-dev.top/binance-api/sapi/c2c/)
* **Capital & Asset Management:** [https://py-dev.top/binance-api/sapi/capital/](https://py-dev.top/binance-api/sapi/capital/)
* **Python Automation Tutorials:** [https://py-dev.top/blog/crypto-exchange-development/](https://py-dev.top/blog/crypto-exchange-development/)

---

## 💻 Quick Python Example (Pre-Signed Upload Request)

```python
import requests

url = "[https://api.binance.com/sapi/v1/c2c/chat/image/pre-signed-url](https://api.binance.com/sapi/v1/c2c/chat/image/pre-signed-url)"
headers = {
    "clientType": "WEB",
    "Content-Type": "application/json"
}
payload = {
    "imageName": "bank_receipt.jpg"
}

response = requests.post(url, headers=headers, json=payload)
print(response.json())
