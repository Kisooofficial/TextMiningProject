# What is this repository?
It is a repository related to the project in the subject Text Mining in the first semester of 2022.
# What is a project name?
Topic modeling of 'Today's House' review, a site that sells home products, provides opportunities to compensate for  shortcomings and maximize their strengths
# Why I do this project?
COVID-19 Develops Untact-Related Industry. Various industries have developed, but among them, the untact industry is developing. Each company is planning a marketing strategy using untact, and in this process, AI-based marketing methods are being activated. Choosing a topic to provide better service to students who are living alone among college students
With the end of COVID-19, the proportion of people living alone is expected to increase due to the increase in face-to-face classes. Therefore, it was necessary to improve the products mainly used by those living alone.a selection of topics

# The overall project flow chart
<img src = "https://user-images.githubusercontent.com/84063359/177031095-911e3d75-92fa-4c9c-bad5-5bd50793f1e7.png"
     width = 100% height = 200>

# Process 
## Data Gathering 
Using Crawling such as Selenium, BeautifulSoup. After that, I get 200 thousands of review data
## Noise Canceling 
Using han-spell library fixing hangul spelling.
## Morphological Analysis and Disuse of Terms
First of all, I considered to analyze in terms of Morphs. But, for topic modeling, I should get correct word not morphs. So, I decided to get Part Of Speech(POS).
