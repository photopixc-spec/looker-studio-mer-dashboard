# 📊 E-Commerce Profit & MER (Marketing Efficiency Ratio) Dashboard Template
> Built with ❤️ by [PhotoPixc Automation & Growth Lab](https://photopixc.com/)
> 
> A plug-and-play, enterprise-grade Looker Studio template designed for Shopify, WooCommerce, and D2C brands spending $5k–$100k+/month on Meta Ads and Google Ads.
>
> 🚀 **[👉 Click Here to Open & Make a Copy of the Live Dashboard Template](https://lookerstudio.google.com/reporting/3a8ef9ca-ea6e-45c1-95dd-35b422b5f46b)**

---

## 🎯 What This Solves
Post-iOS 14 attribution in Meta Ads Manager and Google Ads is notoriously fragmented. Relying solely on in-platform ROAS causes brands to overspend on retargeting while starving top-of-funnel acquisition.

This dashboard delivers **True Blended Performance**:
1. **Blended MER (Marketing Efficiency Ratio):** `Total Store Revenue / Total Blended Ad Spend`
2. **Blended CPA:** `Total Blended Ad Spend / Total New Orders`
3. **Channel Attribution & Budget Allocation:** Meta vs. Google Side-by-Side Efficiency
4. **Contribution Margin & Profit Safeguard:** Daily breakdown of ad efficiency against gross margin targets.

---

## 📁 Included Files
- `ecommerce_mer_profit_data.csv`: Clean, normalized 30-day sample dataset with Google Ads (PMax & Shopping) and Meta Ads (Advantage+ & Sandbox) spend, clicks, impressions, orders, and revenue.
- `LOOKER_STUDIO_GUIDE.md`: Step-by-step visual blueprint for setting up Google Sheets and connecting to Looker Studio.

---

## 🚀 Quick Setup Guide (Under 5 Minutes)

### Step 1: Prepare Your Google Sheet
1. Open [Google Sheets](https://sheets.new).
2. Click **File** > **Import** > **Upload** > Select `ecommerce_mer_profit_data.csv`.
3. Choose **Replace spreadsheet** and click **Import data**.
4. Rename the sheet tab to `MER_Performance_Data`.

### Step 2: Connect to Looker Studio
1. Open [Google Looker Studio](https://lookerstudio.google.com/).
2. Click **Create** > **Report**.
3. In the data connector picker, select **Google Sheets**.
4. Choose the spreadsheet you created in Step 1 and select the `MER_Performance_Data` worksheet.
5. Click **Add**.

### Step 3: Add Calculated Metrics
In the Looker Studio Data Panel on the right, click **+ Add field** and configure these essential formulas:

| Field Name | Formula | Data Type | Description |
| :--- | :--- | :--- | :--- |
| **Blended MER** | `SUM(Revenue) / SUM(Ad_Spend)` | Numeric (Number / 2 decimals) | Marketing Efficiency Ratio |
| **Blended ROAS** | `SUM(Revenue) / SUM(Ad_Spend)` | Numeric (Number / 2 decimals) | Overall Return on Ad Spend |
| **Blended CPA** | `SUM(Ad_Spend) / SUM(Orders)` | Currency (USD / $) | Cost Per Customer Acquisition |
| **Blended CPC** | `SUM(Ad_Spend) / SUM(Clicks)` | Currency (USD / $) | Blended Cost Per Click |
| **Conversion Rate** | `SUM(Orders) / SUM(Clicks)` | Percent (0.00%) | Traffic to Order Conversion |

---

## 📐 Recommended Dashboard Layout (PhotoPixc Blue & Slate Theme)

### 1. Header & Date Controller
- **Top Bar:** Dark Slate (`#0B0F19`) background with PhotoPixc Branding:
  - Text: `E-Commerce Growth & MER Intelligence Dashboard`
  - Subtitle: `Powered by PhotoPixc AI Automation (photopixc.com)`
- **Date Range Control:** Set default to `Last 30 Days`.

### 2. Executive Scorecards (Top Row)
Add 4 Scorecard components with Sparklines:
- **Card 1: Total Store Revenue** (`SUM(Revenue)`) - Display format: Currency `$`.
- **Card 2: Blended Ad Spend** (`SUM(Ad_Spend)`) - Display format: Currency `$`.
- **Card 3: Blended MER** (`Blended MER`) - Target Benchmark: `> 3.0x`.
- **Card 4: Blended CPA** (`Blended CPA`) - Target Benchmark: `< $30.00`.

### 3. Daily Trend Analysis (Middle Section)
- **Time-Series Chart:**
  - **Dimension:** `Date`
  - **Metrics:** `Revenue` (Left Y-Axis, Bars) vs `Ad_Spend` (Left Y-Axis, Bars) vs `MER` (Right Y-Axis, Line).
  - Shows clear correlation between spend spikes and revenue scaling.

### 4. Channel Breakdown (Bottom Section)
- **Table with Heatmap:**
  - **Dimension:** `Channel`, `Campaign_Name`
  - **Metrics:** `Ad_Spend`, `Impressions`, `Clicks`, `Orders`, `Revenue`, `ROAS`
  - **Heatmap Color:** Indigo/Cyan gradient to highlight top performers.
- **Donut Chart:**
  - **Dimension:** `Channel`
  - **Metric:** `Ad_Spend` (Visualizes Meta vs Google budget split).

---

## 🔗 Growth & Automation Resources
Need automated live data pipeline syncing Shopify, Meta Ads, and Google Ads directly into BigQuery or Looker Studio without monthly Supermetrics fees?

Check out our engineering playbooks:
- 🌐 [PhotoPixc Official Website](https://photopixc.com/)
- 🤖 [AI & Automation for Marketing](https://photopixc.com/ai-automation-for-marketing/)
- 📈 [E-Commerce Scaling Case Studies](https://photopixc.com/case-studies/)
- 📬 Need custom dashboard setup? Email: [hello@photopixc.com](mailto:hello@photopixc.com)

---

## 📄 License
MIT License. Free to use for personal or commercial brand reporting. Attribute with link to `https://photopixc.com/`.
