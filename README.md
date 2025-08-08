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

This document contains 649 rows (650 including the header) and represents student records from two Portuguese schools: Gabriel Pereira (GP) and Mousinho da Silveira (MS).

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
|32. G2|Final grade (Target variable)|Integer (0–20)|

## Cloud IDE Reminders

To log into the Heroku toolbelt CLI:

1. Log in to your Heroku account and go to _Account Settings_ in the menu under your avatar.
2. Scroll down to the _API Key_ and click _Reveal_
3. Copy the key
4. In the terminal, run `heroku_config`
5. Paste in your API key when asked


You can now use the `heroku` CLI program - try running `heroku apps` to confirm it works. This API key is unique and private to you so do not share it. If you accidentally make it public then you can create a new one with _Regenerate API Key_.


## Dataset Content
* Describe your dataset. Choose a dataset of reasonable size to avoid exceeding the repository's maximum size and to have a shorter model training time. If you are doing an image recognition project, we suggest you consider using an image shape that is 100px × 100px or 50px × 50px, to ensure the model meets the performance requirement but is smaller than 100Mb for a smoother push to GitHub. A reasonably sized image set is ~5000 images, but you can choose ~10000 lines for numeric or textual data. 


## Business Requirements
* Describe your business requirements


## Hypothesis and how to validate?
* List here your project hypothesis(es) and how you envision validating it (them) 


## The rationale to map the business requirements to the Data Visualizations and ML tasks
* List your business requirements and a rationale to map them to the Data Visualizations and ML tasks


## ML Business Case
* In the previous bullet, you potentially visualized an ML task to answer a business requirement. You should frame the business case using the method we covered in the course 


## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).



## Unfixed Bugs
* You will need to mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation is not a valid reason to leave bugs unfixed.

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-24](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis and Machine Learning Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


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

