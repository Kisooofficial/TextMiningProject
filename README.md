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
Analyizing keyword each topic

### how?
After rescoring score, I divide up sections by four class. It is verybad(lower than 2), bad(higher than 2 & lower than 3), normal(higher than 3 & lower than 4), good(higher than 4)

# Results
+ Sentiment Analysis
<img src = "https://user-images.githubusercontent.com/84063359/177031785-e67d0fb1-8840-4bea-a0cd-f558a5576fb0.png" width = 100% height = 150></img>
+ Comparing score that rescoring before&After, It is an error that differences between user-assigned ratings and sentimental ratings 
Rescoring error before => 2.20, Rescoring error after => 0.55(after using 0.25, 0.75 weight)
+ correction score average by four sections
<img src = "https://user-images.githubusercontent.com/84063359/177032112-4ef5c634-3770-4ec8-be74-9c88ae9ad9f7.png" width = 100% height = 150></img>
+ Topic Modeling results(it is only summary)
<img src = "https://user-images.githubusercontent.com/84063359/177032148-7dfc440e-ea0e-4825-98ab-7c6897d15096.png" width = 100% height = 300></img>

# Expected effects of this project
+ Accurate diagnosis related to the establishment of an emotion analysis model is required
The model generally adjusted the positive and negative well, but there were quite a few cases where it did not. We need to think about this further. We are considering the direction of improving accuracy by periodically adding disused terms to parts such as newly coined words specialized in Korean.
+ Topic modeling suggests alternatives to overall poor evaluation
From the consumer's point of view, you can see people's overall assessment of the product, and from the seller's point of view, you can understand consumers' overall needs and help them solve problems. In the future, we plan to find the best topic while looking for hyperparameters using the gensim library.
+ Link to future recommendations
Entering the era of super-personalization through the era of untact, personalized marketing has become important. It is possible to implement a recommendation system using collaborative filtering and content-based filtering using the constructed data.
=> Since you can get your personal nicknames from today's home, you need to think about implementing the recommended system techniques above, and you need to think about solving cold start problems that may occur in this process.
***
For another details, please reference powerpoint such as a presentation of a proposal and final presentation
