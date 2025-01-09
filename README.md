# Core Web Vitals Analysis Tool

Analyze Core Web Vitals (CWV) metrics like Largest Contentful Paint (LCP), Cumulative Layout Shift (CLS), and First Input Delay (FID) using Python. This project cleans data, creates visualizations, and provides summary statistics to help optimize web performance.

## Features
- Clean and preprocess CWV metrics.
- Generate visualizations:
  - LCP and CLS histograms.
  - Scatter plot for LCP vs CLS.
- Display key metrics, including missing FID counts.

## Setup
1. Install dependencies:
   ```
   pip install pandas matplotlib
   ```
2. Ensure the dataset `crux_cwv_metrics_cleaned_origins.csv` is in the project directory.
3. Run the analysis:
   - Jupyter Notebook:
     ```
     jupyter notebook find_cwv_for_top_10.ipynb
     ```
   - Python Script:
     ```
     python find_cwv_for_top_10.py
     ```

## Output
- **Visualizations**:
  - LCP and CLS distributions.
  - LCP vs CLS scatter plot.
- **Summary**:
  - Total number of origins.
  - Valid origins (non-missing LCP and CLS).
  - Missing FID count.

## Example Input Data
| Origin       | LCP (ms) | CLS   | FID (ms) |
|--------------|----------|-------|----------|
| example.com  | 2500     | 0.1   | 30       |
| testsite.org | 3200     | 0.05  | NaN      |

## License
MIT License. See LICENSE file for details.
