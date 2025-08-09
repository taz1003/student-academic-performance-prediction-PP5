# ![Project image](static/images/mainImage.png)

# Student Academic Performance Analysis

This project is part of the five milestone projects within the Full Stack Developer course offered by Code Institute. It is the final project in this course and represents my chosen path in Predictive Analytics. The initial concept for this project revolves around 'working with data'.

In this project, you will be guided step by step through the entire process, from data cleaning to feature engineering. The content has been personalized to create a welcoming atmosphere, helping you gain a thorough understanding of each individual step, including what I did and how I accomplished it.

If you ever feel confused, please refer back to the README file, where you will find a wealth of important information relevant to the project.

The live application can be found [here].

## Dataset Content

The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/larsen0966/student-performance-data-set).

**What is Kaggle?**

- Kaggle is an online community platform for data scientists and machine learning enthusiasts.
- Kaggle allows users to collaborate with other users, find and publish datasets, use GPU integrated notebooks, and compete with other data scientists to solve data science challenges.

In this project, I created a fictional user story. However, the predictive analytics conducted could be applied to a real project in the workplace.

### About the dataset

This dataset contains 649 rows (650 including the header) and represents student records from two Portuguese schools: Gabriel Pereira (GP) and Mousinho da Silveira (MS). This data approaches the students' academic achievement in secondary education. The data attributes include student grades, demographic, social and school related features and it was collected by using school reports and questionnaires.

This dataset contains student profiles, such as:

- demographic information;

- family background;

- study habits;

- extracurricular activities;

- access to resources;

- previous grades.

For each student, the dataset includes features describing their personal and academic background, as well as their final grade in Portuguese (G3), which will be used as the target variable for prediction.

In any part of the project where you don’t understand one of the variables used in the analysis, please refer to the table below.
Ordering starts from 0 to match the imported dataset.

---

|Variable|Meaning|Units/Categories|
|:----|:----|:----|
|0. school|Student's school|'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira|
|1. sex|Student’s gender|F = Female, M = Male|
|2. age|Age of the student|Integer (15–22 years)|
|3. address|Home address type|U = Urban, R = Rural|
|4. famsize|Family size|LE3 = ≤ 3 members, GT3 = > 3 members|
|5. Pstatus|Parent’s cohabitation status|T = Together, A = Apart|
|6. Medu|Mother’s education level|0 = None, 1 = Primary, 2 = 5–9th grade, 3 = Secondary, 4 = Higher|
|7. Fedu|Father’s education level|Same as Medu|
|8. Mjob|Mother’s occupation|teacher, health, services, at_home, other|
|9. Fjob|Father’s occupation|teacher, health, services, at_home, other|
|10. reason|Reason for choosing this school|home, reputation, course, other|
|11. guardian|Student’s guardian|mother, father, other|
|12. traveltime|Home-to-school travel time|1 = <15 min, 2 = 15–30 min, 3 = 30–60 min, 4 = >1 hour|
|13. studytime|Weekly study time|1300 - 215245|
|14. failures|Number of past class failures|Integer (0–4)|
|15. schoolsup|Extra educational support|yes / no|
|16. famsup|Family educational support|yes / no|
|17. paid|Extra paid classes in subject|yes / no|
|18. activities|Extra-curricular activities|yes / no|
|19. nursery|Attended nursery school|yes / no|
|20. higher|Plans for higher education|yes / no|
|21. internet|Internet access at home|yes / no|
|22. romantic|In a romantic relationship|yes / no|
|23. famrel|Quality of family relationships|Scale: 1 (very bad) - 5 (excellent)|
|24. freetime|Free time after school|Scale: 1 (very low) - 5 (very high)|
|25. goout|Going out with friends|Scale: 1 (very low) - 5 (very high)|
|26. Dalc|Workday alcohol consumption|Scale: 1 - (very low) - 5 (very high)|
|27. Walc|Weekend alcohol consumption|Scale: 1 - (very low) - 5 (very high)|
|28. health|Current health status|Scale: 1 (very bad) - 5 (very good)|
|29. absences|Number of school absences|Integer (0–93 days)|
|30. G1|First period grade|Integer (0–20)|
|31. G2|Second period grade|Integer (0–20)|
|32. G3|Final grade (Target variable)|Integer (0–20)|

## Cloud IDE Reminders

To log into the Heroku toolbelt CLI:

1. Log in to your Heroku account and go to _Account Settings_ in the menu under your avatar.
2. Scroll down to the _API Key_ and click _Reveal_
3. Copy the key
4. In the terminal, run `heroku_config`
5. Paste in your API key when asked

You can now use the `heroku` CLI program - try running `heroku apps` to confirm it works. This API key is unique and private to you so do not share it. If you accidentally make it public then you can create a new one with _Regenerate API Key_.

## Agile methodology - Development

