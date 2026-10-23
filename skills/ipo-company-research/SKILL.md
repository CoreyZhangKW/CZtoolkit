---
name: ipo-company-research
description: Conducts comprehensive background research on pre-IPO or listed companies for capital markets lawyers and sponsors. Use when a user asks to research a company for an IPO pitch, prepare background materials for management meetings, analyze a company's core business, market position, financial performance, competitive advantages, capital markets story, or potential risks for listing, refinancing, or investor-facing positioning.
---

# IPO Company Research Skill

This skill guides Manus in conducting deep, structured background research on companies, especially pre-IPO or already listed companies, to help capital markets lawyers and sponsors prepare management pitches, meeting materials, diligence notes, and investor-facing positioning.

## Core Workflow

When asked to research a company for an IPO, refinancing, capital markets positioning, or management pitch, follow these steps in order.

### 1. Confirm Company Identity and Disclosure Universe

- Identify the company's exact legal name, common short name, stock code if any, official website, registered address, founding history, registered capital, controller, and key corporate milestones and recent corporate events such as restructuring, M&A, or debt offerings.
- If the company is listed, delisted, or has previously filed for listing, prioritize official public disclosures over secondary sources. Search and review the latest annual report, latest semi-annual report, latest quarterly updates where relevant, ESG or sustainability report, IPO prospectus, listing application proof, bond offering memorandum, feedback responses, regulatory notices, and major transaction announcements.
- For A-share companies, search CNINFO, exchange websites (上交所/深交所), company investor-relations pages, SASAC (国资委) disclosures for state-owned enterprises, and reputable financial portals. For HK-listed or applicant companies, search HKEXnews, the Stock Exchange application proof page, annual reports, prospectuses, and announcements.
- Preserve source URLs and document names as references. Use the most complete source available, such as annual report full text rather than annual report summary.

### 2. Build the Evidence Base Before Writing

- Extract hard facts from official disclosures: segment revenue, gross margin, R&D expenses, R&D headcount, patents, certifications, customer names if disclosed, supplier dependence, production capacity, product applications, geographic revenue, cash flow, capital expenditure, and pending transactions.
- Supplement official disclosures with credible industry data from regulator reports, industry associations, market research summaries, exchange filings of peers, and reputable financial media.
- Cross-check important numerical claims against at least one official source where possible. Always cite the reporting period, such as 2025 annual report or 2025 interim report.
- For technical or manufacturing companies, capture both commercial evidence and operational evidence: customer certification cycles, equipment base, quality systems, testing capabilities, capacity, yield, supply-chain localization, and product roadmap.

### 3. Deep Dive into Core Business, Market Position, and Business Model

- Describe the company's revenue model, product portfolio, major business lines, customer groups, supplier structure, production and delivery model, and sales process.
- Identify the strategic role of the company's products in the value chain. Explain why the product is mission-critical to customers and what would make replacement difficult.
- Find industry rankings, market size, growth drivers, entry barriers, regulatory tailwinds, localization trends, and peer comparisons, including a list of the company's key competitors in China and overseas.
- Identify core assets, including mines, production bases, patents, certifications, platforms, customer access, data assets, infrastructure, manufacturing lines, R&D centers, or licenses, and confirm their operational status.

### 4. Financial Performance and Governance

- Compile the latest three years of key financial data, including revenue, gross profit, gross margin, net profit, adjusted profit if applicable, operating cash flow, capex, R&D expenses, total assets, borrowings, and gearing if relevant.
- For listed companies, include latest interim results if they materially update the story.
- Identify shareholders, ultimate controllers, directors, supervisors, senior management, incentive plans, pledged shares, related-party transactions, major acquisitions, and material financing activity.

### 5. Competitive Advantages Messaging Playbook

The competitive-advantages section is often the most important part of the report for management and investor communication. Do not write generic advantages. Convert the evidence base into 4-6 concise but attention-grabbing headings, each supported by 1-2 short paragraphs of official disclosures and current industry data.

Use this method:

