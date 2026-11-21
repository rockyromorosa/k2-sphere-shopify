# K2 Sphere — Shopify Storefront Development & Customization

**Professional Client Project | My Amazon Guy (MAG)**

**Role:** Shopify Developer — Primary Hands-on Development, Customization & Bug Fixes  
**Project Type:** Extensive Shopify storefront development, UI/UX improvements, and storefront bug fixes  
**Platform:** Shopify  
**Technologies:** Shopify Liquid, HTML, CSS, JavaScript, Shopify product metafields, Shopify Theme Editor  
**Live Website:** https://k2-sphere.com/

---

## Project Overview

**K2 Sphere** is an apparel eCommerce brand with a Shopify storefront featuring product collections, color and size variants, a product-detail purchase experience, and a Creator & Affiliate Program.

During my employment at **My Amazon Guy (MAG)**, **I personally handled most of the hands-on Shopify development and fixes for K2 Sphere during my assignment**. My responsibilities went beyond making minor visual edits: I implemented storefront customizations, investigated and fixed UI and interaction problems, improved the product shopping experience, and tested changes across screen sizes.

My work included product-page layouts and controls, color-variant image behavior, responsive styling, cart usability fixes, Creator & Affiliate Program form presentation, and related workflow configuration and QA. The source files below document both custom implementations and concrete fixes I made in the existing theme.

This repository is a **portfolio record of real client work**, not a tutorial or a demonstration store. It combines storefront screenshots with relevant Shopify theme files to illustrate the implementations I worked on.

**Scope:** I was responsible for a substantial share of the development and troubleshooting work, particularly the fixes. K2 Sphere was already operating on Shopify, so my work was **development and enhancement of an existing storefront**, not an assertion that I built its original commercial theme or third-party applications from scratch.

---

## My Direct Responsibilities

- **Hands-on implementation:** Built and modified Shopify Liquid templates, CSS, and JavaScript for storefront UI and customer interactions.
- **Problem-solving:** Investigated defects, traced conflicting theme/app behavior, applied targeted fixes, and checked their effects on desktop and mobile layouts.
- **Product experience:** Worked directly on the product gallery, variant swatches, size selection, product content, and purchase controls.
- **Cart experience:** Resolved mobile drawer, overlay, button visibility, and related styling problems.
- **Creator integration:** Customized the theme-side appearance and responsiveness of the OPTIS creator application experience and worked on the related configuration and newsletter workflow.

## My Development Work and Fixes

### 1. Shopify Product Detail Page Development

I worked extensively on the product presentation and purchase experience, including:

- Responsive desktop, tablet, and mobile product-page layouts.
- Product color swatches and rectangular size-selection controls.
- Image-gallery behavior when customers change product color variants.
- Thumbnail positioning, gallery presentation, and video visibility adjustments.
- Custom **Add to Bag** and **Buy Now** button presentation and interactions.
- Product information tabs for **Description**, **Size & Fit**, and **About the Brand**.
- Size-guide access with product-specific metafield support.
- Wishlist icon styling and selected-state presentation.
- Related-product merchandising and responsive display adjustments.

The Shopify Liquid templates combine product data, metafields, section settings, CSS, and JavaScript to produce these behaviors.

### 2. Cart and Conversion-Focused UI Fixes

A significant part of my K2 Sphere work involved **diagnosing and correcting existing cart UI problems**, including:

- Mobile side-cart recommendation positioning.
- Removal of a stuck or obscuring side-cart overlay.
- Cart-page checkout and shipping-calculator button visibility.
- Styling and interaction fixes for cart controls.
- Supporting theme-level side-cart and coupon interface adjustments.

These were practical storefront fixes, not merely design mockups or speculative improvements.

### 3. Creator & Affiliate Program Frontend Customization

The storefront includes a Creator & Affiliate Program with a separate onboarding/application experience.

My theme-level customization included UI refinements around the **OPTIS-powered form**, such as:

- Responsive form layout and mobile presentation.
- Product-selection and color-swatch display refinements.
- Content ownership and agreement interface presentation.
- Consent and signature-canvas styling and layout adjustments.
- Handling dynamically inserted form elements through JavaScript and DOM observation.

**Integration boundary:** The underlying OPTIS form engine, application submission service, and signature-capture engine are third-party functionality. The included `theme.liquid` documents theme-side modifications and UI behavior, not the complete application backend.

### 4. Creator Application Configuration and Newsletter Workflow

In addition to theme-side styling, my earlier K2 Sphere work covered **OPTIS Creator Application configuration and Shopify marketing automation**:

- Worked on creator product preferences with up to three product choices, including color and size selections; the first choice was required in the planned configuration.
- Updated Creator & Affiliate Program commission messaging from **5–10%** to **5–20%**.
- Implemented and tested the creator newsletter-consent/customer-tagging flow using **OPTIS customer creation and Shopify Flow**. The workflow was named **`K2 SPHERE - Creator Newsletter Subscription & Tagging`** and used the **`K2-Creator-Newsletter`** tag; positive and negative QA scenarios were reported as passed.

