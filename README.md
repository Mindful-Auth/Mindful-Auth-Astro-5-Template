# Mindful Auth: Astro + Cloudflare D1 Starter

Edge-Native identity starter for Astro. Mindful Auth provides the identity logic and security layer, while you maintain 100% ownership of your user data in your own Cloudflare D1 database.

> **[Claim 1 of 20 Lifetime Beta Spots](https://share.tapeapp.com/ebfb35f7be514a288dece3d369bd7779)**

[![Setup Mindful Auth Authentication App with Astro & Cloudflare D1](https://img.youtube.com/vi/M0CGPNKiEiE/maxresdefault.jpg)](https://www.youtube.com/watch?v=M0CGPNKiEiE)

[Click to watch the full setup video on YouTube](https://www.youtube.com/watch?v=M0CGPNKiEiE)

## Why Mindful Auth?

Most auth providers hold your user data hostage and add significant latency to your stack. Mindful Auth is different:

- **100% Data Ownership:** Your users live in your D1 database. We never store your plain-text user data or "trap" your users in our dashboard.
- **Workers Native:** Optimized for the Cloudflare Workers runtime for maximum performance and future-proof architecture.
- **Zero Latency:** Authentication logic runs at the Edge, directly alongside your application code.
- **Privacy First:** Built on the "Mindful" principle. Only the data you choose to share leaves your infrastructure.
- **Bot Protection:** Native integration with Cloudflare Turnstile for seamless, invisible security.

## Quick Start

1) **[Create a Mindful Auth account](https://docs.mindfulauth.com/guides/mauth/setup/create-account/)** at [app.mindfulauth.com/register](https://app.mindfulauth.com/register).

2) **[Set up your Astro frontend](https://docs.mindfulauth.com/guides/frontend/astro/astro-overview/)** - Initialize your project using this template.

3) **[Get Turnstile credentials](https://docs.mindfulauth.com/guides/mauth/setup/turnstile/)** Add your Cloudflare Turnstile Site Key and Secret Key (required for bot protection).

4) **[Setup Email Webhooks](https://docs.mindfulauth.com/guides/mauth/setup/webhooks/)** - Use any email provider (Postmark, Resend) or automation tool (Make, n8n) to send verification emails and magic links. This template includes a pre-configured webhook handler for Postmark. [Read this guide here](https://docs.mindfulauth.com/guides/frontend/astro/astro-email-webhook/).

5) **[Setup D1 Tables](https://docs.mindfulauth.com/guides/backend/d1/d1-tables/)** - Run the required SQL commands in your Cloudflare D1 console to initialize the `members` and `audit_logs` tables.

*Note: Mindful Auth is backend agnostic and we can integrate any backend of your preference. Currently we support Cloudflare D1 and [Tape](https://docs.mindfulauth.com/guides/backend/tape/tape-template/)*

6) **[Onboard hostname](https://docs.mindfulauth.com/guides/mauth/setup/onboarding/)** - In your Mindful Auth dashboard, add the hostname where your Astro app will be deployed (e.g. `portal.myapp.com`).  

7) **[Get your INTERNAL_API_KEY](https://docs.mindfulauth.com/guides/mauth/setup/internal-api/)** - This key is required to authenticate your Astro frontend with the Mindful Auth API. For maximum security, never add this key to your .env file. Add it as an encrypted secret directly in your Cloudflare Workers dashboard or via the CLI.

> For full documentation, visit [https://docs.mindfulauth.com](https://docs.mindfulauth.com/)

## Mindful Auth Features

- **Astro 5.0+ Ready** - Leveraging the latest SSR and Middleware capabilities.
- **Fully Headless** - Total control over your UI. No "black-box" components or forced styling.
- **[Password Authentication](https://docs.mindfulauth.com/guides/mauth/options/password-auth/)** - traditional email + password login method where users create accounts with a password and verify their email via a secure link.
- **[Magic Link Authentication](https://docs.mindfulauth.com/guides/mauth/options/magic-login/)** - passwordless login method with up to four distinct security layers where users receive a secure link via email to log in.
- **[Two-Factor Authentication](https://docs.mindfulauth.com/guides/mauth/options/two-factor-auth/)** - add an extra layer of security to your authentication flow with TOTP-based 2FA.
- **[Audit Logs](https://docs.mindfulauth.com/guides/mauth/options/audit-logs/)** - track and monitor all authentication events for security and compliance purposes.
- **[Lock/Unlock Members on Demand](https://docs.mindfulauth.com/guides/mauth/api/lock-unlock/)** - perfect for handling suspicious activity or manual account management.
- **[Six Layer Defense System](https://docs.mindfulauth.com/guides/mauth/security/rate-limits/)** -  a comprehensive security system that includes rate limits, bot protection, and anomaly detection to safeguard your authentication flow from malicious actors.
- **[Per-Tenant Key Derivation](https://docs.mindfulauth.com/guides/mauth/security/tenant-key-derivation/)** - for maximum security in multi-tenant applications.
- **[Shared Security Layer](https://docs.mindfulauth.com/guides/mauth/security/shared-responsibility/)** - Mindful Auth secures the authentication layer (login, registration, password reset, 2FA, etc.) but does not store any member data. Your backend is responsible for securing member data.

## Limited Beta Offer

Mindful Auth is currently in beta. We are looking for 20 founding developers to help us stress-test the edge implementation and influence our roadmap. Founding members receive:

- Free Lifetime Access
- Direct access to the founder for integration support
- Influence over the upcoming feature roadmap

**[Apply for the Beta](https://share.tapeapp.com/ebfb35f7be514a288dece3d369bd7779)**

## Support

For support with this template, please reach out to the Mindful Auth team at [https://mindfulauth.com/contact](https://mindfulauth.com/contact) or [join our Discord community](https://discord.gg/vqXjBEyDvW).