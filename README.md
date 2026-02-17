# 🏏 India vs Pakistan WC 2026 — Twitter Analysis & Business Insights

> A full end-to-end social media analytics pipeline on 12,500+ tweets from the most-watched cricket match of 2026.

---

## 📌 What This Project Does

This notebook scrapes, cleans, and deeply analyzes Twitter/X activity around the **India vs Pakistan Champions Trophy 2026** match. The goal isn't just descriptive stats — every section ends with an actionable **business insight** that a brand, agency, or sports analytics team could act on.

The full pipeline covers:

- **Data Quality & Bot Detection** — custom 5-signal bot scoring system
- **Engagement Analysis** — power law, Lorenz curve, Gini coefficient
- **Verified vs Unverified** — reach and engagement gap quantification
- **Media vs Text Tweets** — visual content multiplier analysis
- **Hashtag Effectiveness** — how hashtag count impacts engagement (counterintuitive result)
- **Language & Geography** — 10-language breakdown of audience reach
- **Match Timeline** — minute-by-minute volume and engagement windows
- **Tweet Length vs Performance** — optimal character range by objective
- **Sentiment Analysis (VADER)** — negativity bias and its brand implications
- **Virality Deep Dive** — top 10 tweets dissected
- **Coordinated & Bot Activity** — what bots were pushing and why it doesn't work
- **Correlation Matrix** — what actually predicts likes, views, and retweets

---

## 🔑 Key Findings

| Finding | Insight |
|---|---|
| **42% of tweets were bot/spam** | Raw data is meaningless without cleaning |
| **Top 1% drove 85.4% of all likes** | Influence is hyper-concentrated — target 50 accounts to own a narrative |
| **#1 most liked account was Afghan** | The Afghanistan narrative dominated — unexpected cross-border emotion |
| **Negative tweets got 37% more likes** | Anger outperforms celebration in raw engagement |
| **1 hashtag = 77 avg likes. 6+ hashtags = 4 avg likes** | Hashtag stuffing actively kills reach |
| **Entire peak happened in 60 minutes** | Brands have a single window — be live or be invisible |
| **Verified + Media = 61x more engagement** | Content type and account credibility compound |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| `pandas` / `numpy` | Data wrangling |
| `VADER (vaderSentiment)` | Sentiment scoring |
| `BERTopic` | Topic modeling |
| `langdetect` | Language detection |
| `plotly` / `matplotlib` / `seaborn` | Visualizations |
| `google-generativeai` | Gemini API (optional — for extended insights) |
| `wordcloud` | Hashtag/term frequency visuals |

---

## 📁 Repository Structure

```
ind-vs-pak-twitter-analysis/
│
├── Ind_vs_Pak_Full_Analysis.ipynb   # Main analysis notebook
├── README.md                         # This file
├── .gitignore                        # Excludes raw data CSV
└── requirements.txt                  # All dependencies
```

> ⚠️ **The raw dataset (`indvspak_master.csv`) is not included** due to privacy considerations around real user handles. The notebook is fully documented so you can replicate the pipeline on your own scraped data.

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/ind-vs-pak-twitter-analysis.git
cd ind-vs-pak-twitter-analysis
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set your Gemini API key (optional)
```bash
export GEMINI_API_KEY='your-key-here'
```
Or in Google Colab, use the **Secrets panel (🔑)** to store `GEMINI_API_KEY`.

### 4. Add your dataset
Place `indvspak_master.csv` in the root directory. Expected columns:

| Column | Description |
|---|---|
| `Post_ID` | Unique tweet ID |
| `Author_Handle` | Twitter handle |
| `Tweet_Content` | Full tweet text |
| `UTC_Time` | Timestamp (UTC) |
| `Like_Count` | Like count |
| `Repost_Count` | Retweet count |
| `View_Count` | View count |
| `Reply_Count` | Reply count |
| `Bookmark_Count` | Bookmark count |
| `Verified_Status` | Boolean — account verified? |
| `Language` | Language code (en, hi, ur, etc.) |
| `has_media` | Boolean — image/video attached? |
| `likely_bot` | Boolean — bot detection flag |
| `is_organic` | Boolean — passed all quality filters? |
| `bot_signals` | Integer — number of bot signals triggered (0–5) |

---

## 📊 Sample Visualizations

The notebook generates 15+ interactive Plotly charts including:

- **Funnel chart** — Raw → Deduplicated → Organic data pipeline
- **Lorenz curve** — Engagement inequality across accounts
- **Hourly timeline** — Volume and engagement by UTC hour
- **Sentiment shift** — How the crowd's mood changed during the match
- **Hashtag effectiveness** — Count vs average likes (the counterintuitive chart)
- **Correlation heatmap** — What actually drives likes, views, retweets

---

## 💡 Business Applications

This analysis framework is directly applicable to:

- **Sports marketing teams** — identifying real-time activation windows
- **Social media agencies** — proving ROI of verified + visual content strategy
- **Brand strategists** — understanding audience sentiment and conversation ownership
- **Data journalists** — covering audience behavior in live sports events

---

## ⚠️ Ethics & Privacy

- No raw user data is published in this repository
- Individual handles are not called out in public outputs
- Analysis is used for aggregate pattern detection only
- Complies with Twitter/X's API Terms of Service for research use

---

## 📬 Connect

If you found this useful or have questions about the methodology, feel free to connect on [LinkedIn](https://linkedin.com/in/YOUR_HANDLE) or open an issue.

---

*Built with Python 🐍 | Data collected February 2026*