1. Start from the company's disclosed facts, not from adjectives. Use annual reports, interim reports, prospectuses, ESG reports, and official announcements as the anchor.
2. Combine company evidence with market evidence. For each advantage, pair an internal proof point, such as revenue, margin, patents, certifications, customer access, capacity, or equipment, with an external tailwind, such as market size, growth rate, regulation, localization, or customer capex cycle.
3. Rewrite the title into a capital-markets message. Prefer simple, memorable headings that communicate why investors or management should care.
4. Keep the supporting text short. Each advantage should normally be 1-2 paragraphs, with the most compelling data only.
5. Avoid unsupported superlatives. If using phrases such as “leading”, “global”, “only”, “first”, or “high barrier”, support them with a disclosure, ranking, award, customer list, certification, or quantifiable performance.

Use this title pattern where helpful:

| Generic draft | Stronger investor-facing title |
|---|---|
| Customer certification advantage | “Locked into the Customer’s Critical Process: Top-Tier Customer Certification as a Moat” |
| Market opportunity | “Riding a [market size] Industry Wave: Core Product Exposed to Structural Growth” |
| R&D advantage | “R&D Compounding: Turning Import Substitution into Global Competition” |
| Product expansion | “[Core Product] + [Second Curve]: From Single Champion to Platform Supplier” |
| Manufacturing capability | “Mass Production Is the Real Moat: Quality Systems and Heavy Equipment Enable High-End Delivery” |

For each advantage, include: (i) a punchy heading, (ii) one paragraph of public evidence, (iii) one paragraph explaining why the point matters to management, investors, valuation, or IPO positioning. Keep the section polished enough to be copied into a pitch deck or management briefing.

### 6. Strategic Analysis and IPO Recommendations

- Analyze the company's positioning, mission, development strategy, and capital markets narrative.
- Formulate specific recommendations for future strategy and use of proceeds. Link every recommendation to a disclosed bottleneck or growth opportunity, such as capacity expansion, R&D, working capital, overseas sales, supply-chain localization, acquisitions, digitalization, compliance systems, or ESG upgrades.
- For listed companies, adapt the recommendation to the relevant context: refinancing, H-share listing, spin-off, overseas listing, acquisition financing, market repositioning, or investor-relations story refresh.

### 7. Risk Assessment and ESG Compliance

- Search specifically for major litigation, disputes, regulatory penalties, exchange inquiry letters, sanctions, safety or environmental incidents, product quality issues, IP disputes, related-party transactions, debt pressure, share pledges, goodwill impairment, and M&A integration risks.
- Identify ESG-related risks, including environmental compliance, labor issues, supply-chain traceability, overseas trade controls, sanctions, export restrictions, data security, and anti-bribery compliance.
- Place this section after the strategic and competitive analysis unless the user asks for a legal due diligence memo, because the pitch report should first establish business value before presenting risks. Lawyers need to know the “skeletons in the closet” before pitching, so do not soften this section.

### 8. Report Generation and Deliverables

- Write the final report in Chinese unless the user explicitly requests another language.
- Use a professional capital markets style, with complete paragraphs, concise tables, and data-backed analysis.
- Use inline numeric citations with Markdown reference-style links for factual claims and external data.
- Generate both Markdown (`.md`) and Word (`.docx`) outputs. Do not generate PDF unless explicitly requested.
- Convert Markdown to Word with the bundled script, which uses pandoc and adds a table of contents:

  ```bash
  python /home/ubuntu/skills/ipo-company-research/scripts/md_to_docx.py <input.md> <output.docx>
  ```

- Install pandoc first if it is missing (`sudo apt-get install -y pandoc`). If pandoc cannot be installed or the script fails, use the bundled `python-docx` fallback instead of writing a converter from scratch. It handles headings (H1-H4), tables with styled headers and alternating row shading, bold/italic inline formatting, and Chinese font configuration (宋体 body, 黑体 headings); it does not handle images or nested lists:

  ```bash
  python3 -m venv .venv && .venv/bin/pip install python-docx   # use a venv if pip3 install is blocked
  python /home/ubuntu/skills/ipo-company-research/scripts/md_to_docx_py.py <input.md> <output.docx>
  ```

