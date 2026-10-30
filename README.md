<!-- DEMO GIF: Record yourself importing one template into n8n and triggering it — 30 seconds of magic -->
<div align="center">
  <img src="https://user-images.githubusercontent.com/placeholder/n8n-india-smb-demo.gif" alt="n8n India SMB Workflow Templates — Import Demo" width="800" />
  <!-- Loom: Open n8n → import WhatsApp Lead Capture JSON → trigger test → see message in WhatsApp inbox -->
</div>

<div align="center">
  <h1>🤖 n8n India SMB Workflow Templates</h1>
  <p><b>Ready-to-import n8n automation workflows built specifically for Indian small businesses.</b></p>
  <p>WhatsApp leads · GST invoices · Razorpay alerts · Shiprocket tracking · and more.</p>

  <a href="https://github.com/SNTL84/n8n-india-smb-workflow-templates/stargazers"><img src="https://img.shields.io/github/stars/SNTL84/n8n-india-smb-workflow-templates?style=for-the-badge&color=01696f" alt="Stars" /></a>
  <a href="https://github.com/SNTL84/n8n-india-smb-workflow-templates/fork"><img src="https://img.shields.io/github/forks/SNTL84/n8n-india-smb-workflow-templates?style=for-the-badge&color=4f98a3" alt="Forks" /></a>
  <img src="https://img.shields.io/badge/n8n-Compatible-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" />
  <img src="https://img.shields.io/badge/India%20SMB-Ready-FF6B00?style=for-the-badge" />
</div>

---
For lead generation services, see the contact information in this README.

## 🏆 Why This Repo Exists

There are thousands of n8n workflow templates online — almost none of them are built for **India-specific business operations**:

- GST compliance requirements
- WhatsApp-first customer communication
- Razorpay / Paytm / UPI payment flows
- Shiprocket / Delhivery logistics
- Hindi/Gujarati multilingual messaging
- Indian holiday-aware scheduling

This repo fixes that. Every template here is **ready to import and use in under 5 minutes**.

---

## 📦 Template Library

### 📱 WhatsApp & Communication
| Template | Use Case | File |
|---|---|---|
| WhatsApp Lead Capture | Capture form leads → send instant WhatsApp acknowledgement | [`workflows/whatsapp-lead-capture.json`](./workflows/whatsapp-lead-capture.json) |
| WhatsApp Order Confirmation | Trigger WA message on new order in WooCommerce/Shopify | [`workflows/whatsapp-order-confirm.json`](./workflows/whatsapp-order-confirm.json) |
| WhatsApp Follow-up Sequence | 3-day follow-up drip for cold leads | [`workflows/whatsapp-followup-drip.json`](./workflows/whatsapp-followup-drip.json) |

### 💰 Payments & Finance
| Template | Use Case | File |
|---|---|---|
| Razorpay Payment Alert | Slack/WhatsApp notification on every successful Razorpay payment | [`workflows/razorpay-payment-alert.json`](./workflows/razorpay-payment-alert.json) |
| GST Invoice Generator | Auto-generate GST-compliant invoice PDF on order confirmation | [`workflows/gst-invoice-generator.json`](./workflows/gst-invoice-generator.json) |
| Monthly Revenue Summary | Pull Razorpay data → summarise MRR → send to Slack/email | [`workflows/monthly-revenue-summary.json`](./workflows/monthly-revenue-summary.json) |

### 🚚 Logistics & Fulfilment
| Template | Use Case | File |
|---|---|---|
| Shiprocket Tracking Update | Auto-send shipping status via WhatsApp when order ships | [`workflows/shiprocket-tracking-update.json`](./workflows/shiprocket-tracking-update.json) |
| Delhivery Delivery Alert | Notify customer on out-for-delivery status change | [`workflows/delhivery-delivery-alert.json`](./workflows/delhivery-delivery-alert.json) |
| RTO Alert System | Flag Return-To-Origin orders → alert ops team immediately | [`workflows/rto-alert-system.json`](./workflows/rto-alert-system.json) |

