# Data Science Salaries on US Marketplace

** Data Science Salaries** is a comprehensive data analysis project of data science job salaries in 2025, designed to explore and analyse data, with deep dive into salary trends and visualisation. 

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* The Dataset containes 151445 entries with 11 columns including a period time from 2020 to 2025, covering salary, type of employment, experience levels, company size and geographical data.
* Column Descriptions:

     * work_year: covers salaries from 2020 through 2025.

     * experience_level: 
        * EN: Entry-level / Junior
        * MI: Mid-level / Intermediate
        * SE: Senior-level
        * EX: Executive / Director

     * employment_type:
        * FT: Full-time
        * PT: Part-time
        * CT: Contract
        * FL: Freelance

     * job_title

     * salary: the employee's gross annual salary in the original reported currency, before taxes and deductions.

        * salary_currency: the currency in which the salary was originally paid.

        * salary_in_usd: the employee's salary converted into USD using 2025 exchange rates for standardized comparison.

     * employee_residence: the country where the employee resides.

     * remote_ratio: indicates the percentage of remote work:
        * 0: No remote work (On-site)
        * 50: Hybrid (partially remote)
        * 100: Fully remote

     * company_location

     * company_size
        * S: Small (1–50 employees)
        * M: Medium (51–500 employees)
        * L: Large (501+ employees)


## Business Requirements
* The project is focused to analyse salary trends and how they vary across year, title and location.

## Hypothesis and how to validate? 
* Hypothesis 1: Data science salaries have increased year-over-year from 2020 to 2025.
   * Validation: Analyze the trend of average salaries by year using line and area plots. Perform statistical tests (e.g., linear regression) to confirm a significant upward trend.
   
* Hypothesis 2: Salary levels vary significantly by company size and location.
   * Validation: Visualize salary distributions by company size and location using box plots, treemaps, and sunburst charts. Use group-by analysis and statistical tests to confirm differences.

## Project Plan
* High-level steps taken for the analysis:
   * Data Collection: Obtained the raw salary dataset covering 2020–2025, including job, salary, and company attributes.
   * Data Cleaning & Processing: Dropping irrelevant columns.
   * Exploratory Data Analysis (EDA): Explored distributions, trends, and relationships using summary statistics and visualizations (histograms, box plots, line plots).
   * Data Visualization: Used Matplotlib, Seaborn, and Plotly to create insightful plots (area, box, treemap, sunburst, scatter matrix) to address business questions and hypotheses.
  
* Data management throughout the project:
   * Collection: Downloaded and documented the source of the dataset: (https://www.kaggle.com/datasets/adilshamim8/salaries-for-data-science-jobs?resource=download&select=salaries.csv)
   * Processing: Cleaned and transformed the data using Pandas, ensuring consistency and accuracy.
   * Analysis: Performed EDA and hypothesis testing in Jupyter notebooks for reproducibility.
   * Interpretation: Documented insights and visualizations in the notebook and README for transparency.

* Rationale for chosen research methodologies:
   * Used EDA and visualization to quickly identify patterns, trends, and outliers in the data.
   * Used Jupyter notebooks for an interactive, iterative workflow and clear documentation of the analysis process.

## The rationale to map the business requirements to the Data Visualisations
The main business requirements and their mapping to data visualizations are:

1. **Understand salary trends over time**
   * Identifying how salaries change year-over-year helps stakeholders make informed decisions about compensation and hiring.

2. **Compare salaries across experience levels and job titles**
   * Understanding pay differences by role and seniority supports career planning and organizational structuring.
   
3. **Explore salary differences by company size and location**
   * Company size and geography influence compensation; visualizing these factors helps benchmark and strategize.
   
4. **Identify overall salary distribution and outliers**
   * Understanding the spread and anomalies in salary data is crucial for fair pay and risk management.
   

## Analysis techniques used
The main data analysis methods used in this project include:

 **Descriptive statistics**: Used to summarize and describe the main features of the dataset: mean, median, mode, standard deviation.
 **Data visualization**: Employed a variety of plots (histograms, box plots, line plots, area plots, treemaps, sunburst, scatter matrix) to explore distributions, trends, and relationships.
Used data visualization tools such as Matplotlib, Seaborn, and Plotly to analyze salary trends and differences across categories: year, experience level, remote ratio, company size, etc.

**Limitations and alternative approaches:**
 * No limitations were identified that impacted the analysis.

**Structure and justification:**
- The analysis was structured in a logical, step-by-step manner: data cleaning, EDA, feature engineering, visualization, statistical testing, and interpretation.
- This approach ensures transparency, reproducibility, and clear mapping from business questions to analytical results.
- Jupyter notebooks were used to document each step, making it easy to iterate and communicate findings.

**Data limitations and alternative approaches:**
 * No data limitations were identified that impacted the analysis.

**Use of generative AI tools:**
- Generative AI such as ChatGPT and Copilot was used for ideation, code optimization, and design thinking.
- AI tools helped generate code snippets for data cleaning, visualization, and statistical analysis, speeding up development.
- AI was also used to draft documentation, structure the analysis, and suggest alternative approaches or visualizations.

## Ethical considerations
* No data privacy, bias or fairness issues were identified.
* No legal or societal issues were identified.

## Unfixed Bugs
* No unfixed bugs are present in the project.

## Development Roadmap
* Challenges faced and strategies used:
   * Visualizing datasets in a way that is both informative and clear.
   * Visualization libraries with Plotly and created static images for GitHub compatibility.
   * Used Jupyter notebooks for step-by-step documentation and code execution, and version control with Git.
   * Exporting interactive plots as static images for sharing and GitHub display.
   * Integrated Kaleido with Plotly to export static images and embedded them in the notebook. 

## Main Data Analysis Libraries
The main data analysis libraries used in this project are:

- **pandas**  
   For data manipulation and analysis.  
   - Example: `df = pd.read_csv('dataset/processed/salaries_processed.csv')`
   - Example: `df.groupby('work_year')['salary_in_usd'].mean()`

- **numpy**  
   For numerical operations and array handling.  
   - Example: `import numpy as np`
   - Example: `np.mean(df['salary_in_usd'])`

- **matplotlib**  
   For static data visualization.  
   - Example: `plt.figure(figsize=(10,6))`
   - Example: `plt.boxplot(df['salary_in_usd'])`

- **seaborn**  
   For advanced statistical visualizations.  
   - Example: `sns.histplot(df['salary_in_usd'], kde=True)`
   - Example: `sns.pairplot(df[['salary_in_usd', 'work_year']])`

- **plotly**  
   For interactive and advanced visualizations.  
   - Example: `fig = px.area(df, x='work_year', y='salary_in_usd')`
   - Example: `fig.write_image('area_plot.png')`

- **kaleido**  
   For exporting Plotly figures as static images.  
   - Example: `fig.write_image('plot.png')`

### Content 
* Instructions on how to implement and present the information were adapted from various online resources:
   - [YouTube](https://www.youtube.com/)
   - [Wikipedia](https://www.wikipedia.org/)
   - [ChatGPT](https://chatgpt.com/)
   - [Code Institute Learning Platform](https://learn.codeinstitute.net/)
   - [Kaggle](https://www.kaggle.com/)

## Acknowledgements (optional)
* Thanks to Vasi who provided support through this project.
