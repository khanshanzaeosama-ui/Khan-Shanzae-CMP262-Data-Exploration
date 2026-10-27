# CMP 262: Data Exploration, Cleaning, and Matplotlib

## GitHub Starter Repository

Use the following repository to access the Data Exploration, Cleaning, and Matplotlib starter files:

[**CMP 262 Data Exploration and Cleaning with Python Starter Repository**](https://github.com/ahedhli12/CMP262-Data-Exploration-and-Cleaning-with-Python)

### Getting Started

1. Open the starter repository using the link above.
2. Select **Use this template → Create a new repository**.
3. Choose your personal GitHub account as the owner.
4. Name your repository:

   **LastName-FirstName-CMP262-Data-Exploration**

5. Set your repository to **Public**.
6. Select **Create repository**.
7. Clone your newly created repository to your computer.
8. Open the cloned repository in **Visual Studio Code**.
9. Open **MatplotlibAssignment.ipynb**.
10. Make sure the `data/student_interest_survey.csv` file is available.
11. Complete all sections marked **TODO**.
12. Run and test all notebook cells.
13. Complete **AI-Use-Report.md**.
14. Save the cleaned CSV in the `cleaned-data` folder.
15. Save at least two chart images in the `charts` folder.
16. Commit and push your completed work to GitHub.
17. Include the link to your public GitHub repository in your Blackboard Ultra submission.

**Important:** Clone your own newly created repository, not the instructor's starter repository.

## Objective

Use pandas to explore and clean a small student-interest dataset, then use Matplotlib to create charts that communicate what you discover.

This assignment introduces Matplotlib for the first time. You will practice one chart at a time and explain what each chart shows.

## What You Need to Do

### Part 1: Load and inspect the data

- Import pandas and Matplotlib.
- Read `data/student_interest_survey.csv` into a pandas DataFrame.
- Display the first rows, dimensions, column names, data types, and missing-value counts.

### Part 2: Clean the data

- Standardize the column names.
- Remove duplicate rows.
- Decide how to handle missing values.
- Standardize inconsistent values in at least one text column.
- Confirm that the cleaned data is ready for analysis.

### Part 3: Create charts

Create all five charts below:

1. A bar chart that compares categories.
2. A histogram that shows the distribution of a numeric column.
3. A scatter plot that compares two numeric columns.
4. A line chart that uses sorted numeric data.
5. A pie chart that shows parts of a whole.

Every chart must include a clear title. Add axis labels when they apply. Use readable colors and an appropriate figure size.

### Part 4: Explain your results

After every chart, add a Markdown cell with two or three sentences explaining:

- What the chart displays.
- What pattern or result you notice.
- Why that result may matter.

### Part 5: Save your work

#### Save the notebook

Visual Studio Code normally saves the notebook when you press **Ctrl+S**. Save regularly while you work. Before submitting, select **Run All** and confirm that every cell runs without an error.

#### Save the cleaned data as a new CSV file

Do not overwrite the original file in the `data` folder. Use `to_csv()` to save the cleaned DataFrame in the `cleaned-data` folder:

```python
# Save the cleaned DataFrame as a different CSV file.
# index=False prevents pandas from adding an extra row-number column.
cleaned_survey.to_csv(
    "cleaned-data/student_interest_survey_cleaned.csv",
    index=False
)
```

#### Save a chart as an image

Place `plt.savefig()` after the chart instructions but before `plt.show()`:

```python
# Save the current chart in the charts folder.
plt.savefig("charts/my_chart.png", bbox_inches="tight")

# Display the chart inside the notebook.
plt.show()
```

Use a clear filename such as `major_bar_chart.png` or `interest_histogram.png`. Save at least two charts as PNG files.

#### Check that the files were created

Open the `cleaned-data` and `charts` folders in the Visual Studio Code Explorer. Confirm that the new CSV file and PNG files appear there. Do not submit empty folders.

#### Save the repository to GitHub

Saving with **Ctrl+S** saves files only on your computer. Use Git to send the saved files to GitHub:

```bash
git status
git add .
git commit -m "Complete Matplotlib assignment"
git push
```

Complete `AI-Use-Report.md`, then open your GitHub repository and verify that your notebook, cleaned CSV, chart images, and AI report appear there.

## Required Repository Files

- `MatplotlibAssignment.ipynb`
- `AI-Use-Report.md`
- `data/student_interest_survey.csv`
- `cleaned-data/student_interest_survey_cleaned.csv`
- At least two PNG chart files in `charts`

## Rubric: 100 Points

| Area | Points |
|---|---:|
| Load and explore the data | 15 |
| Clean the data | 20 |
| Five required charts | 35 |
| Titles, labels, colors, and readability | 10 |
| Written interpretation of charts | 10 |
| Saved CSV, saved charts, and organized repository | 5 |
| Completed AI Use Report | 5 |

## GitHub Submission

Your GitHub repository should include your completed:

- `MatplotlibAssignment.ipynb`
- `AI-Use-Report.md`
- `data/student_interest_survey.csv`
- `cleaned-data/student_interest_survey_cleaned.csv`
- At least two PNG chart files in the `charts` folder

Make sure your latest work has been committed and pushed before submitting the assignment.

Use these commands after completing or updating your work:

```bash
git status
git add .
git commit -m "Complete data exploration and Matplotlib assignment"
git push
```

Open your repository on GitHub and confirm that the latest version of your notebook, cleaned CSV, and chart images appear there.

## Blackboard Ultra Submission

Blackboard Ultra is the official submission location.

Submit the required assignment materials through Blackboard Ultra and include the link to your public GitHub repository.

**Uploading work to GitHub alone does not count as submitting the assignment.**
