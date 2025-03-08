# Testing Meta Lead Integration in OneLead

After setting up the **Meta App** and configuring **Meta Webhook Config** in OneLead, you should test whether your integration is working correctly. This guide covers **how to verify webhook connectivity**, **send a test lead**, and **troubleshoot common issues**.

---

## Verify Webhook Configuration

Before testing with a real lead, confirm that the [**Meta Webhook Config**](./setup.md) is properly set up.

---

## Sending a Test Lead Using Meta's Testing Tool

### **Step 1: Open Facebook Lead Ads Testing Tool**
1. Go to the [Facebook Lead Ads Testing Tool](https://developers.facebook.com/tools/lead-ads-testing).
2. Select your **Facebook Page** (the same one linked to your Meta Ads).
3. Choose the **Lead Form** that you want to test.
4. Click **Create Lead**.

### **Step 2: Check OneLead for Incoming Leads**
- Go to **OneLead > Meta Webhook Lead Logs**.
- Check if the lead log was received successfully.
- If leads are not appearing, check **Frappe Logs** or **Error Logs** for any errors.

---

## Testing with Curl (Manually Sending a Lead)

If you are running OneLead locally and want to manually send a test lead without using Facebook's Lead Ads Tool, use the following cURL command to simulate a webhook event.

```bash
curl -X POST http://{base_url}/api/method/onelead.utils.meta_lead.webhook \
-H "Content-Type: application/json" \
-d '{
  "entry": [{
    "id": "1635959026695683",
    "time": 1735291694,
    "changes": [{
      "value": {
        "adgroup_id": "120212669930254",
        "ad_id": "120212669955550254",
        "created_time": 1735291689,
        "leadgen_id": "56740452634061",
        "page_id": "1635959142565683",
        "form_id": "527829666666421",
        "field_data": [
          { "name": "full_name", "values": ["Test User"] },
          { "name": "email", "values": ["test@example.com"] },
          { "name": "phone_number", "values": ["+1234567890"] }
        ]
      },
      "field": "leadgen"
    }]
  }],
  "object": "page"
}'
```

### **What This Command Does**
- Sends a **test lead** to your Meta Webhook Lead Logs.
- if the page_id and form_id match in the **Meta Ads Page Config**, and form fields are mapped correctly, the lead will be **captured automatically**.

---

## Debugging Issues

### **1. Webhook Not Triggering?**
- Check if the **Webhook URL** is correctly set in the Meta App.
- Ensure the **Webhook Verify Token** matches what’s in **Meta Webhook Config**.
- check **Error Logs** in Frappe for any issues.

### **2. Lead Not Showing in your Lead doctype?**
- Confirm that the **Meta Ads Page Config** of a Page is mapped correctly to a **Lead Form** in question.
- check **Meta Lead Form** doctype to check the form is fetched.
- Click **"Populate Forms"** in **Meta Ads Page Config** to refresh the list of active forms.
- Ensure that **Page Flow is enabled** in Meta Webhook Config.

---

## Next Steps
- [Set Up Meta Ads Page Config](../features/meta_ads_page_config.md)
- [Troubleshooting Guide](../../troubleshooting/meta_webhook_issues.md)

For further assistance, check the [GitHub Issues](https://github.com/redsoftware-hq/onelead/issues).
