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
## <span style = "color:red">Data Gathering</span> 
Using Crawling such as Selenium, BeautifulSoup. After that, I get 200 thousands of review data
## Noise Canceling 
Using han-spell library fixing hangul spelling.
## Morphological Analysis and Disuse of Terms
First of all, I considered to analyze in terms of Morphs. But, for topic modeling, I should get correct word not morphs. So, I decided to get Part Of Speech(POS). I only used nouns, adjective, verb.
## Text Vectorization 
I considered using TF-IDF, but it has sparsity problems. I solve a problem using Tokenize. I search rare words, and delect it to have more accuracy in sentiment analyizing.
## Sentiment Analysis
To solve the difference between the mood of the review and the rating, we conduct an sentiment analysis. After sentiment analysis, I rescore rating.(sentiment score * 0.25 + rating * 0.75)

## Topic Modeling
### how?
After rescoring score, I divide up sections by four class. It is verybad(lower than 2), bad(higher than 2 & lower than 3), normal(higher than 3 & lower than 4), good(higher than 4)

# Results
+ Sentiment Analysis
<img src = "https://user-images.githubusercontent.com/84063359/177031785-e67d0fb1-8840-4bea-a0cd-f558a5576fb0.png" width = 100% height = 150>
+ Comparing score that rescoring before&After, It is an error that differences between user-assigned ratings and sentimental ratings 
+ +Before Rescoring
<img src = "https://user-images.githubusercontent.com/84063359/177031836-4aee808a-c31c-465e-941a-7c44cd7e6965.png" width = 50% height = 200>
<img src = "https://user-images.githubusercontent.com/84063359/177031862-7074b6de-93c5-4ff9-85f6-c3cc0229cc20.png" width = 50% height = 200>
+ After 
