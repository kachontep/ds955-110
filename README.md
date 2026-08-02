# Product Sales Analytics Dashboard (Quarto + R)

An interactive product transactions analytics dashboard built with **Quarto** and **R** (`ggplot2`, `plotly`, `crosstalk`, `dplyr`, `readr`, `lubridate`, `scales`). Designed for seamless deployment to **GitHub Pages**.

---

## 📊 Dashboard Features

- **Navbar Personal Details**: Displays **Kajornthep Piyanun 6910025010** on the right side of the navbar.
- **Interactive Crosstalk Filters**: Filter data in real time by:
  - Product Category (`รองเท้า`, `กางเกง`, `เสื้อ`, `กระเป๋า`)
  - Customer Region (`North`, `South`, `East`, `West`, `City`)
  - Product Color (`Black`, `White`, `Red`)
  - Product Size (`M`, `L`)
  - Customer Gender (`Female`, `Male`)
- **KPI Value Boxes**: Highlighting Total Revenue (฿917,000), Total Items Sold (999), Unique Customers (10), and Average Item Price (฿917.9).
- **Interactive Visualizations (Plotly & ggplot2)**:
  - **Daily Sales Revenue Trend**: Time-series plot showing revenue over time by product line.
  - **Revenue Share by Product Category**: Interactive donut chart.
  - **Revenue by Customer Region**: Regional sales distribution bar chart.
  - **Revenue by Customer Age Range & Gender**: Grouped demographic sales bar chart.
- **Streamlined Single-Page Layout**: Clean layout optimized for executive overview.

---

## 🚀 How to Run Locally

### Prerequisites
- [R](https://cloud.r-project.org/) (version 4.0+)
- [Quarto CLI](https://quarto.org/) (bundled with RStudio or standalone executable)
- R packages: `dplyr`, `readr`, `lubridate`, `ggplot2`, `plotly`, `DT`, `crosstalk`, `scales`, `tidyverse`

To install the required R packages in R console:
```r
install.packages(c("dplyr", "readr", "lubridate", "ggplot2", "plotly", "DT", "crosstalk", "scales", "tidyverse"))
```

### Preview the Dashboard
Open your terminal in the project directory and run:

```bash
quarto preview index.qmd
```
*(If using RStudio's bundled Quarto executable on Windows, run `& "C:\Program Files\RStudio\resources\app\bin\quarto\bin\quarto.exe" preview index.qmd`)*

### Render Static Site
To generate the static HTML dashboard files in `_site/`:

```bash
quarto render index.qmd
```

---

## 🌐 Deploying to GitHub Pages

### Automatic Deployment via GitHub Actions

This repository includes a pre-configured GitHub Actions workflow at [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

1. Push your repository to GitHub:
   ```bash
   git add .
   git commit -m "Update Product Sales Analytics dashboard"
   git push origin main
   ```
2. In your GitHub repository:
   - Go to **Settings** > **Pages**.
   - Under **Build and deployment** > **Source**, select **GitHub Actions**.
3. Every commit to `main` will automatically build and publish your dashboard!

---

## 📁 Repository Structure

```text
├── .github/
│   └── workflows/
│       └── deploy.yml    # GitHub Actions workflow for GitHub Pages
├── dataset/
│   └── product-transactions.csv # Transaction dataset
├── _quarto.yaml          # Quarto project metadata & layout configuration
├── index.qmd             # Main Quarto R Dashboard source document
├── .gitignore            # Git ignore rules for R and Quarto artifacts
└── README.md             # Project documentation
```