**Status and evidence:** These are documented project activities from earlier work discussions, **not source code contained in the five theme files**. The client subsequently requested an **independent email-only newsletter sign-up approach**, so the earlier workflow must not be presented as necessarily representing the current live signup behavior. The third-party app's own form logic and backend are not included here.

### 5. Responsive Fixes, Merchandising, and Testing

- Adjusted product-page layouts for desktop, tablet, and mobile breakpoints.
- Refined sticky product-media behavior on tablets and worked through color-switching/thumbnail issues.
- Checked visual consistency across product and cart interfaces in the Shopify theme editor and storefront previews.
- Supported sale-price updates for K2 Sphere apparel products. These were store-merchandising changes, not custom-coded discount logic; current storefront pricing may differ from the historical updates.

---

## Storefront Screenshots

The screenshots below document the main customer journeys in the K2 Sphere storefront. The linked files are uploaded in this repository. The development sections above distinguish the functionality I implemented and fixed from the larger storefront and third-party applications.

### Homepage

![K2 Sphere homepage hero](<01 - Homepage/K2Sphere_01_Homepage_Hero.png>)

The homepage features K2 Sphere's branded campaign hero and main shopping navigation.

### Creator & Affiliate Program

![Creator and affiliate landing page](<02 - Creator Landing Page/K2Sphere_02_Creator_Landing_Page.png>)

![Creator application form](<03 - Creator Application/K2Sphere_03_Creator_Application.png>)

![Product and color selection](<03 - Creator Application/K2Sphere_04_Product_Selection.png>)

![Agreement and digital signature interface](<03 - Creator Application/K2Sphere_05_Digital_Signature.png>)

These screenshots show the public creator-program journey and the form's visible input, product-selection, and agreement interfaces.

### Collection Page

![All Collection page](<04 - Collection Pages/K2Sphere_06_All_Collection.png>)

The collection view presents products with catalog filtering, sorting, prices, and color options.

### Product Detail Page

![Essentials Long Sleeve Top product page](<07 - Product Detail Pages/K2Sphere_07_Essentials_Long_Sleeve_PDP.png>)

The product page demonstrates the color and size selection, image gallery, wishlist, purchase buttons, description tabs, and related-item layout.

---

## Technical Spotlight 1 — Product Detail Page Customization

**Main source:** [`product-template-1.liquid`](<05 - Custom Code/product-template-1.liquid>)

The product template implements a customized presentation layer for a Shopify product and its variants.

### Shopify Liquid

- Uses product and variant information supplied by Shopify.
- Displays a product subtitle using the `custom.product_subtitle` metafield with a section-setting fallback.
- Displays badge text using the `custom.product_badge_text` metafield when populated.
- Supports a product-specific size-guide image with a theme-setting fallback.
- Renders configurable product blocks and related-product selections.

### JavaScript and CSS

- Styles color-circle swatches and rectangular size controls.
- Implements custom purchase buttons and a Buy Now navigation handler.
- Manages product-information tab visibility.
- Adjusts image-gallery layout at tablet breakpoints.
- Contains JavaScript hooks that **queue** product-view and add-to-cart interaction events for Klaviyo. Their presence in source code does not independently establish successful delivery or analytics attribution. The click handlers also do not wait for confirmed add-to-cart success.

The source demonstrates how Liquid, product metafields, JavaScript, and responsive CSS are combined in a real Shopify storefront.

---

## Technical Spotlight 2 — Variant-Aware Product Media

**Verified source:** [`product-template-1.liquid`](<05 - Custom Code/product-template-1.liquid>)  
**Additional uploaded source:** A separate full mobile product section whose schema is named **`DTC Custom Product Mobile`**. Its **original filename in Shopify is not yet verified**, so it is intentionally not linked here under an assumed name.

The product-page work includes gallery logic that considers the selected product color and coordinates the displayed media with that variant.

Implementation details visible in the supplied product template include:

- Loading product data through Shopify's `/products/{handle}.js` endpoint.
- Reading variant-to-image associations and media positions.
- Grouping images by color ranges to determine which gallery items to display.
- Using Slick gallery filtering and navigation for the main image and thumbnails.
- Preserving a relative gallery position during color changes where possible.
- Keeping a product video visible when configured through a dedicated metafield.
- Applying additional mobile and tablet layout adjustments.

This implementation was developed within the existing Shopify theme and depends on the theme's gallery markup and JavaScript libraries.

---

## Technical Spotlight 3 — Cart UI Troubleshooting

**Main sources:** [`cart-draw.css`](<05 - Custom Code/cart-draw.css>), [`cart-template.liquid`](<05 - Custom Code/cart-template.liquid>), and [`theme.liquid`](<05 - Custom Code/theme.liquid>)

