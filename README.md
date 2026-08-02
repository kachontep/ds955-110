# Executive Business Analytics Dashboard (Quarto + R)

An example interactive business analytics dashboard built with **Quarto** and **R** (`ggplot2`, `plotly`, `DT`, `dplyr`). Designed for seamless deployment to **GitHub Pages**.

---

## 📊 Dashboard Features

- **KPI Value Boxes**: Key metrics highlighting Total Revenue, Profit, Profit Margins, and Transaction Counts.
- **Interactive Visualizations**:
  - Monthly Revenue Trend by Region (interactive line chart powered by `plotly`).
  - Revenue Share by Product Category (interactive pie chart).
  - Profitability by Customer Segment (bar chart).
  - Sales vs. Profit Relationship (scatter plot with regression trends).
- **Data Table**: Filterable and searchable transaction data table powered by `DT`.
- **Multi-Tab Navigation**: Clean structure separating Overview metrics and Detailed Data.

---

## 🚀 How to Run Locally

### Prerequisites
- [R](https://cloud.r-project.org/) (version 4.0+)
- [Quarto CLI](https://quarto.org/) (bundled with RStudio or standalone executable)
- R packages: `dplyr`, `ggplot2`, `plotly`, `DT`, `scales`, `viridisLite`

To install the required R packages in R console:
```r
install.packages(c("dplyr", "ggplot2", "plotly", "DT", "scales", "viridisLite"))
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

### Option 1: Automatic Deployment via GitHub Actions (Recommended)

This repository includes a pre-configured GitHub Actions workflow at [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

1. Push your repository to GitHub:
   ```bash
   git add .
   git commit -m "Add Quarto R dashboard"
   git push origin main
   ```
2. In your GitHub repository:
   - Go to **Settings** > **Pages**.
   - Under **Build and deployment** > **Source**, select **GitHub Actions**.
3. Every commit to `main` will automatically build and publish your dashboard!

### Option 2: Publish via Command Line

Alternatively, you can publish directly using Quarto's CLI:

```bash
quarto publish gh-pages
```

---

## 📁 Repository Structure

```text
├── .github/
│   └── workflows/
│       └── deploy.yml    # GitHub Actions workflow for GitHub Pages
├── _quarto.yaml          # Quarto project metadata & layout configuration
├── index.qmd             # Main Quarto R Dashboard source document
├── .gitignore            # Git ignore rules for R and Quarto artifacts
└── README.md             # Project documentation
```