- In the beginning of the project I decided to create a Kanban project, where to input 'issues', the idea was to help me in following a
direction while building this project.
- The kanban board for this project can be found in this [url](https://github.com/users/taz1003/projects/4/views/1).

## Crisp-DM, what is it and how is it used?

CRISP-DM, which stands for CRoss Industry Standard Process for Data Mining, is a process model that serves as the foundation for data science projects.

CRISP-DM consists of six sequential phases:

1. **Business Understanding** - What are the business requirements?
2. **Data Understanding** - What data do we have or need? Is the data clean?
   - Remember, "garbage in, garbage out," so it’s essential to ensure your data is properly cleaned.
3. **Data Preparation** - How will we organize the data for modeling?
4. **Modeling** - Which modeling techniques should we use?
5. **Evaluation** - Which model best aligns with the business objectives?
6. **Deployment** - How will stakeholders access the results?

For a more in-depth understanding of each phase and how to implement them, please refer to [CRISP-DM](https://www.datascience-pm.com/crisp-dm-2/).

## Business Case Overview

An academic advising team at a Portuguese high school is interested in identifying the most important factors influencing students' academic performance, with a focus on their final grade (G3). The goal is twofold:

1. Understand how different background, lifestyle, and support-related attributes correlate with student outcomes.
2. Predict final performance to better support at-risk students through early intervention.

The client has access to a publicly available dataset containing student demographic data, family background, academic behavior, and personal circumstances. This data provides a unique opportunity to explore and model the key factors influencing final academic performance.

## Rationale to map the business requirements to the Data Visualizations and ML tasks

### Business Requirement 1 : **Understand which factors most influence students' academic performance.**

- The client expects to explore correlations and patterns between variables such as parental education, study time, relationship status, internet access, family support, and other lifestyle indicators, with the final academic grade (G3) -
  1. Visual analysis of the most influential features
  2. Insights into how specific features affect student success

### Business Requirement 2 : **Predict a student's final grade based on their profile and behavior.**

- The client wants a predictive model that can estimate a student's final grade using the available features. This will help academic staff assess performance risks and guide targeted interventions -
  1. Predictive system embedded into a dashboard
  2. Real-time input widgets to test predictions based on hypothetical or real student profiles

## Hypothesis

### Hypothesis One

We suspect that students who dedicate more weekly study time tend to achieve higher final grades.

- A correlation study between 'studytime' and 'G3' can help investigate this relationship.

### Hypothesis Two

Parents maybe?

- A Correlation study can help in this investigation.

### Hypothesis Three

Absence rate?

- A Correlation study can help in this investigation.

### Hypothesis Four

Alchohol intake Dalc and Walc negatively impacting G3?

- A Correlation study can help in this investigation.

### Hypothesis Five

Hopefully better family relationships :D

- A Correlation study can help in this investigation.

## ML Business Case

### Predict Final grade (G3)

## Dashboard Design

## Unfixed Bugs

## Deployment

The master branch of this repository has been used for the deployed version of this application.

### Using Github & VSCode

To deploy my Data application, I used the [Code Institute milestone-project-bring-your-own-data Template](https://github.com/Code-Institute-Solutions/milestone-project-bring-your-own-data).

- Click the 'Use This Template' button.
- Add a repository name and brief description.
- Click the 'Create Repository from Template' to create your repository.
- To create a workspace you then need to click 'Code', then 'Create codespace on main', this can take a few minutes.
- When you want to work on the project it is best to open the workspace from 'Codespaces' as this will open your previous workspace rather than creating a new one. You should pin the workspace so that it isn't deleted.
- Committing your work should be done often and should have clear/explanatory messages, use the following commands to make your commits:
  - `git add .`: adds all modified files to a staging area
  - `git commit -m "A message explaining your commit"`: commits all changes to a local repository.
  - `git push`: pushes all your committed changes to your Github repository.

### Forking the GitHub Repository

By forking the GitHub Repository you will be able to make a copy of the original repository on your own GitHub account allowing you to view and/or make changes without affecting the original repository by using the following steps:

1. Log in to GitHub and locate the [GitHub Repository](repo here???)
2. At the top of the Repository (not top of page) just above the "Settings" button on the menu, locate the "Fork" button.
3. You should now have a copy of the original repository in your GitHub account.

### Making a Local Clone

1. Log in to GitHub and locate the [GitHub Repository](https://github.com/Code-Institute-Solutions/milestone-project-heritage-housing-issues)
2. Under the repository name, click "Clone or download".
3. To clone the repository using HTTPS, under "Clone with HTTPS", copy the link.
4. Open commandline interface on your computer
5. Change the current working directory to the location where you want the cloned directory to be made.
6. Type `git clone`, and then paste the URL you copied in Step 3. `$ git clone (paste url)`
7. Press Enter. Your local clone will be created.

### Deployment To Heroku

- The App live link is: (paste url)
- The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly in case all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.

---

## Main Data Analysis and Machine Learning Libraries

|Libraries Used In The Project|How I Used The Library|Link|
|:----|:----|:----|
|Numpy|Used to process arrays that store values and aka data|[URL](https://numpy.org/)|
|Pandas|Used for data analysis, data exploration, data manipulation,and data visualization|[URL](https://pandas.pydata.org/)|
|Matplotlib|Used for graphs and plots to visualize the data|[URL](https://matplotlib.org/)|
|Seaborn|Used to visualize the data in the Streamlit app with graphs and plots|[URL](https://seaborn.pydata.org/)|
|ML: feature-engine|Used for engineering the data for the pipeline|[URL](https://feature-engine.readthedocs.io/en/latest/)|
|ML: Scikit-learn|Used to creat the pipeline and apply algorithms, and feature engineering steps|[URL](https://scikit-learn.org/stable/)|
|Streamlit|Used for creating the app to visualize the project's study|[URL](https://streamlit.io/)|
|Kaggle|Used to import the dataset required to perform the analysis|[URL](https://www.kaggle.com/)|
|Grammarly|Used to improve, modify or add written communications throughout the project|[URL](https://app.grammarly.com/)|

## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page were taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.