- Add centered page numbers to the footer of any Word deliverable, as the user requires them on formal legal and pitch documents. The script rewrites the file in place, so run it after the final conversion:

  ```bash
  python /home/ubuntu/skills/ipo-company-research/scripts/add_page_numbers.py <output.docx>
  ```

- Preview the Word file before delivery.

## Output Structure Template

The final report should follow this structure, tailored to the company and user request:

1. **摘要（Executive Summary）**: Company overview, investment or IPO readiness, and core judgment.
2. **公司概况与历史沿革**: Basic facts, restructuring, controller, milestones, capital operations, and listing history if any.
3. **核心业务与核心资产**: Product lines, technologies, operating model, production bases, customers, suppliers, and key assets.
4. **市场地位与竞争优势**: Industry size and growth, market position, key competitors, and 4-6 attention-grabbing competitive advantages supported by official disclosures and industry data.
5. **主要客户、供应商与商业模式**: Customer certification, revenue model, procurement model, supplier risks, and customer concentration where disclosed.
6. **财务表现**: Three-year financial table plus latest interim update if material; analyze revenue quality, margin, cash flow, R&D, leverage, and capex.
7. **股东与管理层构成**: Shareholding, controller, board and senior management, incentive arrangements, pledges, related-party matters, and governance observations.
8. **业务发展策略与募资用途建议**: **[Core section]** Capital markets story, strategic priorities, proposed use of proceeds, and execution logic.
9. **重大诉讼、争议与主要风险**: Legal, regulatory, financial, operational, ESG, geopolitical, supply-chain, IP, and M&A risks.
10. **结论与资本市场建议**: Concise positioning, transaction suitability, diligence priorities, and recommended next steps.
11. **参考文献**: Official disclosures and credible sources used.

## Quality Standards

- Prioritize official disclosures, exchange filings, regulator portals, company websites, and authoritative industry bodies.
- Use public internet search to fill gaps, but do not let media articles override official disclosures.
- For listed companies, always check the latest annual report and interim report before finalizing competitive advantages, financial analysis, or management-facing messaging.
- Make the report useful for capital markets lawyers: surface legal and disclosure issues, but also provide a clear, persuasive equity story.
- Make competitive advantages boardroom-ready: short titles, hard data, and a clear reason the advantage matters to investors.
- Avoid boilerplate use-of-proceeds recommendations. Tie each recommendation to the company's disclosed strategy, financial constraints, and industry trend.
- Attach both final Word and Markdown files, and include any standalone revised chapter if the user asked to update a specific section.

## Researching Chinese Companies

Search engines and data sources behave very differently for Chinese companies than for Western ones. Read `references/search-methodology.md` before starting a Chinese-language research task. Key rules of thumb:

- **Works:** `curl` with a desktop User-Agent against Sina Finance (`finance.sina.com.cn`) and nfnews.com (南方+); DuckDuckGo HTML search (`duckduckgo.com/html/?q=...`) for discovery, spacing queries apart to avoid rate limiting; browser navigation plus console extraction of `.article-content` for 界面新闻, 财联社 and 21经济报道.
- **Avoid:** curl scraping of Bing, Baidu or Baidu Baike (JS-rendered or CAPTCHA-protected), and Google search curl from non-US IPs.
- **Query patterns:** company name plus 招股书 / 上市 / 财务数据 / 股东 / 增资 / 估值 / 处罚 / 证监局; add Wind数据 or 排名 for securities firms and other ranking-driven sectors.
- **Financial data priority:** Sina Finance articles, then company annual reports and prospectuses, then Wind or 东方财富 Choice data cited in media, then company IR pages.

## Source Repository

GitHub: https://github.com/CoreyZhangKW/CZtoolkit
Path: `skills/ipo-company-research/`
