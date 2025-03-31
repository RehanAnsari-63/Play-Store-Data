# App Data and Reviews Analysis

## Overview
This project involves analyzing app data and user reviews to explore relationships between app ratings and sentiment polarity of reviews. The dataset includes information about mobile apps (e.g., ratings, installs, size) and their corresponding user reviews (e.g., sentiment polarity, subjectivity). The analysis is performed using Python with libraries such as Pandas, Matplotlib, and Seaborn.

## Project Structure
- **`apps_data.csv`**: Dataset containing app metadata (e.g., app name, category, rating, reviews, size, installs).
- **`reviews_data.csv`**: Dataset containing user reviews with sentiment analysis (e.g., translated review, sentiment, polarity, subjectivity).
- **`analysis.ipynb`**: Jupyter Notebook with the full analysis script (data loading, cleaning, merging, visualization, and correlation calculation).

## Prerequisites
To run this project, you need the following installed:
- Python 3.x
- Required Python libraries:
  - `pandas`
  - `matplotlib`
  - `seaborn`

You can install the dependencies using pip:
```bash
pip install pandas matplotlib seaborn
```

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. Navigate to the project directory:
   ```bash
   cd your-repo-name
   ```
3. Ensure the datasets (`apps_data.csv` and `reviews_data.csv`) are in the same directory as the notebook.
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook analysis.ipynb
   ```
5. Run all cells in the notebook to execute the analysis.

## Analysis Steps
1. **Data Loading**: Load `apps_data.csv` and `reviews_data.csv` into Pandas DataFrames.
2. **Data Cleaning**:
   - Handle missing values by dropping rows with NaN in critical columns (e.g., `Rating`, `Sentiment_Polarity`).
   - Remove duplicates from the apps dataset.
   - Convert `Size` and `Installs` columns to numeric formats.
3. **Data Merging**: Merge the apps and reviews datasets on the `App` column using a left join.
4. **Exploratory Data Analysis**:
   - Display basic statistics and data info.
   - Visualize the relationship between `Sentiment_Polarity` and `Rating` using a scatter plot.
5. **Correlation Calculation**: Compute the Pearson correlation between `Sentiment_Polarity` and `Rating`.

## Results
- **Scatter Plot**: A scatter plot is generated to visualize the relationship between sentiment polarity and app ratings (see `analysis.ipynb` for the output).
- **Correlation**: The correlation between `Sentiment_Polarity` and `Rating` is approximately `0.046`, indicating a very weak positive relationship.

## Sample Output
- **Scatter Plot**: Displays sentiment polarity (x-axis) vs. ratings (y-axis) with a slight spread, suggesting no strong linear relationship.
- **Correlation Value**: `0.046445404101646014` (weak positive correlation).

## Dependencies
- Python 3.x
- Pandas: For data manipulation and analysis.
- Matplotlib: For basic plotting.
- Seaborn: For enhanced visualization.

## Notes
- The datasets (`apps_data.csv` and `reviews_data.csv`) are assumed to be available in the repository or provided by the user.
- The analysis assumes that the datasets are structured as shown in the notebook (e.g., column names like `App`, `Rating`, `Sentiment_Polarity`).
- The scatter plot is saved in the notebook output but can be modified to save as a file if needed.

## Future Improvements
- Add more visualizations (e.g., box plots, histograms) to explore other aspects of the data.
- Incorporate additional features (e.g., `Installs`, `Category`) into the analysis.
- Handle edge cases (e.g., outliers in `Rating` or `Sentiment_Polarity`) more robustly.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For questions or contributions, feel free to open an issue or contact the repository owner.
