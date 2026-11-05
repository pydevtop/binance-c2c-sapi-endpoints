# Referencia de Binance SAPI y C2C REST API

[![Referencia de Binance SAPI](https://img.shields.io/badge/Docs-Binance%20SAPI%20%26%20C2C-F0B90B?style=flat&logo=binance&logoColor=black)](https://github.com/pydevtop/binance-c2c-sapi-endpoints)

Portal de referencia para desarrolladores, completamente estructurado e indexado, sobre **Binance SAPI (API especializada)** y los **endpoints C2C / P2P**, basado en las especificaciones oficiales de la API REST de Binance. Incluye esquemas de datos, ejemplos prácticos y guías de integración con Python.

**Explora la documentación interactiva:** [https://py-dev.top/es/binance-api](https://py-dev.top/es/binance-api)

## 🌍 Documentación disponible

| Idioma | Documentación |
|--------|---------------|
| 🇺🇸 English | [README.md](README.md) |
| 🇪🇸 Español (LATAM) | [README_ES.md](README_ES.md) |

---

## Módulos y endpoints de SAPI incluidos

Mientras que la documentación estándar de Binance se enfoca principalmente en los mercados Spot y Futures, este repositorio organiza e indexa funcionalidades especializadas de SAPI disponibles en [PyDev Systems](https://py-dev.top/es/binance-api):

- **Binance C2C / P2P API**
  - Automatización del chat de órdenes y recepción de mensajes mediante webhooks.
  - URLs prefirmadas para subir imágenes (`POST /sapi/v1/c2c/chat/image/pre-signed-url`).
  - Envío automatizado de comprobantes de pago mediante WebSocket y carga de archivos binarios.

- **Operaciones de capital y fiat**
  - Historial de depósitos y retiros, y validación de direcciones.
  - Consultas del estado de cuenta, saldos de activos y transferencias internas entre billeteras.

- **Operaciones de subcuentas y margen**

---

## Navegación rápida

- **Portal interactivo para desarrolladores:** [https://py-dev.top/es/binance-api](https://py-dev.top/es/binance-api)
- **Descripción general y endpoints de SAPI:** [https://py-dev.top/es/binance-api/sapi](https://py-dev.top/es/binance-api/sapi)
- **API de chat y órdenes C2C:** [https://py-dev.top/es/binance-api/sapi/binance-sapi-c2c-api](https://py-dev.top/es/binance-api/sapi/binance-sapi-c2c-api)
- **Gestión de capital y activos:** [https://py-dev.top/es/binance-api/sapi/capital](https://py-dev.top/es/binance-api/sapi/capital)
- **Tutoriales de automatización con Python:** [https://py-dev.top/es/blog/crypto-exchange-development](https://py-dev.top/es/blog/crypto-exchange-development)

---

## Ejemplo rápido en Python (solicitud de URL prefirmada)

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

---

## Ecosistema PyDev y repositorios relacionados

Explora nuestros bots de código abierto, herramientas y contratos inteligentes para trading de criptomonedas y automatización.

### Automatización Binance P2P y C2C

- [**binance-p2p-telegram-bot**](https://github.com/pydevtop/p2p-binance-telegram-bot) — Automatización del chat, seguimiento de órdenes y liberación automática de criptomonedas.
- [**binance-p2p-mpesa-payment-bot-kenya**](https://github.com/pydevtop/binance-p2p-mpesa-payment-bot-kenya) — Automatización de pagos M-PESA mediante Safaricom Daraja API para el mercado P2P de Kenia.
- [**message-receipt-sending-binance-p2p-chat-websocket**](https://github.com/pydevtop/message-receipt-sending-binance-p2p-chat-websocket) — Envío de comprobantes y notificaciones de pago al chat P2P de Binance mediante WebSocket.
- [**p2p-trade-bot-binance**](https://github.com/pydevtop/p2p-trade-bot-binance) — Seguimiento de precios de competidores y ajuste dinámico de anuncios P2P.
- [**binance-p2p-order-history-fetcher**](https://github.com/pydevtop/binance-p2p-order-history-fetcher) — Exportación y almacenamiento del historial de órdenes P2P, incluidos los datos de las contrapartes.
- [**binance_p2p_bot**](https://github.com/pydevtop/binance_p2p_bot) — Bot de compra automatizada de órdenes de USDT y otros pares de criptomonedas.

### Sistemas de trading y arbitraje

- [**bybit-signal-trading-bot**](https://github.com/pydevtop/bybit-signal-trading-bot) — Bot para Spot y Futures de Bybit, integrado con webhooks de TradingView y herramientas de gestión de riesgos.
- [**interexchange-arbitrage-bot**](https://github.com/pydevtop/interexchange-arbitrage-bot) — Sistema de arbitraje de criptomonedas entre múltiples exchanges.

### Herramientas DeFi y MEV

- [**defi_staking_smart_contract**](https://github.com/pydevtop/defi_staking_smart_contract) — Contrato inteligente de staking ERC-20 desarrollado en Solidity.
- [**sending-bundles-flashbots**](https://github.com/pydevtop/sending-bundles-flashbots) — Herramienta en Python para construir y enviar bundles de transacciones mediante Flashbots.
