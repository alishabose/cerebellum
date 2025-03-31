# Team CEREBELLUM (Women in Data Science)

## 👥 Team Members
| Name   | GitHub Handle      | Contribution |
|--------|--------------------|--------------|
| Alisha | [@alishabose](github.com/alishabose)         | Led the project, worked on data pre-processing and visualization |
| Emily  | [@emsteinnn](github.com/emsteinnn)          | Built and trained the model, handled data concatenation  |
| Krishi | [@krishishah05](github.com/krishishah05)    | Visualized data distributions and handled missing values |
| Anika  | [@aninuona](github.com/aninuona)           |  Focused on feature engineering and hyperparameter tuning |

## 🎯 Project Highlights
- Built a **Random Forest Classifier** using **multi-output classification** to predict an individual's **sex** and **ADHD diagnosis** based on functional and categorical metadata.
- Was graded on Kaggle's private dataset to get an accuracy score 
- Used **SHAP** for model explainability to interpret the decisions made by the classifier.
- Implemented **standardization** and **multi-output classification** to optimize results within compute constraints.

## 🔗 WiDS Datathon 2025 | Kaggle Competition Page
[WiDS Datathon 2025 Kaggle Link](https://www.kaggle.com/competitions/widsdatathon2025)

## 👩🏽‍💻 Setup & Execution
### Cloning the Repository
1. Clone this repository to your local machine by running the following command:
    ```bash
    git clone [https://github.com/cerebellum](https://github.com/alishabose/VIR-WiDS-Team-Cerebellum-)
    ```

### Installing Dependencies
2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Setting Up the Environment
3. Set up your Python environment (if necessary). For example, if you use `conda`:
    ```bash
    conda create --name widsdatathon python=3.8
    conda activate widsdatathon
    ```

### Accessing the Dataset(s)
4. Download the datasets from the Kaggle competition page and place them in the appropriate directories.

### Running the Notebook or Scripts
5. Run the code:
    ```bash
    jupyter notebook team-cerebellum.ipynb
    ```

## 🏗️ Project Overview
This project is part of the **WiDS Datathon 2025** in collaboration with **Break Through Tech AI Program**. The challenge focuses on building predictive models using neuroimaging data to determine ADHD diagnosis and sex based on patterns in brain activity. By doing so, the work aims to contribute to improving diagnostic accuracy for ADHD in males and females, providing more accurate and personalized treatment approaches.

## 📊 Data Exploration
The dataset provided in the Kaggle competition includes:
- **Categorical Metadata**: Information about participants, including demographics and behavioral data.
- **Functional Connectome Matrices (FCM)**: Data related to brain activity from neuroimaging.
- **Quantitative Metadata**: Neuroimaging measures for functional connectivity and brain regions.

### Data Preprocessing Approach:
- **Encoding categorical variables** using `pd.get_dummies`.
- **Handling missing values** by filling them with the mean of respective columns.
- **Feature scaling** using `StandardScaler` to normalize numeric features.
  
### Challenges:
- Dealing with missing values in large datasets.
- Aligning different data types (categorical, numeric, and matrix data).
  
### Visualizations:
- The visualizations range from a frequency chart of the distribution of 'emotional problem's diagnoses (1) to the count of ADHD prevalence by parent (2) which is another factor in ADHD diagnosis, to finally a graph of results with predicted to actual outcomes of diagnoses.
  
<img width="841" alt="Screenshot 2025-03-22 at 8 38 41 PM" src="https://github.com/user-attachments/assets/ad03bca0-c56f-40cf-ac3c-95e881d5a266" />
<img width="649" alt="Screenshot 2025-03-22 at 8 38 26 PM" src="https://github.com/user-attachments/assets/9b2a4774-8da3-4126-9c92-da77ff8ff80e" />
<img width="667" alt="Screenshot 2025-03-22 at 8 38 18 PM" src="https://github.com/user-attachments/assets/1a1ebf6c-59f7-45bf-881e-547a420b4dfc" />


## 🧠 Model Development
### Model Used:
- **Random Forest Classifier** was chosen for its ability to handle high-dimensional data and provide insights into feature importance.

### Feature Selection and Hyperparameter Tuning:
- Applied **multi-output classification** to predict both ADHD diagnosis and sex simultaneously.
- **GridSearchCV** could be used for hyperparameter tuning if further optimization is needed, provided having time to run and GPU capacity.

### Training Setup:
- Split the data into training and validation sets using `train_test_split`.
- Used **precision score** to evaluate the performance of the model.

## 📈 Results & Key Findings
### Performance Metrics:
- **Precision score**: 0.39120, with our best score being 0.42176, based on the model's performance in the Kaggle leaderboard.

### Key Findings:
- The model was able to identify brain activity patterns that distinguish between different ADHD diagnoses and sex categories. For ADHD research, this could be imperative in order for early and late intervention strategies. For example, being able to use this data could contribute massively to how clinicians perceive and diagnose ADHD—whereas currently ADHD is diagnoses less frequently in women, this could help bridge this gap.

### Visualizations:
- Visualizing data, specifically ADHD Outcome, Gender, and ADHD Prevalence
- Played around with other visualizations in the first submission, then boiled down to what was helpful
- Predicted vs Actual Outcome 

## 🖼️ Impact Narrative
ADHD is linked to brain activity patterns, specifically within the **default mode network** and **executive function regions**. ADHD diagnosis shows differences in male and female presentations, including varying attention and impulse control patterns. Better understanding of these differences through brain activity analysis will enhance diagnostic accuracy and treatment methods for ADHD.

## 🚀 Next Steps & Future Improvements
### Limitations:
- The current model’s performance is constrained by limited compute power on Kaggle (free CPU usage).
- We also struggled with improving our accuracy, specifically with the addition of a new training dataset towards the end of the competition.
  
### What Would You Do Differently With More Time/Resources?
- Apply advanced deep learning techniques such as **Convolutional Neural Networks (CNNs)** and **Graph Neural Networks (GNNs)** to capture more intricate patterns in brain activity.
- We could also do more hyperparameter tuning and if provided more time and efficiency, such as more  usage outside of Kaggle's capabilities, we would be able to run the model with more iterations.

### Additional Datasets or Techniques to Explore:
- Explore **ADHD Teen Integrative Data Analysis Longitudinal (TIDAL)** dataset, which focuses specifically on adolescents with ADHD.
- Use GridSearch for hyperparameter tuning in order to work on our accuracy score, and potentially L1 regularization in order to get rid of unncessary features and help with overfitting.
  
## 📄 References & Additional Resources
- Young, S., Adamo, N., Ásgeirsdóttir, B. B., Branney, P., Beckett, M., Colley, W., Cubbin, S., Deeley, Q., Farrag, E., Gudjonsson, G., Hill, P., … Woodhouse, E. (2020). Females with ADHD: An expert consensus statement taking a lifespan approach providing guidance for the identification and treatment of attention-deficit/ hyperactivity disorder in girls and women. *BMC psychiatry*, 20(1), 404. https://doi.org/10.1186/s12888-020-02707-9