Examples of cart-related work include:

- Correcting mobile side-cart product recommendation positioning.
- Preventing overlay pseudo-elements from obstructing cart interactions.
- Improving button readability and visibility on the cart page.
- Refining side-cart interface states and presentation.

These examples show the kind of **hands-on bug fixing and frontend troubleshooting** that made up a major part of my K2 Sphere assignment.

---

## Technical Spotlight 4 — Creator Form UI Integration

**Main source:** [`theme.liquid`](<05 - Custom Code/theme.liquid>)

The custom theme code contains style and interaction adjustments for the OPTIS creator application. It uses responsive CSS, browser-side JavaScript, and DOM observation to work with dynamically rendered controls.

Examples include mobile form layout refinements, product-option swatches, agreement-modal presentation, and signature-canvas interface styling.

The underlying form data model, legal agreement content, submission workflow, and third-party app internals are not presented as independently authored Shopify theme components.

---

## Technology Stack

| Technology | Usage |
|---|---|
| Shopify | eCommerce storefront and product catalog |
| Shopify Liquid | Product templates, theme sections, and dynamic storefront data |
| HTML | Product-page and interface markup |
| CSS | Component styling, responsive layouts, cart and form fixes |
| JavaScript | Variant selection, galleries, UI interactions, and event handling |
| Shopify Metafields | Product subtitles, badges, size guides, and media references |
| Shopify Theme Editor | Configurable product and interface settings |
| Slick / PhotoSwipe | Media gallery behaviors integrated with the theme |
| OPTIS | Third-party creator application form presented and customized within the storefront |
| Klaviyo | Frontend product-view and click-based add-to-cart queue calls (delivery not independently verified) |
| Shopify Flow | Creator newsletter-consent/customer-tagging workflow reported in project QA; not exported in this repository |

---

## Repository Structure

```text
k2-sphere-shopify/
├── 01 - Homepage/
│   └── K2Sphere_01_Homepage_Hero.png
├── 02 - Creator Landing Page/
│   └── K2Sphere_02_Creator_Landing_Page.png
├── 03 - Creator Application/
│   ├── K2Sphere_03_Creator_Application.png
│   ├── K2Sphere_04_Product_Selection.png
│   └── K2Sphere_05_Digital_Signature.png
├── 04 - Collection Pages/
│   └── K2Sphere_06_All_Collection.png
├── 05 - Custom Code/
│   ├── theme.liquid
│   ├── cart-draw.css
│   ├── cart-template.liquid
│   ├── product-media.liquid
│   └── product-template-1.liquid
├── 07 - Product Detail Pages/
│   └── K2Sphere_07_Essentials_Long_Sleeve_PDP.png
└── README.md
```

> **Source note:** The file uploaded as `product-media.liquid` contains a full mobile product section named `DTC Custom Product Mobile`. Its original theme path has not yet been independently confirmed. These selected files also include pre-existing theme code and do not form a complete runnable Shopify theme. A separate legacy copy of the README is temporarily present at the repository root and can be removed after this version is restored.

---

## What This Project Demonstrates

- Significant direct responsibility for Shopify Liquid theme development and bug fixing.
- Responsive eCommerce user-interface implementation.
- Product variant, image-gallery, and media behavior customization.
- Shopify metafield-driven content and Theme Editor configuration.
- Cart troubleshooting and targeted frontend fixes.
- Third-party embedded form UI integration and styling.
- Creator application configuration and newsletter consent/tagging QA (historical workflow, not included as source).
- Browser-side JavaScript interaction and event handling.
- Real client delivery within a professional eCommerce agency.

---

## Project Ownership and Attribution

K2 Sphere was a professional client project I worked on as a **Shopify Developer at My Amazon Guy (MAG)**. **I personally completed most of the hands-on development work and fixes within my K2 Sphere assignment.** This repository is a record of that direct professional work, including the customizations and technical problems I resolved.

The client owns its brand and storefront, and pre-existing theme components and third-party applications retain their respective ownership. That does not diminish my direct responsibility for the code changes, integration customizations, and fixes described here.

Code and screenshots should only be published where permitted by the applicable client, employer, theme, and third-party licensing terms. **Authorization to access or edit a Shopify theme is not automatically permission to redistribute the entire commercial theme publicly.** Check the applicable sharing permissions, and remove credentials, confidential business details, or protected third-party code before publication.

**Evidence note:** Technical functionality described above is grounded in the shared `theme.liquid`, `cart-draw.css`, `cart-template.liquid`, `product-template-1.liquid`, and uploaded mobile-section code. Newsletter/Flow and merchandising activities are drawn from previous K2 Sphere project discussions, not from the provided code files. Store screenshots and historical work notes alone do not confirm the current production state of every feature.

---

## Live Website

**K2 Sphere:** https://k2-sphere.com/

---

**Portfolio maintained by Rocky Romorosa**  
Shopify & eCommerce Developer
