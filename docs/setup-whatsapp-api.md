# How to Get WhatsApp Business API Access in India

This guide covers the fastest path to a working WhatsApp Business API for Indian SMBs using n8n.

## Option 1: Meta Cloud API (Free, Official)

1. Go to [developers.facebook.com](https://developers.facebook.com)
2. Create a Meta App → Select **Business** type
3. Add **WhatsApp** product
4. Go to **WhatsApp → Getting Started**
5. Use the test number to send your first message
6. To use your own number: **WhatsApp → Phone Numbers → Add Phone Number**
7. Copy your **Access Token** and **Phone Number ID**

## Option 2: Interakt / AiSensy (Easier for Non-Tech)

For Indian SMBs that want a managed WhatsApp API:
- [Interakt.shop](https://www.interakt.shop) — ₹999/month, popular in India
- [AiSensy](https://aisensy.com) — good for Shopify/WooCommerce

Both provide n8n-compatible webhooks and REST APIs.

## Setting Up in n8n

1. In n8n, go to **Credentials → New → WhatsApp**
2. Enter your **Access Token** and **Phone Number ID** from Meta
3. Test with a message to your own number
4. Import any template from `/workflows/` and connect this credential

## Required Message Templates

For business-initiated messages (not replies), WhatsApp requires pre-approved templates.
- Go to **Meta Business Suite → WhatsApp → Message Templates**
- Create templates for: order confirmation, payment alert, lead acknowledgement
- Templates are approved within 24 hours

---
*Built by Milan · SNTL 84 · [desidevloper.com](https://desidevloper.com)*