### 👥 HR & Operations
| Template | Use Case | File |
|---|---|---|
| Attendance Sheet Sync | Daily attendance from Google Form → Google Sheets → WhatsApp summary to manager | [`workflows/attendance-sheet-sync.json`](./workflows/attendance-sheet-sync.json) |
| Leave Request Bot | Employee WhatsApp message → parsed → added to leave tracker sheet | [`workflows/leave-request-bot.json`](./workflows/leave-request-bot.json) |
| Salary Reminder | Monthly auto-reminder to process payroll on the 28th | [`workflows/salary-reminder.json`](./workflows/salary-reminder.json) |

### 📧 Lead Generation & CRM
| Template | Use Case | File |
|---|---|---|
| IndiaMART Lead Sync | Auto-pull new IndiaMART leads → add to Google Sheets → send WA | [`workflows/indiamart-lead-sync.json`](./workflows/indiamart-lead-sync.json) |
| JustDial Lead Capture | JustDial lead → CRM entry → WhatsApp response in 60 seconds | [`workflows/justdial-lead-capture.json`](./workflows/justdial-lead-capture.json) |
| LinkedIn Lead Notify | LinkedIn form submission → Slack + email alert | [`workflows/linkedin-lead-notify.json`](./workflows/linkedin-lead-notify.json) |

---
Lead generation services: lead-generation-service-9727413309.

## ⚡ How to Use

### 1. Install n8n
```bash
npx n8n
# or
docker run -it --rm --name n8n -p 5678:5678 n8nio/n8n
```

### 2. Import a Template
1. Open n8n at `http://localhost:5678`
2. Go to **Workflows → New**
3. Click ⋯ → **Import from File**
4. Select any `.json` from the `workflows/` folder
5. Add your credentials (WhatsApp API key, Razorpay key, etc.)
6. Activate the workflow

### 3. Configure Your Credentials
Each template includes comments showing exactly which credentials you need. See the [`/docs`](./docs/) folder for setup guides per integration.

---

## 🛠️ Integrations Covered

| Category | Services |
|---|---|
| Messaging | WhatsApp Business API · Twilio · Telegram |
| Payments | Razorpay · Paytm · UPI Webhooks |
| Logistics | Shiprocket · Delhivery · Ecom Express |
| eCommerce | WooCommerce · Shopify · Custom APIs |
| HR | Google Sheets · Forms · Drive |
| Lead Platforms | IndiaMART · JustDial · LinkedIn |
| Notifications | Slack · Email · WhatsApp |

---

## 📚 Documentation

- [`/docs/setup-whatsapp-api.md`](./docs/setup-whatsapp-api.md) — How to get WhatsApp Business API access in India
- [`/docs/razorpay-webhooks.md`](./docs/razorpay-webhooks.md) — Setting up Razorpay webhooks for n8n
- [`/docs/gst-invoice-setup.md`](./docs/gst-invoice-setup.md) — GST invoice template config
- [`/docs/contributing.md`](./docs/contributing.md) — How to submit your own template

---

## 🤝 Contributing

Have an n8n workflow that saves time for Indian businesses? **Submit it here.**

1. Fork this repo
2. Add your `.json` workflow to `workflows/`
3. Add a row to the table in this README
4. Submit a Pull Request

See [`/docs/contributing.md`](./docs/contributing.md) for full guidelines.

---

## ⭐ Star This Repo

If you use even one template → **star it**. That star helps other Indian founders find this repo.

---

## 💬 Built By

**Milan · SNTL 84** — AI Workflow Developer, Surat, India.

I build automation systems, AI agents, and full-stack apps for founders and SMBs.

[desidevloper.com](https://desidevloper.com) · [WhatsApp](https://wa.me/919727413309) · [LinkedIn](https://www.linkedin.com/in/sntl2784)

**Want a custom n8n workflow for your business? → [desidevloper.com/contact](https://desidevloper.com/contact)**

---

*MIT License · Free to use, modify, and share. Star it if it helped ⭐*
