
# Mini Project - Data Analysis

## **Overview**

This project is part of a data analysis journey focused on understanding university enrollment data. The data includes information about students enrolling in courses offered in two formats: online and on-campus. The objective is to analyze how these formats affect student enrollment and to explore other variables such as pre-scores, post-scores, department affiliations, and prerequisites.

## **Dataset Description**

The dataset provided for this project includes the following features:

- **Course Type:** Whether the course is offered online or on-campus.
- **Pre-Score:** The score of the student before taking the course.
- **Post-Score:** The score of the student after completing the course.
- **Department:** The department offering the course.
- **Prerequisites:** Any prerequisites required for the course.
- **Enrollment:** The number of students enrolled in the course.

## **Approach**

The analysis is broken down into several key steps:

### 1. **Data Loading**

The dataset is loaded into a pandas DataFrame for processing.

### 2. **Data Cleaning**

To ensure that the analysis is accurate, the following steps were performed:

- Removal of null or missing values.
- Conversion of data into appropriate formats (e.g., categorical encoding for course types).
- Handling of outliers where necessary.
- Ensuring data consistency across all fields.

### 3. **Data Exploration and Visualization**

A variety of visualizations were created to better understand the relationships in the data:

- **Bar plots** to show the comparison between online and on-campus enrollments.
- **Box plots** to examine the spread of scores (pre and post) based on course type.
- **Scatter plots** to investigate potential correlations between pre-scores and post-scores.
- **Heatmaps** to visualize relationships between different variables, including course type and enrollment numbers.

### 4. **Conclusions**

Insights derived from the analysis include:

- A comparison of enrollment rates between online and on-campus courses.
- The effect of pre-requisites on student performance and enrollment.
- Trends in student performance based on course type (e.g., changes in pre- and post-scores).

## **Tools Used**

- **Python**: The main programming language used for data analysis.
- **Libraries**:
  - `pandas`: For data manipulation and loading.
  - `matplotlib`: For data visualization.
  - `numpy`: For numerical operations.
  - Additional libraries as needed (e.g., `seaborn` for advanced plots).

## **Project Files**

- **mni-project.ipynb**: Jupyter notebook containing the entire analysis, with detailed code and outputs.

## **How to Run the Project**

1. **Clone the repository** or download the Jupyter notebook (`mni-project.ipynb`).
2. Ensure that the following libraries are installed:
   - `pandas`
   - `numpy`
   - `matplotlib`
   - `seaborn` (optional, for advanced visualizations)
   
   You can install them using pip:

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. Open the Jupyter notebook:
   ```bash
   jupyter notebook mni-project.ipynb
   ```

4. Execute the cells step by step to run the analysis.

## **Future Enhancements**

Possible improvements to the project could include:

- Analyzing more features, such as student demographics.
- Using machine learning techniques to predict future enrollment trends.
- Automating the data cleaning process for more robust handling of different datasets.