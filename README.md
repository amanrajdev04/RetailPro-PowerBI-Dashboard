# RetailPro-PowerBI-Dashboard
Power BI portfolio project – Retail Sales, Product Performance and Regional Analysis.

1. Overview
Page	Purpose
1. Supermarket & Retail Chain Dashboard	Sales overview: totals, products, categories, regions, monthly trend, profitability by sub-category
2. Product Performance Dashboard	Which products earn or lose money, and how discounts affect profit
3. Regional Performance Dashboard	How each region and province performs on sales, margin and category profit

Shared design elements
•	Banner: navy rounded banner with the RetailPro logo, white page title and navigation buttons on the right.
•	Visual headers: slate-blue title bars with white bold centred text on every visual.
•	Slicers (left side): Year, Category and Region, synced across pages (View, Sync slicers).
•	Theme and background: Retail_Sales_Theme_Safe.json and the Panels background image. Colours: navy #1F3864, teal #2E86AB, orange #F18F01, green #2E8B57, red #C73E1D.
•	Navigation buttons: Action type Page navigation, same position on each banner.
2. Page 1: Retail Sales Overview
KPI cards
Card	Field	Notes
Total Orders	Total Orders	5,496 with no filters
Total Profit	Total Profit	$1.52M
Total Sales	Total Sales	Set decimal places to 2 so it reads $14.92M, not $15M
Profit Margin	Profit Margin %	10.20%

Charts
Visual	Type	Fields	Settings
Total Sales by Product Name	Clustered bar chart	Y-axis: Product Name
X-axis: Total Sales	Filter: Top N, 10 items, by Total Sales
Sort descending, data labels on
Total Sales by Product Category	Donut chart	Legend: Product Category
Values: Total Sales	Legend on the right
Total Sales and Total Profit by Region	Line and clustered column chart	X-axis: Region
Column: Total Sales
Line: Total Profit (secondary axis)	Sorted by sales, legend at top
Total Sales and Total Profit by MonthYear	Line chart	X-axis: MonthYear
Y-axis: Total Sales
Secondary: Total Profit	MonthYear sorted by YearMonthKey
Profitability by Category & Sub-Category	Clustered column chart	X-axis: Product Category, then Product Sub-Category
Values: Total Profit	Category to sub-category hierarchy; negative bars show losing sub-categories (Tables, Bookcases)

Navigation
•	Button Product Performance Analysis, destination page 2.
•	Button Regional Performance Analysis, destination page 3.
3. Page 2: Product Performance
KPI cards
Card	Field	Notes
Total Products	Total Products	1,263
Total Quantity	Total Quantity	215K
Avg Discount	Avg Discount %	4.97%
Loss-Making Products	Loss-Making Products	553 (44% of products)

Charts and table
Visual	Type	Fields	Settings
Top 10 Products by Profit	Clustered bar chart	Y-axis: Product Name
X-axis: Total Profit	Filter: Top N, 10 items, by Total Profit
Bars green #2E8B57
Bottom 10 Products by Profit	Clustered bar chart	Y-axis: Product Name
X-axis: Total Profit	Filter: Bottom N, 10 items, by Total Profit
Bars red #C73E1D
Discount vs profit	Scatter (bubble) chart	Values: Product Sub-Category
X-axis: Avg Discount %
Y-axis: Total Profit
Size: Total Sales	Averages cluster tightly (4.6% to 5.2%); discount bands would show the pattern more clearly
Product Details	Table	Product Name, Product Category, Total Sales, Total Profit, Profit Margin %, Total Quantity	Sorted by Total Sales descending; total row on; red/green font on Total Profit

Navigation
•	Button Retail Sales Overview, destination page 1.
•	Button Regional Performance Analysis, destination page 3.
4. Page 3: Regional Performance
KPI cards
Card	Field	Notes
Top Region	Top Region	West
Lowest Margin Region	Lowest Margin Region	Nunavut
Profit per Order	Profit per Order	276.89
Loss Order %	Loss Order %	62.35%

Charts and matrix
Visual	Type	Fields	Settings
Sales By Province	Treemap	Category: Province
Details: Region
Values: Total Sales	Used instead of a map because Map visuals are disabled by the tenant admin
Profit Margin % by Region	Clustered bar chart	Y-axis: Region
X-axis: Profit Margin %	Sorted descending; data labels on
Colour rules: 0 to <5% red #C73E1D, 5% and above green
Sales Trend By Region	Line chart	X-axis: Year
Y-axis: Total Sales
Legend: Region	Filter: Top N, 5 regions, by Total Sales; legend at top
Region - Category Profit Matrix	Matrix	Rows: Region
Columns: Product Category
Values: Total Profit	Background colour gradient (red low, yellow middle, green high); totals on

Navigation
•	Button Retail Sales Overview, destination page 1.
•	Button Product Performance Analysis, destination page 2.
5. Interactivity
•	Cross-filtering: clicking a bar, slice or province filters the other visuals on the page (Format, Edit interactions controls this).
•	Slicer sync: Year, Category and Region are synced and visible on all three pages.
•	Page navigation: Ctrl + click on buttons in Desktop; plain click after publishing.
6. Known polish items
•	Page 1: Total Sales card shows $15M; set decimals to 2.
•	Page 3: matrix total shows a long decimal value; set the measure's decimal places to 0 or 2.
•	Page titles use different patterns (Supermarket & Retail Chain Dashboard, Product Performance Dashboard, Regional Performance Dashboard); consider one naming style.
•	Discount vs profit chart: group discounts into bands (0%, 1 to 10%, 11 to 20%, over 20%) to show losses at high discounts.

