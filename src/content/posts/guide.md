---
title: Gyoza User Guide
date: 2024-04-01
lastMod: 2024-08-10T03:58:16.758Z
summary: Welcome to Gyoza — a simple and cute Astro blog theme. This article will introduce how to use and deploy Gyoza.
category: Tutorial
tags: [Astro, Gyoza]
sticky: 1
---

## Prerequisites

- Node version >= 18.18.0
- pnpm version > 8.1.0

## Installation

### Fork & Clone Repository

Log into your GitHub account, open [lxchapu/astro-gyoza](https://github.com/lxchapu/astro-gyoza), and click the **Fork** button in the top-right corner to copy the repo into your account.

Copy the repo’s URL, open your terminal, and run `git clone` to clone it locally.

> This project recommends using **pnpm** as your package manager. If you haven’t installed pnpm yet, please install it first.

### Install Dependencies

```sh
cd astro-gyoza
pnpm install
```

### Available Commands

Run locally:

```sh
pnpm dev
```

Build static files:

```sh
pnpm build
```

Local preview:

```sh
pnpm preview
```

### Configuration

Most project configuration lives in `src/config.json`.

You should **first update `site.url` to your own domain** to avoid navigation issues.

Here’s an overview of the config options:

```json
{
  "site": {
    "url": "", // Site URL
    "title": "", // Site title
    "description": "", // General site description (SEO)
    "keywords": "", // General site keywords (SEO)
    "lang": "en", // Site language
    "favicon": "", // Browser favicon, stored in /public
    "appleTouchIcon": "" // Apple touch icon, stored in /public
  },
  "author": {
    "name": "", // Author name
    "twitterId": "", // Twitter handle (with @), used for Open Graph
    "avatar": "" // Author avatar URL
  },
  // Homepage Hero component
  "hero": {
    "name": "", // Display name
    "bio": "", // Short tagline
    "description": "", // Longer description
    "socials": [
      {
        "name": "", // Platform name
        "icon": "", // Icon class
        "url": "", // Link
        "color": "" // Icon color
      }
    ],
    "yiyan": "" // One-liner quote
  },
  "color": {
    "accent": [{ "light": "", "dark": "" }], // Accent colors
    "bg": {
      "primary": { "light": "", "dark": "" },
      "secondary": { "light": "", "dark": "" }
    },
    "text": {
      "primary": { "light": "", "dark": "" },
      "secondary": { "light": "", "dark": "" }
    },
    "border": {
      "primary": { "light": "", "dark": "" }
    }
  },
  // Top navigation menu
  "menus": [
    {
      "name": "Home",
      "link": "/",
      "icon": "icon-pantone"
    }
  ],
  "posts": {
    "perPage": 10 // Number of posts per page
  },
  "footer": {
    "startTime": "" // Blog start time (ISO format)
  },
  // Waline comment system https://waline.js.org/
  "waline": {
    "serverURL": ""
  },
  // Sponsorship
  "sponsor": {
    "wechat": "" // WeChat sponsor QR code
  },
  // Analytics (set enable=true and configure one)
  "analytics": {
    "enable": false,
    "google": {
      "measurementId": ""
    },
    "umami": {
      "serverUrl": "",
      "websiteId": ""
    },
    "microsoftClarity": {
      "projectId": ""
    }
  }
}
```

## Deployment

> Here we’ll use **Vercel** as an example, but you can also choose Cloudflare Pages or your own server.
> Before deploying, make sure you’ve updated `site.url`.

### Deploy to Vercel

Log into your Vercel account, click **Add new\... → Project**, and under **Import Git Repository** select the repo you forked earlier. Click **Import**.

In the project setup page, just hit **Deploy** — wait a bit, and you’re done 👌.

Vercel will give you a default domain. You can set up a custom domain in project settings. For more details, check the Vercel documentation.

```

---

✨ This keeps the structure faithful but makes the English flow naturally for blog readers.

Do you want me to also **polish the summary line** (make it a bit more fun/engaging for readers instead of literal translation)?
```
