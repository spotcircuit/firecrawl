
# 🔥 Firecrawl

Firecrawl is a minimal, Vercel-hosted static site that serves dynamically generated HTML result pages.

It is designed to integrate with automated scraping or extraction workflows (e.g., via [n8n](https://n8n.io/)) where results are published to this repository and auto-deployed by Vercel.

---

## 📦 Folder Structure


- All HTML result pages are stored in `public/results/`
- Pages are served from Vercel at:  
  `https://firecrawl.vercel.app/results/{filename}.html`

---

## 🚀 Deployment

This repo is auto-deployed by [Vercel](https://vercel.com).  
Every push to `main` triggers a redeploy.

**Live URL**:  
[https://firecrawl.vercel.app](https://firecrawl.vercel.app)


## 🤖 Automation

The HTML result files are committed to this repo via the GitHub REST API.

### Example `n8n` Setup:
- Scrape or extract content using Firecrawl API
- Format content as HTML
- Base64 encode and commit to this repo via:

Payload:
```json
{
"message": "Add result file",
"content": "base64-encoded-html-content",
"branch": "main"
}
 Use Cases
Web scraping reports

NLP extraction summaries

AI-generated content delivery

Client-facing result dashboards

MIT — free to use, extend, and adapt.
