You are given an existing business dashboard UI. Your task is to restructure the navigation, page hierarchy, and filter logic ONLY, without modifying any existing UI elements, components, charts, tables, or visual styling.
STRICT CONSTRAINTS
Do NOT redesign UI components
Do NOT change layout styling, colors, or visual hierarchy
Do NOT remove or add new widgets
ONLY reorganize pages, sections, and filters
Preserve all existing data representations
CURRENT STRUCTURE
The current dashboard consists of:
Overview Page
Channel Page
Product Page
Customer Page
Insights Page
TARGET STRUCTURE
PRIMARY PAGES (Reduce to 3 pages only)
Overview
Business KPI View
SIP KPI Overview
PAGE LOGIC
1. Overview Page
Remains as-is (no structural change except adding sidebar filters)
2. Business KPI View
3. SIP KPI Overview
Both pages must follow IDENTICAL STRUCTURE:
Each page contains 4 SECTIONS:
Location
Channel
Customer
Product
These sections are NOT separate pages — they are internal views/tabs within the page.
SIDEBAR FILTER SYSTEM (CRITICAL)
A dynamic sidebar filter must be present on ALL pages.
CORE BEHAVIOR:
Filters must adapt based on the selected section
The FIRST filter = selected section
Remaining filters follow in logical order
FILTER ORDER LOGIC
If user selects:
Location section:
Location (Primary)
Customer
Channel
Product
Channel section:
Channel
Location
Customer
Product
Customer section:
Customer
Location
Channel
Product
Product section:
Product
Location
Customer
Channel
ADVANCED FILTERS (Must be included in sidebar)
Add the following filters EXACTLY as defined:
1. Competitive Comparison (Checkboxes)
Industry better than us
Us better than industry
2. Market Share
Slider control
3. Growth / Change Percentage
Formula:
(curr - prev) / prev * 100
Metrics:
AAUM
Gross Sales (GS)
Net Sales (NS)
Time frames:
MTD
QTD
YTD
(UI: slider or range selector)
4. Sales Filter
Gross Sales
Net Sales
5. Industry + Us
Combined dataset filter (subset of competitive comparison)
6. Emerging Filters (Time Horizon Based)
Time horizons:
3M
6M
9M
12M
Metrics:
AAUM
GS
NS
Scope:
Industry
ABSL
IMPORTANT: Apply ONLY to “Emerging” category
7. Institutional Filters
a. Institutional (Insti)
Condition: Net Sales = 0
b. Peak AUM Filter
Column-level filter inside table
Condition: Peak AUM > slider value
c. Opportunity Filter
Condition: (Current AUM - Peak AUM) > 1 lakh
d. Institutional Type
Conventional
Non-Conventional
8. Emerging Channel / MFD Filter
Based on classification:
Institutional
Retail
OUTPUT EXPECTATION
Generate:
Updated navigation structure (3 pages only)
Page-wise section breakdown
Sidebar filter interaction logic
Flow of how user moves between:
Overview → Business KPI → SIP KPI
Sections within each page
Wireframe-level structure (no styling changes)
Ensure the output is structured, hierarchical, and implementation-ready.
