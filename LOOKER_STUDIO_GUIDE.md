# 🎨 Looker Studio Dashboard Design & Component Specification

This document provides exact styling specifications, palette codes, and chart configurations to replicate the high-converting **PhotoPixc Executive Dashboard**.

---

## 🎨 Color Palette & Typography

| Element | Hex Code | Purpose |
| :--- | :--- | :--- |
| **Canvas Background** | `#F8FAFC` | Light, crisp background (Slate-50) |
| **Card / Widget Background** | `#FFFFFF` | Clean card contrast with 8px corner radius |
| **Primary Brand Accent** | `#2563EB` | PhotoPixc Royal Blue (Buttons, Active Elements) |
| **Secondary Accent** | `#0D9488` | Teal / Cyan (Positive MER & High ROAS) |
| **Warning / Sub-Par** | `#F59E0B` | Amber (MER between 2.0x and 2.5x) |
| **Alert / Danger** | `#EF4444` | Red (MER below 2.0x break-even) |
| **Primary Text** | `#0F172A` | Slate-900 for headings & key numbers |
| **Muted Text** | `#64748B` | Slate-500 for labels & captions |
| **Font Family** | `Inter` or `Roboto` | Standard clean sans-serif |

---

## 📊 Component-by-Component Blueprint

### Page Dimensions
- **Width:** `1360px`
- **Height:** `1080px`

---

### 1. Header Banner
- **Component:** Rectangle Shape
  - Fill: `#0F172A` (Slate 900)
  - Dimensions: `1360px × 80px` (Top: `0px`, Left: `0px`)
- **Title (Text Box):**
  - Text: `E-Commerce Profit & MER Intelligence Engine`
  - Font: Bold, `22px`, White `#FFFFFF`
- **Subtitle / Link (Text Box):**
  - Text: `Designed for Growth Leaders • by photopixc.com`
  - Font: Regular, `13px`, Slate 300 `#CBD5E1`
  - URL link: `https://photopixc.com/ai-automation-for-marketing/`
- **Date Range Picker:**
  - Placed at top-right (`X: 1100px`, `Y: 20px`)
  - Default: `Last 30 days`

---

### 2. Top Metric Scorecards (Row 1: Y = 100px)

| Card | Metric | Comparison Period | Style Note |
| :--- | :--- | :--- | :--- |
| **Card 1** | `Revenue` (SUM) | Previous period | Big Number, Green if positive |
| **Card 2** | `Ad_Spend` (SUM) | Previous period | Big Number, Neutral |
| **Card 3** | `Blended MER` (SUM(Revenue)/SUM(Ad_Spend)) | Previous period | Conditional format: Green if > 3.0x |
| **Card 4** | `Blended CPA` (SUM(Ad_Spend)/SUM(Orders)) | Previous period | Conditional format: Green if < $30.00 |
| **Card 5** | `Total Orders` (SUM(Orders)) | Previous period | Format: Integer |

*Tip: Enable "Compact Numbers" for clean display (e.g., $15.4K).*

---

### 3. Visual Charts (Row 2: Y = 260px)

#### Chart A: Revenue vs Ad Spend Over Time (Left - 60% Width)
- **Chart Type:** Combo Chart
- **Dimension:** `Date`
- **Metric 1 (Bars):** `Ad_Spend` (Fill: `#94A3B8`, Light Slate)
- **Metric 2 (Bars):** `Revenue` (Fill: `#2563EB`, PhotoPixc Blue)
- **Metric 3 (Line - Right Axis):** `Blended MER` (Line Color: `#10B981`, Emerald Green, Width: 3px)
- **Reference Line:** Horizontal reference line on Right Y-axis at `3.0` labeled `Target MER (3.0x)`.

#### Chart B: Budget Allocation & ROAS by Channel (Right - 40% Width)
- **Chart Type:** Donut Chart
- **Dimension:** `Channel`
- **Metric:** `Ad_Spend`
- **Colors:**
  - Google Ads: `#4285F4` (Google Blue)
  - Meta Ads: `#0668E1` (Meta Royal Blue)

---

### 4. Deep-Dive Performance Table (Row 3: Y = 680px)
- **Chart Type:** Table with Heatmap
- **Dimensions:**
  1. `Channel`
  2. `Campaign_Name`
- **Metrics:**
  1. `Ad_Spend` (Format: USD Currency)
  2. `Clicks` (Format: Number)
  3. `CPC` (Format: USD Currency)
  4. `Orders` (Format: Number)
  5. `Revenue` (Format: USD Currency)
  6. `ROAS` (Format: Number, 2 decimals)
- **Heatmap Metric:** `ROAS` (Color scale from `#FEE2E2` (light red) to `#DCFCE7` (light green)).

---

### 5. Footer & Backlink Widget (Bottom: Y = 1000px)
- **Component:** Text & Icon Box
- **Content:**
  ```text
  ⚡ Powered by PhotoPixc Growth Engineering | Get your custom automated analytics pipeline at https://photopixc.com
  ```
- **Clickable Hyperlink:** `https://photopixc.com/`

---

## 💡 How to Publish as a Public Free Lead Magnet
1. In Looker Studio, click **Share** at the top right.
2. Under "Link Settings", change permission to: **"Anyone on the internet with the link can view"**.
3. Check the option: **"Prevent editors from changing access and adding new people"**.
4. Allow viewers to make a copy: Check **"Viewer options -> Allow viewers to download, print, or copy"**.
5. Copy the sharing link.
6. Share this link on LinkedIn, Twitter, Reddit (`r/ecommerce`, `r/PPC`), or on GitHub.
   * Every person who copies your template sees your **PhotoPixc** branding, links back to your site, and contacts you when they need customized automation!
