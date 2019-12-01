# dataScience30
## [Day 3: Workflow, Ethics & Forming a Problem Statement]()
#### By [Glitched Failure](https://www.youtube.com/channel/UCErSNiDZV4rJCNB8NrDGREA)
---
## Objectives
- Participants will have familiarity with the start of a data workflow
- Participants will have familiarity recognizing unethical uses of data
- Participants will gain experience forming a proper problem statement

---
## Code Along

### Workflow:
This is a general way to approach a data science problem. This is by no means exhaustive, but should be a good starting point in understanding proper workflow. It cannot be stressed enough how much of an __iterative process__ working with data is. You may discover during modeling that there's a feature you need to engineer or some cleaning you failed to do, which causes you to go back and start over - this is normal!

1. General Problem Statement
2. Research relevant data sources
3. Specific Problem Statement
4. Gather data
6. Preliminary EDA
5. Clean data
7. EDA
8. Feature Engineering/Selection
9. Model Preparation
10. Modeling
11. Model Evaluation
12. Model Selection
13. Conclusion
14. Publish or present

### Working with data ethically
Data is information, and information is power. It would not be out of line to say once you're equipped with data science as a tool, you will be capable of doing real harm if you are not taking cautionary steps.

One idea that has gained traction is the need for a kind of "Hippocratic Oath" for data scientists.  
The "Hippocratic Oath" is a pledge that medical professionals, like doctors, take stating they will "do no harm". There currently is no such pledge or oath for data scientist, but [a preliminary code of conduct is in the works](https://data.berkeley.edu/news/it%E2%80%99s-time-data-ethics-conversations-your-dinner-table), which will take time for the industry and tought leaders to come to a concensus on.

I bring this up because data is dangerous in the wrong hands, and I would be doing you, and the world, a disservice if I gave you a knife and only showed you HOW to use it without showing you WHEN to use it.

_Disclaimer_: By no means am I an expert on ethics! The topics discussed may provoke strong emotions and I encourage anyone taking this course to reflect on how you might view each situation from different perspectives. __This is NOT about right vs. wrong.__ These exercises are meant to spark the inner dialogue and self criticism any good scientist should have when deciding on WHEN to use the tools at their disposal.

### Ethical Scnarios
#### Scenario 1 - Predicting Recidivism - ([source](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)):
In criminal courts, judges are responsible for deciding everything from bail, to probation, to parole. Of course, judges are human and statistical analysis has consistently shown judges biased - particularly regarding race.  

Your company decides to help remove this bias by creating a machine learning model and training it on criminal data, which will NOT include race as part of its prediction, thereby removing that bias. You and your team make a model that can accurately predict _recidivism_, the likelihood a criminal will become a repeat offender, by giving a defendant a risk score. __This model will NOT decide on bail, probation, or parole__ - it will merely serve as a tool for judges to consider when making their decision. Judges will still have the ultimate decision in the process.

After employing the model, criminals from a minority background consistently have higher risk scores than other groups. Judges use this information to help make their decisions.


Take a few minutes to reflect:  
_Do you think this is ethical?_
<details>
    <summary>
        What happened?
    </summary>
        <p>
            Again, there is no right or wrong here - the point is to ingrain this step into your process. It is your responsibility to step back and reflect on the problem at hand along with a potential solution and think "is this ethical to do?"
        </p>
        <p>
            This scenario actually did happen, and researchers at Propublica found the risk-assessment algorithm held racial bias. Other factors related to race, such as socioeconomic factors, location, education, etc. were highly correlated to race. This is someting the creators did not factor into their model, so even though race was not an explicit feature, it was still being included indirectly.
        </p>
</details>

#### Scenario 2 - Ad Targeting - ([source](https://www.umbel.com/blog/big-data/7-big-data-blunders/))

Advertising is big business, and you can bet online advertisers will pay good money to know what kinds of things a user is searching for, clicking on, mousing over, and discussing.

Your company is an e commerce company, selling products online. There is a ton of data on each users buying habits, search history, and the kinds of items in their "basket" they have yet to purchase. You're assigned to categorize users into profiles, which allows for targeted advertising. For example, a use buying gaming consoles and college textbooks are likely to fit the "male teen" profile, and will be shown ads relevant to that demographic.

The Marketing Department also uses these profiles to also send targeted advertising to the user's mailing address.

Take a few minutes to reflect:  
_Do you think this is ethical?_

<details>
    <summary>
        What happened?
    </summary>
    <p>
        This scenario also happened. A user was searching for pre-pregnancy items and Target flagged the user as fitting the "pregnant woman" profile and began sending pregnacy ads to her address. This user happened to be a teenager living in her parents house and was struggling with how best to tell her parents about her pregnancy. She never got the chance to because her parents found the ads in the mail and angrily sought an explaination from Target, leading the parents to discovery the truth.
    </p>
    <p>
        After the story came out, customers complained how creeped out they felt that the company knew about their pregnancies in advance.
    </p>
</details>

### Creating a proper problem statement - ([source 1](https://towardsdatascience.com/defining-a-data-science-problem-4cbf15a2a461) & [source 2](https://towardsdatascience.com/dont-do-data-science-solve-business-problems-6b70c4ee0083))
A data scientist is like a javelin missile - serving as a solution for particular kinds of problems. And if you're trying to swat a fly, the javelin missile really isn't the best tool for the job.

Recognizing data science problems and forming those problems __correctly__ is the first step to finding the best data science solution. 
- Saying "I want to work with Twitter data!" is NOT stating a problem. 
- Saying "I want to know the average monthly purchase per user per region" is NOT stating a data science problem (this is data analysis, though! As in, you can query a database, group by region and calculate this number - no machine learning required).
- Saying "I have weather data, and I want to predict if it will rain tomorrow given today's humidity, wind direction, and other factors with over 50% accuracy" is a data science problem!

In the last case, notice how specific we are regarding the data, factors involved, and the evaluation metric (accuracy).

A data science problem may:
- Categorize or group data ("Is this an image of a cat or dog?")
- Identify patterns (Predicting the Stock Market)
- Identify anomalies (Fraud Detection)
- Show correlations (A/B Testing)
- Predict outcomes ("Will it rain tomorrow?")

Let's break down why the following problem statement works well:

#### As a person gets older, how does their income change?

Here, we're looking for correlation and we establish the features (age) and target variable (income).

This is the kind of general problem statement you might use to start the process of coming to a data science solution. Taking a look at our workflow, this is the very first step!

1. __General Problem Statement__
2. Research relevant data sources
3. Specific Problem Statement
4. Gather data
6. Preliminary EDA
5. etc...

Let's look at another one!

#### Looking at game data, which users are cheating?

This problem is about anomoly detection (or classification depending on how you look at it. Either way, it counts!). The dataset/input is mentioned, along with the target variable (whether or not a user is cheating).

Once you've established a __general problem statement__, you go on to gather the relevant data. And once you have a good understanding of the data available, you refine your general problem statement into a specific and final problem statement. 

### How to make a specific problem statement
Including some or all of these key elements will go a long way to making your final problem statement specific enough to hold up to scrutiny:
- Where is the data coming from?
- What key features do you want to use?
- What is the target variable?
- What model evaluation metric will you be using?
- What kind of model will you use?
- What is the intended decision making outcome or use case?

For example:

#### Based on a user's packet history, character location, and clicks per minute, we will create a binary classification model to determine if a user is cheating or not in order to reduce or eliminate cheating within our game. We will use f1 score to evaluate the model.

Yes, 2 sentences is fine!  
Here, we see the key features mentioned (packet history, character location, and clicks per minute), the kind of model (binary classification), the intended outcome (reduce cheating), as well as the model evaluation metric (f1).

#### Take 5 minute to come up with a __general problem statement__ for the following 2 scenarios:

1. Your healthcare company has patient data and are interested in detecting patients at risk for coronary heart disease.
    - <details>
            <summary>
                Possible General Problem Statements...
            </summary>
            <p>
                (Correlation) What factors are most important in predicting patient risk for coronary heart disease?
            </p>
            <p>
                (Classification) Based on a patient's profile, which patients are most at risk for developing coronary heart disease?
            </p>
            <p>
                And many more!
            </p>
        </details>

2. You work for the city government, and rainfall frequently causes the local river to flood various neighborhoods. This causes a lot of economic damage and the mayor looks to you to help create an early warning system.
    - <details>
        <summary>
            Possible General Problem Statement...
        </summary>
        <p>
            (Predicting outcomes) Based on local weather, neighborhood, and sewer status, what are the odds the river will flood tomorrow?
        </p>
        <p>
            (Identify patterns) What is the likelihood it will rain tomorrow and rain hard enough to cause the river to flood?
        </p>
        <p>
            And many more!
        </p>
    </details>

Now, take 5 minutes to turn your 2 general problem statements into __specific problem statements__. Feel free to fill in arbitrary details, like the evaluation metric.

<details>
    <summary>
        [Reveal scenario 1 answer]
    </summary>
    <p>
        What roles do cholesterol, smoking, and other factors play in patient risk for coronary heart disease? We will use patient data to train a binary classification model to accurately predict patient risk for coronary heart disease as a way to preemptively intervene before the onset of the disease.
    </p>
</details>

<details>
    <summary>
        [Reveal scenario 2 answer]
    </summary>
    <p>
        Using a SARIMAX model (Time Series), we will predict the likelihood the river will flood as an early warning signal for embankment/levee teams, residents, and emergency response teams to help mitigate property damage. Our predictive target is 33% accuracy as far into the future as possible.
    </p>
</details>

---

## Assignments

### Project
Create a new folder for your project called "project" - YES, there's a project in this course!

Create a new notebook titled "project notebook".

Take 10 minutes to think about a problem you'd like to help solve (small problems are fine!), and form a __general problem statement__ that is relevant to YOU! This problem can be something personal, work related, or just fun!

Don't worry about the dataset - we'll get to this!

### Post!
As a way to encourage discussion, feel free to post your problem statement as a comment on the video! I love hearing what issues others are working on and it may lead to some collaboration opportunities.

### Read
Read one or more of the articles in the ["References"](#References) section.

---
## BONUS

### Kaggle
As a later BONUS lesson, we'll cover Kaggle and the free data science competitions they run. 

As a simple introduction, you can think of Kaggle as a platform for beginners to learn and advanced practitioners to compete for real money, recognition, and bragging rights.

Check out [Kaggle.com](https://www.kaggle.com/) and look into "Knowledge" competitions as a way to get familiar with the platform and even start learning from how others code and work.

### Find Thought Leaders
One of the best ways to get into the data science field is to make connections and ingrain yourself in the subject.

Find 5 thought leaders or newletters in the data science space that resonate with you. Look on LinkedIn, Medium, YouTube, Twitter, and any other platform you can think of and follow or subscribe to stay in the loop!

### SQL (pronounced "sequel")
There is no sugar coating this...  
If you're looking to work in data science you will be at a disadvantage not having at least an __intermediate level understanding of SQL__.

There will be a BONUS lesson dedicated just to SQL, however, getting a head start is in your best interest! Most coding challenge platforms have a section dedicated to SQL.

Check out [Hacker Rank](https://www.hackerrank.com/), [Code Wars](https://www.codewars.com/), [Code Signal](https://app.codesignal.com/), or any of myriad of other such platforms. Start practicing NOW and make it part of your routine!

---
## Vocabulary

### Workflow - ([source](https://kissflow.com/workflow/what-is-a-workflow/))
- A workflow is a sequence of tasks that processes a set of data. Workflows occur across every kind of business and industry. Anytime data is passed between humans and/or systems, a workflow is created. 
- Workflows are the paths that describe how something goes from being undone to done, or raw to processed.

### Ethics - ([source](http://www.bbc.co.uk/ethics/introduction/intro_1.shtml))
- At its simplest, ethics is a system of moral principles. They affect how people make decisions and lead their lives. Ethics is concerned with what is good for individuals and society and is also described as moral philosophy.

### Problem Statement - ([source](https://en.wikipedia.org/wiki/Problem_statement))
- A problem statement is a concise description of an issue to be addressed or a condition to be improved upon. It identifies the gap between the current state and desired state of a process or product.

---
## References
- ["Defining A Data Science Problem" by Nicole Scott](https://towardsdatascience.com/defining-a-data-science-problem-4cbf15a2a461)
- ["Don’t Do Data Science, Solve Business Problems"](https://towardsdatascience.com/dont-do-data-science-solve-business-problems-6b70c4ee0083)
- ["It’s Time for Data Ethics Conversations at Your Dinner Table"](https://data.berkeley.edu/news/it%E2%80%99s-time-data-ethics-conversations-your-dinner-table)
- ["When Big Data Gets It Wrong"](https://www.govtech.com/data/When-Big-Data-Gets-It-Wrong.html)
- [Google almost exposed patient data](https://www.washingtonpost.com/technology/2019/11/15/google-almost-made-chest-x-rays-public-until-it-realized-personal-data-could-be-exposed/)

---
## Have Feedback?
[Submit feedback here](https://docs.google.com/forms/d/e/1FAIpQLScvsDT2Q2VH26FvvfQhjNmP4RwXqh9GWiKSIcTFAHdfCKZdlg/viewform?usp=sf_link)