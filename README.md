# 🎨 Louise's Art Store — Shopify Theme Development

A custom Shopify storefront built as a portfolio project to demonstrate Shopify theme development skills. The store sells prints of paintings (watercolor and gouache) and showcases a customized Dawn theme with custom sections, metafields, and i18n support.

## 🔗 Demo

👉 View live store : [Art Store](https://louiwitt-proto.myshopify.com/)

🔐 **Password : louiwitt-mdp**

---

## 🛠️ Tech Stack

- **Shopify CLI** — local development & theme sync
- **Liquid** — Shopify's templating language
- **Dawn** — used as base theme
- **JSON Templates** — Shopify page architecture
- **Git** — version control

---

## ✨ Features

### Custom Metafields
Extended the default product model with artwork-specific data:
- **Year** (`custom.year`) — year the painting was created

Displayed on the product page via custom Liquid in `sections/main-product.liquid`.

### Custom Section — About Me
Built a custom `sections/about-me.liquid` with:
- Photo, title, rich text and CTA button
- Color picker for background
- i18n support via `locales/` files
- Scroll-triggered animations using Dawn's native animation system

The section is available in the theme customizer via a `presets` block, making it usable by non-technical merchants without touching code.


### Product Page Customization
- Added `artwork_info` custom block grouping year and medium on the same line

---

## 📁 Project Structure

```
dawntheme/
├── assets/             # CSS & JS (base.css customized)
├── config/             # Theme settings (settings_schema.json, settings_data.json)
├── layout/             # theme.liquid — global HTML wrapper
├── locales/            # Translation files (en, fr)
├── sections/
│   ├── main-product.liquid       # Modified — metafields + artwork_info block
│   └── about-me.liquid           # Created from scratch
├── snippets/           # Reusable Liquid components
└── templates/
    ├── product.json              # Product page structure
    └── page.about-me.json        # About Me page template
```

---

## 🧠 Key Concepts Demonstrated

| Concept | Where |
|---|---|
| Liquid templating | `sections/main-product.liquid` |
| Custom section with schema | `sections/about-me.liquid` |
| JSON templates | `templates/page.about-me.json` |
| Metafields (native + custom) | Admin → Custom data + Liquid |
| i18n / locales | `locales/en.default.json`, `locales/en.default.schema.json`, `locales/fr.json` |
| Theme customizer (presets, blocks) | Schema JSON in sections |
| Shopify CLI workflow | `shopify theme dev`, `theme push/pull` |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Shopify CLI : `npm install -g @shopify/cli`
- A Shopify Partner account + development store


## 📚 What I Learned

This project was my first hands-on experience with Shopify after coming from a fullstack background. Key takeaways:

- **Liquid vs JSON templates** — understanding the separation between layout logic (Liquid) and page structure (JSON)
- **Code vs Admin distinction** — learned the separation between developer-controlled code (Liquid templates, CSS/JS, sections) and merchant-controlled admin (content, products, images, Theme Customizer settings)
- **using Dawn as a reference** — reading Dawn's source code (sections, snippets, schema conventions) was a fast way to learn Shopify best practices


*Built by Louise — Software Developer*
