### Fraud Detection Analysis using Spark

#### Task Background
Due to the development of information technology, big data collection, analysis, and storage has become an important component of many industries. Josphineleela et al [[1]](https://www.researchgate.net/publication/369846162_Big_Data_Security_through_Privacy_-_Preserving_Data_Mining_PPDM_A_Decentralization_Approach) pointed out that big data refers to data with a large volume, large file size, and fast speed, which not only provide huge potential for industries, but also introduce a series of data security challenges. Big data security, as an important branch of IT, aims to ensure the confidentiality, integrity, and availability of large-scale data. Enterprises mainly face several prominent data security issues, such as insufficient data access control, insufficient data analysis capabilities, resulting in frequent occurrence of data security issues [[2]](https://ieeexplore.ieee.org/document/10206137). Therefore, the urgent task for enterprises is to develop security management measures based on the big data lifecycle to address security issues.

One typical application is fraud detection. As digitization trend, more financial institutions are providing digital services to public through online banking, leading to the increased usage of credit card. In 2020, Visa [[3]](https://www.statista.com/statistics/618115/number-of-visa-credit-cards-worldwide-by-region/) and Mastercard [[4]][(https://www.statista.com/statistics/618137/number-of-mastercard-credit- cards-worldwide-by-region/) issued 2.278 billion credit cards globally, providing convenience for digital and cashless transactions. Although credit cards provide convenience, fraudulent activities are also increasing, causing huge losses to financial institutions and users, as their private information would be used by fraudsters to obtain account information or engage in transactions without authorization [[5]](https://ieeexplore.ieee.org/document/8361343). According to UK Finance, credit card fraudulent activities have been proven to be one of the main causes of financial losses, with a reported value of £574.2 million in fraud cases in the UK in 2020.


#### Task Introduction
Based on big data technology, we believe that machine learning is an effective means to help financial institutions determine fraudulent and legitimate behaviors. Therefore, we need to find an optimal machine learning algorithm to avoid credit card fraud, reducing the financial losses.

The main aim is to select an optimal machine learning model comparing logistic regression, decision tree and random forest for fraud detection to improve the security of credit card transactions, reduce financial losses and ensure big data security. This research will be carried out from the following aspects:

1. **Exploratory Data Analysis (EDA)**: Conduct an in-depth exploration of dataset to unveil variable distributions, correlations, and potential patterns, laying the foundation for subsequent analyses.
2. **Model Selection**: Evaluate performance on various models, including logistic regression, decision trees, and random forests to determine the best model for fraud detection.
3. **Best Model Optimization**: Choose the best model and further optimize it by analyzing the potential reasons for wrong classification and employing down sampling to enhance the performance.

The whole procedure of this task is shown below:

<img width="709" alt="截屏2024-11-26 16 44 16" src="https://github.com/user-attachments/assets/050588e5-808f-47f1-b904-8c0b1d2e8aea">


#### Dataset Preparation
In this study, we used a simulated credit card transaction dataset that includes information of 1000 customers from January 1, 2019, to December 31, 2020, as well as their transactions with 800 merchants [[Kaggle]](https://www.kaggle.com/datasets/kartik2112/fraud-detection). The total amount of raw data is about 180w, with 22 features. 

**Note**: I only uploaded parts of dataset due to the limiations, the original dataset link is [here](https://www.kaggle.com/datasets/kartik2112/fraud-detection)

#### Model Preparation and analysis

In this tasks, we implemented 3 models namely logistic regression, decision tree and random forest, as these are the most commonly used machine learning model and have great interepretability (Easy for explanation is quite important). Futhermore, I also tried to addressed the problem of high data imbalance, which is quite important as this is frequenly met in fraud detection case. In this case, there are 492,494 non-fraud samples (98.5%) and 7,506 fraud samples (1.5%). Therefore, I tried to downsampling the majority class with ratio of 0.7 to make it more balanced. Moreover, FNR is used as the most important evaluation criterion for selecting models, and FPR as an auxiliary important evaluation indicator, ultimately determining the decision tree as the best model. Based on decision tree, we also addressed the issue of extremely imbalanced labels by exploring the optimal down sampling ratio and achieved a significant reduction in FNR.

<img width="309" alt="截屏2024-11-26 16 43 19" src="https://github.com/user-attachments/assets/d29acbc0-bd8c-4504-b104-af7eba9d94ca">




