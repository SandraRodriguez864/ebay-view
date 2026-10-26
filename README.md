eBay View 

<p align="center"> <a href="https://github.com/yourusername/facebook-bot"> <img src="https://img.shields.io/badge/Try%20It%20Free-1E90FF?style=for-the-badge&logo=fire&logoColor=white" alt="Try it Free" width="30%"> </a> </p>

<p align="center">
  <a href="https://discord.gg/vBu9huKBvy">
    <img src="https://img.shields.io/badge/Join-Discord-5865F2?logo=discord" alt="Join Discord">
  </a>
  <a href="https://t.me/devpilot1">
    <img src="https://img.shields.io/badge/Contact-Telegram-2CA5E0?logo=telegram" alt="Contact on Telegram">
  </a>
</p>


---

##  About

**eBay Viewer** is an open-source toolkit that helps sellers **analyze** and **optimize** their eBay listings.  
It ingests Seller Hub performance data, runs SEO audits, tracks search placement, and notifies you of important changes.  

---



---

<p align="center">
<img src="./ebay-view-bot.png" alt="eBay View Bot Hero" width="80%"/>
</p>



---

## Installation

### 1. Clone & Install
```bash
# 1) Install deps
pip install -r requirements.txt

# 2) Configure env
cp .env.example .env

# 3) Ingest a Seller Hub CSV
python -m src.cli ingest --path data/seller_hub_report.csv --out reports/ingested.csv

# 4) Run SEO audit
python -m src.cli audit --input reports/ingested.csv --out reports/seo_audit.csv

# 5) One-off rank snapshot
python -m src.cli rank --keyword "iphone 13 case" --out reports/rank_snapshot.csv

# 6) Monitor competitor price/stock
python -m src.cli watch --list data/competitors.txt --out reports/price_watch.csv

# 7) Fire alerts from your audit CSV
python -m src.cli alerts --src reports/seo_audit.csv --threshold 0.2)


