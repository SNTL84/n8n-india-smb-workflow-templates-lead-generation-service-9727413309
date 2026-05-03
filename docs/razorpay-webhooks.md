# Setting Up Razorpay Webhooks for n8n

## Step 1: Get Your n8n Webhook URL

1. In n8n, open the **Razorpay Payment Alert** workflow
2. Click the **Webhook** node
3. Copy the **Production URL** (e.g. `https://your-n8n.domain/webhook/razorpay-webhook`)

## Step 2: Configure in Razorpay Dashboard

1. Log in to [dashboard.razorpay.com](https://dashboard.razorpay.com)
2. Go to **Settings → Webhooks**
3. Click **+ Add New Webhook**
4. Paste your n8n webhook URL
5. Select events to subscribe:
   - `payment.captured` — Successful payment
   - `payment.failed` — Failed payment
   - `order.paid` — Order fully paid
   - `refund.created` — Refund initiated
6. Set a **Secret** (random string) — save this for webhook verification
7. Click **Create Webhook**

## Step 3: Verify Webhooks (Recommended)

Razorpay signs every webhook with your secret. To verify in n8n:

```javascript
// In a Code node before processing:
const crypto = require('crypto');
const signature = $input.all()[0].headers['x-razorpay-signature'];
const body = JSON.stringify($input.all()[0].json);
const expectedSig = crypto.createHmac('sha256', 'YOUR_WEBHOOK_SECRET').update(body).digest('hex');
if (signature !== expectedSig) throw new Error('Invalid Razorpay signature');
return $input.all();
```

## Step 4: Test

Use Razorpay's test mode: create a test payment → check your WhatsApp/Slack for the alert.

---
*Built by Milan · SNTL 84 · [desidevloper.com](https://desidevloper.com)*
