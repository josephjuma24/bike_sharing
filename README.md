# Instructions for Bike Sharing Data Science Project

## Project Overview
This project analyzes a synthetic bike sharing dataset for 90 days, focusing on time-series and regression analysis. The main file is a Jupyter notebook (`bike_sharing.ipynb`) containing all code, documentation, and visualizations.

## Data Structure
- **DataFrame Columns:**
  - `date`: ISO date string (use pandas datetime)
  - `rides`: Integer, target variable
  - `temperature`: Float (°C)
  - `humidity`: Float (0-100%)
  - `windspeed`: Float (km/h)
- Data is generated in-notebook using NumPy and pandas, not loaded from external files.

## Key Patterns & Conventions
- **Notebook-Driven Workflow:** All code, analysis, and plots are in a single notebook. No scripts or modules.
- **Visualization:** Uses matplotlib and seaborn for histograms, time-series, and distribution plots. Example:
  ```python
  plt.figure(figsize=(8,5))
  sns.histplot(df['rides'], bins=15, kde=True)
  plt.title("Distribution of Rides")
  plt.show()
  ```
- **Data Exploration:** Always print DataFrame shape, columns, and info before analysis:
  ```python
  print("Dataset Shape:", df.shape)
  print("\nColumns:", df.columns.tolist())
  print("\nDataset Info:")
  print(df.info())
  ```
- **Random Seed:** Set with `np.random.seed(42)` for reproducibility.
- **No External Data:** All data is generated in the notebook; do not expect CSV or external sources.

## Developer Workflow
- **Run All Cells:** Execute notebook cells top-to-bottom for reproducible results.
- **Dependencies:**
  - pandas
  - numpy
  - matplotlib
  - seaborn
- **Environment Setup:** Use a Python environment with the above packages installed. No special build or test commands.
- **Debugging:** Use print statements and plot outputs for diagnostics.

## Integration Points
- No external APIs, files, or services.
- All logic is self-contained in the notebook.

## Examples
- Plotting rides over time:
  ```python
  plt.figure(figsize=(8,6))
  plt.plot(df['date'], df['rides'], marker="o")
  plt.title("Rides Over Time")
  plt.xlabel("Date")
  plt.ylabel("Number of Rides")
  plt.xticks(rotation=45)
  plt.show()
  ```

## Summary
- Focus on notebook cell code and markdown.
- Follow the established patterns for data generation, exploration, and visualization.
- No need for file I/O, external data, or multi-file architecture.
