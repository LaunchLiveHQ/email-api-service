# Email Api Service

A comprehensive guide and comparison of popular email API services, developer platforms, and transactional delivery engines—including their features, protocol support, and free tier allowances.

---

## 📊 Quick Comparison Table

| Service | Free Tier Volume | Daily Cap | CC Required? | Protocols / Delivery | Best For |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[Resend](#1-resend)** | 3,000 emails / month | 100 emails / day | No | REST API, SMTP, React Email | Modern React/Next.js apps & developers |
| **[Postmark](#2-postmark)** | 100 emails / month | None | No | REST API, SMTP, Webhooks | Gold-standard transactional deliverability |
| **[SendGrid](#3-sendgrid)** | 100 emails / day (~3,000/mo) | 100 emails / day | No | REST API, SMTP, Webhooks | Enterprise scale & proven infrastructure |
| **[AWS SES](#4-aws-ses)** | 3,000 emails / month (12 mos) | Account sandbox | Yes (AWS Account) | REST API, SMTP, SDKs | Ultra low-cost high-volume sending |
| **[Mailgun](#5-mailgun)** | 5,000 emails (30-day trial) | Trial limit | Yes (Post-trial) | REST API, SMTP, Webhooks | Powerful inbound routing & deliverability |
| **[Brevo](#6-brevo)** | 300 emails / day (~9,000/mo) | 300 emails / day | No | REST API, SMTP, Webhooks | Highest permanent daily free volume |
| **[MailerSend](#7-mailersend)** | 3,000 emails / month | Account limits | No | REST API, SMTP, Webhooks | Affordable transactional & SMS APIs |
| **[SparkPost](#8-sparkpost)** | 500 emails / month (Test) | None | No | REST API, SMTP | Predictive deliverability & enterprise analytics |
| **[Mailchimp](#9-mailchimp)** | 1,000 sends / month (500 contacts) | 500 sends / day | No | REST API (Marketing), Mandrill Demo | Marketing newsletters & e-commerce |
| **[Iterable](#10-iterable)** | Demo / Sandbox upon request | N/A | Contact Sales | REST API, Webhooks | Omni-channel enterprise lifecycle marketing |
| **[Loops](#11-loops)** | 2,000 emails / mo (1,000 contacts) | None | No | REST API, Webhooks, React components | SaaS onboarding & product-led email |
| **[Plunk](#12-plunk)** | 3,000 emails / month | None | No | REST API, SMTP, Open-source self-host | Open-source AWS SES wrapper & privacy |
| **[Mailtrap](#13-mailtrap)** | 1,000 sends / mo + 100 testing | None | No | REST API, SMTP | Dual testing sandbox + transactional delivery |
| **[Cloudflare](#14-cloudflare)** | Unlimited inbound + 3k/mo outbound | Scaled daily quota | No | Workers binding (`env.EMAIL`), REST API, SMTP | Serverless edge delivery & inbound routing |
| **[Unosend](#15-unosend)** | Up to 5,000 emails / month | None | No | REST API, SMTP | Credit-based pay-as-you-go transactional |
| **[Scaleway](#16-scaleway)** | 300 emails / month | None | Yes (Scaleway Console) | REST API, SMTP | European sovereign cloud infrastructure |
| **[ZeptoMail](#17-zeptomail)** | 10,000 email credits (on signup) | None | No | REST API, SMTP, Webhooks | Pure transactional email by Zoho |
| **[MailPace](#18-mailpace)** | 100 emails / month | None | No | REST API, SMTP, Webhooks | Lightweight, carbon-conscious, no spam |
| **[Sequenzy](#19-sequenzy)** | Free trial / 500 contacts | None | No | REST API, Webhooks, AI builder | Automated SaaS revenue & onboarding flows |
| **[JetEmail](#20-jetemail)** | Developer free tier / trial credits | None | No | REST API, SMTP, Anycast Network | Independent low-latency delivery network |
| **[Lettermint](#21-lettermint)** | 1,000 emails / month | None | No | REST API, SMTP | 100% EU-hosted & GDPR compliant delivery |
| **[Lettr](#22-lettr)** | Free tier (up to 500 subscribers) | None | No | REST API, Drag & Drop Editor | Unified transactional + marketing for indie SaaS |
| **[Primitive](#23-primitive)** | Developer sandbox / Agent tier | None | No | REST API, Webhooks, Programmatic Inboxes | Email infrastructure built for AI agents |
| **[useSend](#24-usesend)** | 3,000 emails / month | None | No | REST API, SMTP, Open-source self-host | Open-source email platform & self-hosting |
| **[SendPulse](#25-sendpulse)** | 12,000 emails / month | 400 emails / day | No | REST API, SMTP, Webhooks | Generous permanent transactional free tier |
| **[EmailOctopus](#26-emailoctopus)** | 10,000 emails / mo (2,500 contacts) | None | No | REST API, Webhooks | High-volume marketing campaigns & automations |
| **[Mailjet](#27-mailjet)** | 6,000 emails / month | 200 emails / day | No | REST API, SMTP, Webhooks | European deliverability & multi-language SDKs |
| **[Elastic Email](#28-elastic-email)** | 3,000 emails / month | 100 emails / day | No | REST API, SMTP, Webhooks | Cost-effective transactional & marketing APIs |
| **[SMTP2GO](#29-smtp2go)** | 1,000 emails / month | 200 emails / day | No | REST API, SMTP | Highly reliable SMTP relay with reporting |
| **[AhaSend](#30-ahasend)** | 1,000 emails / month | None | No | REST API, SMTP, CLI | Developer-first European transactional email |
| **[EmailJS](#31-emailjs)** | 200 emails / month | None | No | Client SDKs (JS/React/Vue/Flutter) | Serverless frontend email sending without backend |
| **[Forward Email](#32-forward-email)** | Unlimited inbound / Paid SMTP | None | No | REST API, DNS Routing, SMTP | Privacy-first open-source domain forwarding |
| **[Novu](#33-novu)** | 30,000 events / month | None | No | REST API, Multi-channel SDKs | Open-source notification infrastructure |
| **[Courier](#34-courier)** | 10,000 notifications / month | None | No | REST API, Webhooks, Routing rules | Unified multi-channel routing & template engine |
| **[Postal](#35-postal)** | Unlimited (Open Source Self-Hosted) | None | No | REST API, SMTP, Webhooks | Full self-hosted delivery platform (SendGrid alt) |
| **[Listmonk](#36-listmonk)** | Unlimited (Open Source Self-Hosted) | None | No | REST API, Webhooks | High-performance self-hosted newsletter/mail manager |

---

## 📚 Service Breakdown & Free Tier Details

---

### 1. Resend
* **Overview**: A developer-first email platform built around React Email, modern TypeScript SDKs, and clean UI/DX. It allows developers to build emails as React components and send them via a sleek REST API.
* **Free Tier Allowance**:
  * **3,000 emails / month**
  * **100 emails / day** limit
  * **1 custom sending domain**
  * 1 API key, 3 days of log retention
* **Credit Card Required**: No
* **Key Features**: First-class `@react-email` integration, Next.js / Vercel friendly, webhooks, analytics, SMTP relay, DKIM/SPF auto-validation.
* **Website**: [resend.com](https://resend.com)

---

### 2. Postmark
* **Overview**: Renowned for market-leading deliverability and speed. Postmark strictly separates transactional emails from marketing broadcasts to guarantee instant inbox placement for password resets, receipts, and 2FA codes.
* **Free Tier Allowance**:
  * **100 emails / month** (Developer Plan forever free)
  * Send to any recipient, full access to developer tools and REST API
  * Unlimited server setups and domains
* **Credit Card Required**: No
* **Key Features**: Sub-second delivery times, detailed 45-day message history, inbound email webhooks and parsing, transactional template builder, message streams.
* **Website**: [postmarkapp.com](https://postmarkapp.com)

---

### 3. SendGrid (Twilio SendGrid)
* **Overview**: One of the industry’s largest and most established email delivery platforms, capable of handling hundreds of billions of emails per month for startups and global enterprises alike.
* **Free Tier Allowance**:
  * **100 emails / day** forever (~3,000 emails / month)
  * Includes core sending features, analytics, and SMTP relay
* **Credit Card Required**: No
* **Key Features**: Robust REST API v3, SMTP relay, dynamic transactional templates with Handlebars, email validation, subuser management, comprehensive webhooks.
* **Website**: [sendgrid.com](https://sendgrid.com)

---

### 4. AWS SES (Simple Email Service)
* **Overview**: Amazon Web Services’ hyper-scalable, cost-efficient bulk and transactional email infrastructure.
* **Free Tier Allowance**:
  * **3,000 messages / month free** for the first 12 months (via AWS Free Tier).
  * *Note*: Starts in the AWS SES Sandbox (can only send to verified emails/domains until production access is requested and approved).
* **Credit Card Required**: Yes (Valid AWS account)
* **Key Features**: Industry-lowest pricing ($0.10 per 1,000 emails after free tier), dedicated IP pools, Virtual Deliverability Manager (VDM), native integration with IAM, CloudWatch, S3, and SNS.
* **Website**: [aws.amazon.com/ses](https://aws.amazon.com/ses)

---

### 5. Mailgun (Sinchem)
* **Overview**: Powerful, developer-centric email API known for sophisticated inbound email routing, advanced parsing, and automated IP reputation management.
* **Free Tier Allowance**:
  * **5,000 free emails** during a 30-day trial period.
  * Sandbox domain for testing without domain verification; standard pay-as-you-go Flex plan after trial.
* **Credit Card Required**: Required for production domains and post-trial pay-as-you-go.
* **Key Features**: Inbound email parsing to JSON, email address verification API, send-time optimization, detailed deliverability logs, robust Python/Node/Go/PHP SDKs.
* **Website**: [mailgun.com](https://mailgun.com)

---

### 6. Brevo (formerly Sendinblue)
* **Overview**: An all-in-one marketing and transactional communication platform based in Europe, offering email, SMS, WhatsApp, and CRM.
* **Free Tier Allowance**:
  * **300 emails / day** (~9,000 emails / month) forever
  * Unlimited contact storage
  * *Note*: Free emails include a discreet Brevo logo in the footer.
* **Credit Card Required**: No
* **Key Features**: High daily sending allowance, transactional SMTP + REST API, visual drag-and-drop template designer, marketing automation workflows, GDPR compliant.
* **Website**: [brevo.com](https://brevo.com)

---

### 7. MailerSend
* **Overview**: Built by the creators of MailerLite, MailerSend is focused specifically on transactional messaging (email, SMS, and inbound webhooks) with intuitive developer tooling.
* **Free Tier Allowance**:
  * **3,000 emails / month**
  * 1 verified custom domain
  * Basic email verification (100 checks)
* **Credit Card Required**: No
* **Key Features**: Drag-and-drop / HTML / Markdown email builders, webhooks, multi-user accounts, IP reputation monitoring, tracking for opens and clicks.
* **Website**: [mailersend.com](https://mailersend.com)

---

### 8. SparkPost (MessageBird / Bird)
* **Overview**: Enterprise-grade email delivery service that powers major tech platforms, offering deep predictive delivery analytics and ISP optimization.
* **Free Tier Allowance**:
  * **Developer / Test Account**: 500 emails / month free (or 15,000 emails over 30 days during introductory trials).
* **Credit Card Required**: No (for developer test sandbox)
* **Key Features**: Signals analytics (predictive bounce and spam diagnostics), adaptive email delivery, REST API, SMTP relay, sub-accounts.
* **Website**: [sparkpost.com](https://sparkpost.com)

---

### 9. Mailchimp (Intuit Mailchimp & Mandrill)
* **Overview**: The gold standard for marketing campaigns, newsletters, and audience automation. Mandrill is Mailchimp’s transactional email add-on.
* **Free Tier Allowance**:
  * **Mailchimp Free**: 500 contacts, 1,000 sends / month (daily cap of 500 sends).
  * **Mandrill (Transactional)**: Demo mode included with 500 free test sends to verified domains (requires a paid Mailchimp plan for full production transactional use).
* **Credit Card Required**: No (for Free Marketing tier)
* **Key Features**: Drag-and-drop email designer, campaign automation, forms and landing pages, behavioral targeting, audience segmentation.
* **Website**: [mailchimp.com](https://mailchimp.com)

---

### 10. Iterable
* **Overview**: Enterprise cross-channel customer engagement platform for unifying email, SMS, push notifications, and in-app messages.
* **Free Tier Allowance**:
  * **No public self-service free tier**.
  * Developer sandboxes and demo environments are provisioned via enterprise sales and solution architects.
* **Credit Card Required**: Enterprise sales / contract-based
* **Key Features**: Massive scale, AI-driven journey optimization, omni-channel orchestration, deeply configurable audience segmentation and webhook pipelines.
* **Website**: [iterable.com](https://iterable.com)

---

### 11. Loops
* **Overview**: The modern email platform built specifically for SaaS companies. It bridges transactional notifications with product-led email sequences and newsletters.
* **Free Tier Allowance**:
  * **Up to 1,000 contacts**
  * **2,000 emails / month**
  * Full access to API, forms, and visual journey builder
* **Credit Card Required**: No
* **Key Features**: React Email component support, Notion-like clean writing interface, Stripe & Segment integrations, event-triggered user journeys.
* **Website**: [loops.so](https://loops.so)

---

### 12. Plunk
* **Overview**: An open-source, developer-friendly email platform built on top of AWS SES. Plunk provides an intuitive API, marketing journeys, and self-hosting capabilities without enterprise markup.
* **Free Tier Allowance**:
  * **Plunk Cloud**: **3,000 emails / month** free
  * **Self-Hosted**: Unlimited (connect your own AWS SES account)
* **Credit Card Required**: No
* **Key Features**: Open-source core, instant setup, single API key for transactional and marketing, event-driven automations, modern developer dashboard.
* **Website**: [useplunk.com](https://useplunk.com)

---

### 13. Mailtrap
* **Overview**: An all-in-one email platform providing both an isolated **Email Sandbox** (to inspect, debug, and preview emails safely before staging/prod) and a high-deliverability **Email Sending** service.
* **Free Tier Allowance**:
  * **Email Sending**: **1,000 emails / month**
  * **Email Testing (Sandbox)**: **100 test emails / month**, 1 inbox, 5MB inbox size
* **Credit Card Required**: No
* **Key Features**: HTML/CSS validation, spam score analysis, preview across desktop & mobile clients, REST API, SMTP relay, quick SDK integrations (Node, Python, Ruby, PHP).
* **Website**: [mailtrap.io](https://mailtrap.io)

---

### 14. Cloudflare (Cloudflare Email Service - Sending & Routing)
* **Overview**: Cloudflare's full email solution uniting **Email Routing** (inbound management) and the newly introduced **Email Sending** service (outbound transactional delivery). It allows developers to send emails directly via a Cloudflare Workers binding (`env.EMAIL.send`), a standard REST API (`api.cloudflare.com/client/v4/accounts/{account_id}/email/sending/send`), or traditional authenticated SMTP relay (`smtps://smtp.mx.cloudflare.net:465`).
* **Free Tier Allowance Need to be on Paid Workers Plan**:
  * **Email Routing (Inbound)**: **100% Free & unlimited** custom email address forwarding to destination inboxes and Workers.
  * **Email Sending (Outbound)**: Includes **3,000 emails / month** on Workers plans (with overage at $0.35 per 1,000 emails).
  * **Free Sends to Verified Destinations**: Sending to verified destination addresses is **always free** and does not count toward monthly quotas or daily limits.
  * **Daily Quota**: Starts with a conservative daily sending allowance that automatically scales upward with sending reputation and deliverability metrics.
* **Credit Card Required**: No (for free DNS/Routing; standard Workers account for outbound sending)
* **Key Features**: 
  * Three delivery protocols: Cloudflare Workers binding (`env.EMAIL.send(...)`), REST API, and SMTP relay (`smtps://smtp.mx.cloudflare.net:465`).
  * Automated DNS onboarding (`cf-bounce` subdomain configuration for MX, SPF, DKIM, and DMARC).
  * Native serverless edge execution with zero third-party dependencies.
  * Supports attachments up to 5 MiB (up to 25 MiB when sending to verified destination addresses) and 50 recipients per email.
* **Documentation & Quickstart**: [Cloudflare Email Service - Send Emails](https://developers.cloudflare.com/email-service/get-started/send-emails/)
* **Website**: [developers.cloudflare.com/email-service](https://developers.cloudflare.com/email-service/)

---

### 15. Unosend
* **Overview**: A modern, streamlined transactional email API designed with transparent, credit-based pay-as-you-go pricing rather than costly monthly subscriptions.
* **Free Tier Allowance**:
  * **Up to 5,000 emails / month** (or 3,000 free starter credits upon signup).
  * Pay-as-you-go top-ups ($4 per 10,000 emails thereafter).
* **Credit Card Required**: No
* **Key Features**: REST API, SMTP relay, pay-as-you-go credit model (no recurring monthly fees), dedicated IP options, webhook event listeners.
* **Website**: [unosend.co](https://unosend.co)

---

### 16. Scaleway (Scaleway Transactional Email - TEM)
* **Overview**: European cloud infrastructure provider offering a high-performance, GDPR-first transactional email API (TEM) hosted strictly in EU data centers (Paris/Amsterdam/Warsaw).
* **Free Tier Allowance**:
  * **300 free emails / month** forever
  * Very cost-effective pricing thereafter (€0.25 per 1,000 emails)
* **Credit Card Required**: Yes (Scaleway cloud console account)
* **Key Features**: European data sovereignty, SPF/DKIM validation, REST API, SMTP relay, real-time analytics, automated bounce management.
* **Website**: [scaleway.com](https://www.scaleway.com/en/transactional-email-tem/)

---

### 17. ZeptoMail (Zoho)
* **Overview**: Zoho's dedicated transactional email delivery platform, engineered to separate mission-critical notifications from bulk marketing newsletters to preserve pristine IP reputation.
* **Free Tier Allowance**:
  * **10,000 free email credits** on account creation / trial
  * Credits never expire until fully consumed; pay-as-you-go credit packs thereafter ($2.50 per 10,000 emails).
* **Credit Card Required**: No
* **Key Features**: Strict transactional-only policy (no marketing spam allowed), automated DKIM/SPF alignment, REST API, SMTP relay, sub-account segregation.
* **Website**: [zoho.com/zeptomail](https://www.zoho.com/zeptomail/)

---

### 18. MailPace (formerly OhMySMTP)
* **Overview**: A lightweight, fast, and privacy-focused transactional email API built with sustainability and eco-friendliness in mind (runs on green energy).
* **Free Tier Allowance**:
  * **100 emails / month** forever on the Free Developer Plan
  * Full API and SMTP access with no credit card
* **Credit Card Required**: No
* **Key Features**: No marketing email permitted (transactional only), sub-second delivery, 100% green-energy hosted, REST API, SMTP server, zero tracking bloat.
* **Website**: [mailpace.com](https://mailpace.com)

---

### 19. Sequenzy
* **Overview**: An AI-powered email marketing and lifecycle automation platform for SaaS founders and product teams, turning customer product events into tailored onboarding and retention sequences.
* **Free Tier Allowance**:
  * **Free trial / Free Starter Tier** for up to **500 subscribers**
  * Automated sequence builder and product event ingestion
* **Credit Card Required**: No
* **Key Features**: Event-based triggers, AI sequence assistant, Stripe integration for dunning and churn prevention, developer-friendly event API.
* **Website**: [sequenzy.com](https://sequenzy.com)

---

### 20. JetEmail
* **Overview**: A robust, independent transactional delivery platform featuring its own anycast network, managed IP pools, and inbound filtering engines for developers and agencies.
* **Free Tier Allowance**:
  * **Developer Free Tier / Trial Allowance** for prototyping and testing delivery pipelines.
* **Credit Card Required**: No (for developer testing)
* **Key Features**: Global anycast network for ultra-low latency sending, high-reputation IP pools, REST API, SMTP relay, real-time bounce processing.
* **Website**: [jetemail.com](https://jetemail.com)

---

### 21. Lettermint
* **Overview**: An independent European transactional email delivery service focused on strict data residency, privacy, and full GDPR compliance. All data and servers are 100% within the EU.
* **Free Tier Allowance**:
  * **1,000 free emails / month** on the developer tier
  * Full access to API, SMTP, and SDKs
* **Credit Card Required**: No
* **Key Features**: 100% EU infrastructure (no US cloud dependencies), GDPR compliance, SDKs for Node.js, PHP, Laravel, Python, and Go, real-time delivery logs.
* **Website**: [lettermint.co](https://lettermint.co)

---

### 22. Lettr
* **Overview**: A unified email platform designed for indie hackers, artisans, and SaaS developers who want to manage transactional emails and marketing broadcasts from a single clean interface.
* **Free Tier Allowance**:
  * **Free starter tier** (up to **500 subscribers / sends**)
  * Includes both API access and drag-and-drop campaign editor
* **Credit Card Required**: No
* **Key Features**: Visual drag-and-drop template designer (Topol.io engine), native Laravel package, inbound email parsing, unified transactional + newsletter dashboard.
* **Website**: [lettr.com](https://lettr.com)

---

### 23. Primitive (primitive.dev)
* **Overview**: An email infrastructure platform engineered specifically for **AI agents**. Rather than viewing email merely as an outbound pipe, Primitive treats the "inbox" as a programmable primitive for machine-to-machine workflows.
* **Free Tier Allowance**:
  * **Developer Sandbox / Free Tier** for agent testing and prototyping programmatic inboxes.
* **Credit Card Required**: No
* **Key Features**: Programmable inboxes, automated agent threads, inbound parsing, JavaScript runtime hooks on incoming messages, agentic memory & reply handling.
* **Website**: [primitive.dev](https://primitive.dev)

---

### 24. useSend
* **Overview**: An open-source, developer-friendly email platform built for modern product teams. It provides flexible deployment—either through a managed cloud service or by self-hosting on your own VPS or Docker setup connected to cost-effective infrastructure like AWS SES.
* **Free Tier Allowance**:
  * **useSend Cloud**: **3,000 emails / month** free on the managed cloud platform.
  * **Self-Hosted**: **Unlimited** sends (the core application is open-source and free; you only pay raw provider/infrastructure costs such as AWS SES at $0.10 / 1,000 emails).
* **Credit Card Required**: No
* **Key Features**: Visual drag-and-drop email builder, contact management & audience segmentation, suppression lists, real-time deliverability tracking (opens, clicks, bounces), REST API, and SMTP relay.
* **Website**: [usesend.com](https://usesend.com/)

---

### 25. SendPulse
* **Overview**: A multi-channel marketing and messaging platform featuring an exceptionally generous, dedicated transactional SMTP server and REST API for developers.
* **Free Tier Allowance**:
  * **12,000 emails / month** free for transactional SMTP/API
  * **400 emails / day** cap
  * Full access to SMTP relay and REST API
* **Credit Card Required**: No
* **Key Features**: High-volume transactional sending, SPF/DKIM authentication, detailed delivery logs, unsubscribe link management, webhooks for delivery events.
* **Website**: [sendpulse.com](https://sendpulse.com/features/smtp)

---

### 26. EmailOctopus
* **Overview**: A developer- and creator-friendly email marketing platform designed to be a lightweight, affordable alternative to Mailchimp with high-capacity free sending.
* **Free Tier Allowance**:
  * **10,000 emails / month** free forever
  * Up to **2,500 subscribers**
  * Includes landing pages and automated drip sequences
* **Credit Card Required**: No
* **Key Features**: REST API, campaign automation workflows, custom domain forms, tag-based segmentation, clean visual builder (includes discreet branding on free tier).
* **Website**: [emailoctopus.com](https://emailoctopus.com)

---

### 27. Mailjet (Sinch Mailjet)
* **Overview**: A long-standing European cloud email service provider (part of the Sinch communications group) offering unified marketing campaigns, transactional APIs, and SMTP relay.
* **Free Tier Allowance**:
  * **6,000 emails / month** free forever
  * **200 emails / day** sending cap
  * Up to 1,000 contacts
* **Credit Card Required**: No
* **Key Features**: Robust REST API, SMTP relay, multi-language SDKs (Python, Node, PHP, Go, Java, Ruby), Passport email designer, GDPR-compliant infrastructure.
* **Website**: [mailjet.com](https://www.mailjet.com)

---

### 28. Elastic Email
* **Overview**: A fast, cost-efficient email platform offering both an Email API for developers and a visual email marketing suite, powered by its own delivery infrastructure.
* **Free Tier Allowance**:
  * **3,000 emails / month** free
  * **100 emails / day** cap
  * Up to 1,000 contacts
* **Credit Card Required**: No
* **Key Features**: REST API, SMTP relay, sub-accounts, activity logs (3-day retention), template editor, contact management, webhooks.
* **Website**: [elasticemail.com](https://elasticemail.com)

---

### 29. SMTP2GO
* **Overview**: An enterprise-grade, highly dependable worldwide SMTP relay and API provider, famous for its real-time analytics, spam-trap monitoring, and ease of setup.
* **Free Tier Allowance**:
  * **1,000 emails / month** free forever
  * **200 emails / day** cap (25/hr for unverified domains, lifted upon verification)
  * 5 days of reporting and tracking history
* **Credit Card Required**: No
* **Key Features**: Real-time spam-trap detection, automated bounce & unsubscribe handling, REST API, global anycast SMTP network, multiple sending sub-users.
* **Website**: [smtp2go.com](https://www.smtp2go.com)

---

### 30. AhaSend
* **Overview**: A modern, developer-centric European transactional email API engineered for developers building MVPs, apps, and SaaS who prioritize simplicity and data privacy.
* **Free Tier Allowance**:
  * **1,000 emails / month** free forever
  * Full access to API, SMTP, and CLI tooling
* **Credit Card Required**: No
* **Key Features**: Developer CLI, REST API, SMTP relay, sub-accounts for staging/production segregation, EU data hosting, real-time event webhooks.
* **Website**: [ahasend.com](https://ahasend.com)

---

### 31. EmailJS
* **Overview**: A unique client-side email service that enables sending emails directly from frontend code (JavaScript, React, Vue, Angular, Flutter, iOS) without creating or running any backend server.
* **Free Tier Allowance**:
  * **200 emails / month** free
  * Up to 2 email templates
  * Connect up to 2 email services (e.g., Gmail, SendGrid, Mailgun, Fastmail)
* **Credit Card Required**: No
* **Key Features**: Zero backend infrastructure required, reCAPTCHA integration to prevent form abuse, template parameter injection, client-side SDKs.
* **Website**: [emailjs.com](https://www.emailjs.com)

---

### 32. Forward Email
* **Overview**: A 100% open-source, privacy-first email service built with quantum-resistant encryption. Primarily renowned for unlimited inbound domain forwarding, with optional outbound sending.
* **Free Tier Allowance**:
  * **Unlimited** inbound email forwarding and aliases on custom domains
  * Free REST API for programmatic domain and alias management
  * *Note*: Outbound SMTP sending requires a paid plan ($3/mo).
* **Credit Card Required**: No (for free forwarding and aliases)
* **Key Features**: 100% open-source codebase, no email logging or tracking, disposable aliases, catch-all routing, DMARC/SPF/DKIM automated records.
* **Website**: [forwardemail.net](https://forwardemail.net)

---

### 33. Novu
* **Overview**: An open-source notification infrastructure platform that centralizes and coordinates transactional communications across email, SMS, push notifications, and in-app inbox feeds.
* **Free Tier Allowance**:
  * **30,000 events / month** free on Novu Cloud
  * **Unlimited** events when self-hosted (open source)
* **Credit Card Required**: No
* **Key Features**: Connects with any email provider (SES, Resend, SendGrid, Postmark, Mailgun), visual workflow orchestrator, digests, user notification center UI components.
* **Website**: [novu.co](https://novu.co)

---

### 34. Courier
* **Overview**: A multi-channel notification engine for developers with a powerful visual template designer, multi-provider routing rules, and automatic failovers across email backends.
* **Free Tier Allowance**:
  * **10,000 notifications / month** free
  * Full access to API, design studio, and multi-channel routing
* **Credit Card Required**: No
* **Key Features**: Multi-provider failover routing (fallback to secondary email provider if primary fails), drag-and-drop template studio, preferences management, SDKs for major languages.
* **Website**: [courier.com](https://www.courier.com)

---

### 35. Postal
* **Overview**: A complete, enterprise-grade open-source mail delivery platform designed as a self-hosted alternative to proprietary services like SendGrid, Mailgun, and Postmark.
* **Free Tier Allowance**:
  * **100% Free / Open Source** (MIT License)
  * **Unlimited** emails (run on your own servers / VPS; you control IP reputation and server costs)
* **Credit Card Required**: No
* **Key Features**: Full web UI dashboard, live click/open tracking, IP pool assignment, webhook delivery updates, inbound mail routing, spam/antivirus checking integration.
* **Website**: [postalserver.io](https://postalserver.io)

---

### 36. Listmonk
* **Overview**: A blazingly fast, standalone, self-hosted newsletter and mailing list manager packaged as a single Go binary backed by PostgreSQL.
* **Free Tier Allowance**:
  * **100% Free / Open Source** (GNU AGPL-v3)
  * **Unlimited** emails and subscribers (self-hosted; connect your own SMTP relay or AWS SES)
* **Credit Card Required**: No
* **Key Features**: Ultra-fast performance (thousands of emails/sec), rich REST API for subscriber/campaign management, custom templating, multi-threading, privacy-first tracking.
* **Website**: [listmonk.app](https://listmonk.app)

---

## 🎯 Selection Guide: Which One Should You Pick?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       WHAT IS YOUR PRIMARY USE CASE?                        │
└──────────────────────────────────────┬──────────────────────────────────────┘
                                       │
         ┌─────────────────────────────┼──────────────────────────────┐
         ▼                             ▼                              ▼
  Modern Web / SaaS            High-Volume / Free               Self-Hosted / AI
 ┌─────────────────────┐      ┌─────────────────────┐      ┌─────────────────────┐
 │ • Resend            │      │ • SendPulse         │      │ • Postal            │
 │   (React Email/TS)  │      │   (12,000/mo free)  │      │   (Full mail server)│
 │ • Loops             │      │ • EmailOctopus      │      │ • Listmonk          │
 │   (SaaS lifecycle)  │      │   (10,000/mo free)  │      │   (Fast Go/Postgres)│
 │ • Postmark          │      │ • Brevo             │      │ • useSend / Plunk   │
 │   (Mission-critical)│      │   (300/day = ~9k/mo)│      │   (AWS SES wrapper) │
 │ • Cloudflare        │      │ • Mailjet           │      │ • Primitive         │
 │   (Edge Workers/API)│      │   (6,000/mo free)   │      │   (AI agent inboxes)│
 └─────────────────────┘      └─────────────────────┘      └─────────────────────┘
```

* **Best Developer Experience (DX) for React & Next.js**: [Resend](#1-resend)
* **Highest Permanent Free Volume**:
  * [SendPulse](#25-sendpulse) (12,000 emails/mo)
  * [EmailOctopus](#26-emailoctopus) (10,000 emails/mo)
  * [Brevo](#6-brevo) (300 emails/day = ~9,000/mo)
  * [Mailjet](#27-mailjet) (6,000 emails/mo)
  * [Resend](#1-resend), [MailerSend](#7-mailersend), [Elastic Email](#28-elastic-email), [useSend](#24-usesend) (3,000 emails/mo each)
* **Best Open-Source & Self-Hosted Platforms**:
  * [Postal](#35-postal) (full SendGrid/Mailgun server replacement)
  * [Listmonk](#36-listmonk) (high-speed Go newsletter engine)
  * [useSend](#24-usesend) & [Plunk](#12-plunk) (open-source SaaS & AWS SES wrappers)
* **Best Multi-Channel Notification Orchestration**: [Novu](#33-novu) (30,000 events/mo free) & [Courier](#34-courier) (10,000 notifications/mo free)
* **Best Client-Side / No Backend Required**: [EmailJS](#31-emailjs) (send directly from browser/frontend)
* **Lowest Cost at Millions of Emails**: [AWS SES](#4-aws-ses) ($0.10 / 1,000 emails)
* **Strict Transactional Deliverability**: [Postmark](#2-postmark), [ZeptoMail](#17-zeptomail), and [SMTP2GO](#29-smtp2go)
* **Strict EU Data Residency & GDPR**: [Lettermint](#21-lettermint), [Scaleway](#16-scaleway), and [AhaSend](#30-ahasend)
* **For AI Agents & Programmable Inboxes**: [Primitive](#23-primitive)
* **Pre-Production Email Testing & QA**: [Mailtrap](#13-mailtrap)

---

## 📄 License
This repository is open-source and available under the [MIT License](LICENSE).
