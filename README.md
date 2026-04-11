# Blockonomics Docs — Mintlify Starter

This is the starter repository for the new Blockonomics documentation site, built with [Mintlify](https://mintlify.com).

---

## How to publish this site (step by step)

### Step 1 — Create a GitHub repo

1. Go to [github.com](https://github.com) and create a **new repository** (e.g. `blockonomics-docs`)
2. Make it **Public** (required for Mintlify's free plan)
3. Don't add any files yet

### Step 2 — Push this folder to GitHub

Open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial docs structure"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/blockonomics-docs.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

### Step 3 — Connect to Mintlify

1. Go to [mintlify.com](https://mintlify.com) and click **Get Started**
2. Sign up / log in with GitHub
3. Click **New Project** and select your `blockonomics-docs` repository
4. Mintlify will auto-detect `mint.json` and deploy your site
5. You'll get a live URL like `blockonomics.mintlify.app`

### Step 4 — Add your logo

Replace the placeholder logo paths in `mint.json`:
- `logo/light.png` — your logo for light mode
- `logo/dark.png` — your logo for dark mode
- `favicon.png` — your favicon

Upload those files to the root of this repo.

### Step 5 — Set a custom domain (optional)

In the Mintlify dashboard, go to **Settings → Custom Domain** and add `docs.blockonomics.co` (or similar). You'll need to add a CNAME record in your DNS settings.

---

## File structure

```
blockonomics-docs/
├── mint.json                    ← Navigation config (edit this to change sidebar)
├── getting-started/
│   ├── overview.mdx             ← Homepage of the docs
│   ├── quickstart.mdx           ← Fully written ✅
│   ├── pricing.mdx              ← Fully written ✅
│   ├── create-account.mdx       ← Stub — needs content
│   ├── add-wallet.mdx           ← Stub — needs content
│   ├── add-store.mdx            ← Stub — needs content
│   └── faq.mdx                  ← Fully written ✅
├── integrations/
│   ├── wordpress-woocommerce.mdx ← Fully written ✅
│   ├── whmcs.mdx                ← Fully written ✅
│   ├── prestashop.mdx           ← Stub — needs content
│   ├── telegram-bot.mdx         ← Stub — needs content
│   ├── payment-widget.mdx       ← Stub — needs content
│   ├── api-overview.mdx         ← Fully written ✅
│   ├── api-authentication.mdx   ← Stub — needs content
│   └── api-webhooks.mdx         ← Stub — needs content
├── wallets/
│   ├── overview.mdx             ← Stub — needs content
│   ├── xpub-explained.mdx       ← Stub — needs content
│   ├── ledger.mdx               ← Stub — needs content
│   └── electrum.mdx             ← Stub — needs content
├── troubleshooting/
│   ├── index.mdx                ← Fully written ✅
│   ├── error-codes.mdx          ← Fully written ✅
│   ├── gap-limit.mdx            ← Stub — needs content
│   ├── callbacks-failing.mdx    ← Stub — needs content
│   ├── missing-funds.mdx        ← Stub — needs content
│   └── address-generation.mdx   ← Stub — needs content
├── security/
│   ├── account-security.mdx     ← Stub — needs content
│   ├── two-factor-auth.mdx      ← Stub — needs content
│   ├── crypto-security.mdx      ← Stub — needs content
│   ├── why-trust-blockonomics.mdx ← Stub — needs content
│   └── transaction-policy.mdx   ← Stub — needs content
└── reference/
    ├── blockchain-explorer.mdx  ← Stub — needs content
    ├── checkout-customisation.mdx ← Stub — needs content
    ├── bitcoin-taxes.mdx        ← Stub — needs content
    ├── bug-bounty.mdx           ← Stub — needs content
    └── community.mdx            ← Stub — needs content
```

---

## Writing articles

All content files use `.mdx` format (Markdown + JSX components). Mintlify provides special components you can use anywhere:

```mdx
<Info>A blue info box</Info>
<Warning>An orange warning box</Warning>
<Tip>A green tip box</Tip>
<Note>A grey note box</Note>

<Steps>
  <Step title="First step">Content here</Step>
  <Step title="Second step">Content here</Step>
</Steps>

<Tabs>
  <Tab title="Option A">Content A</Tab>
  <Tab title="Option B">Content B</Tab>
</Tabs>

<CardGroup cols={2}>
  <Card title="Title" icon="rocket" href="/path">Description</Card>
</CardGroup>

<AccordionGroup>
  <Accordion title="Question">Answer here</Accordion>
</AccordionGroup>
```

Full component reference: [mintlify.com/docs/content/components](https://mintlify.com/docs/content/components)

---

## Content priority order

Fill in stubs in this order:

1. `getting-started/create-account.mdx` — every new user needs this
2. `getting-started/add-wallet.mdx` — core setup step
3. `getting-started/add-store.mdx` — core setup step
4. `wallets/xpub-explained.mdx` — linked from many articles
5. `wallets/electrum.mdx` — most recommended wallet
6. `wallets/ledger.mdx` — popular hardware wallet
7. `troubleshooting/callbacks-failing.mdx` — most common support issue
8. `troubleshooting/gap-limit.mdx` — second most common issue
9. `integrations/prestashop.mdx`
10. `security/*` — reuse existing Freshdesk content
