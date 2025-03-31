# Meta Integration for OneLead

OneLead provides **seamless integration with Meta (Facebook) Lead Ads**, ensuring that leads from your Facebook and Instagram campaigns are instantly available in your CRM.

## How It Works

- **Captures leads** from Facebook Lead Forms via webhooks.
- **Maps leads** to internal CRM structures based on configurations.
- **Assigns leads** to users or teams automatically.
- **Tracks lead performance** through analytics.

## Key Setup Steps

1. **Register a Meta App** on the [Facebook Developer Portal](https://developers.facebook.com/).
2. **Configure Webhooks** to receive real-time lead data.
3. **Generate and validate User Access Tokens**.
4. **Map Meta Ad Pages and Forms** inside OneLead.

For a complete guide on **Meta Webhook Configuration**, go to [Meta Webhook Config](setup.md).

> **Note**
> If you're using the Meta integration **for your own business (one business account)**, you **do not need to submit your app for Meta App Review**. Just make sure the person setting it up:
> - Is the **Page Owner** or has **Ads Management access**, and
> - Has the appropriate role (Admin/Developer) on the Meta App.
>
> However, if you intend to make this integration available for **multiple businesses or third-party use**, Meta AppReview is required.
> ⚠️ As of now, OneLead’s current codebase **does not support multi-business integration**, so external use isn't supported yet.

## Next Steps
- [Meta App Setup](setup.md)
- [Meta Form Mapping](meta_form_mapping.md)
- [Meta Webhook Lead Logs](meta_webhook_lead_logs.md)
- [Meta Lead Testing](meta_lead_testing.md)
