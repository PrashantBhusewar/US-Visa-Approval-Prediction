# US-Visa-Approval-Prediction

### About
The Immigration and Nationality Act (INA) of the US permits foreign workers to come to the United States to work on either a temporary or permanent basis. 
The act also protects US workers against adverse impacts on the workplace and maintains requirements when they hire foreign workers to fill workforce shortages. The immigration programs are administered by the Office of Foreign Labor Certification (OFLC).

### Problem statement.
* OFLC gives job certification applications for employers seeking to bring foreign workers into the United States and grants certifications. 
* last year, the number of employees was huge, so OFLC needs Machine learning models to shortlist visa applicants based on their previous data.

### Dataset is taken from Kaggle and stored in GitHub as well as inside the notebook directory 
https://www.kaggle.com/datasets/moro23/easyvisa-dataset

### Features in Datasets:
The data contains the different attributes of the employee and the employer. The detailed data dictionary is given below.

- `case_id`: ID of each visa application
- `continent`: Information of continent the employee
- `education_of_employee`: Information of the education of the employee
- `has_job_experience`: Does the employee have any job experience? Y= Yes; N = No
- `requires_job_training`: Does the employee require any job training? Y = Yes; N = No
- `no_of_employees`: Number of employees in the employer's company
- `yr_of_estab`: Year in which the employer's company was established
- `region_of_employment`: Information on foreign worker's intended region of employment in the US.
- `prevailing_wage`: Average wage paid to similarly employed workers in a specific occupation in the area of intended employment. The purpose of the prevailing wage is to ensure that the foreign worker is - not underpaid compared to other workers offering the same or similar service in the same area of employment.
- `unit_of_wage`: Unit of prevailing wage. Values include Hourly, Weekly, Monthly, and Yearly.
- `full_time_position`: Is the position of work full-time? Y = Full-Time Position; N = Part-Time Position
- `case_status`: Flag indicating if the Visa was certified or denied

### Models Used
* Logistic Regression
* KNeighbors Classifier
* XGB Classifier
* CatBoost Classifier
* RandomForest Classifier

From these above models after hyperparameter optimization, we selected the Top two models which were XGBRegressor and Random Forest Regressors and used the following in Pipeline.

* GridSearchCV is used for Hyperparameter Optimization in the pipeline.

👨‍💻 Tech Stack Used
1. Python
2. FastAPI
3. Machine learning algorithms
4. Docker
5. MongoDB

🌐 Infrastructure Required.
1. AWS S3
2. AWS EC2
3. AWS ECR
4. Git Actions
5. Terraform

### `US_Visa` is the main package folder which contains 

**Artifact** : Stores all artefacts created from running the application

**Components** : Contains all components of the Machine Learning Project
- DataIngestion
- DataValidation
- DataTransformations
- ModelTrainer
- ModelEvaluation
- ModelPusher
