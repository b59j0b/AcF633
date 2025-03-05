java c
AcF633 - Python Programming for Data Analysis 
Group Project
20th February 2025 noon/12pm to 6th March 2025 noon/12pm (UK time)
This assignment contains one question worth 100 marks and constitutes 35% of the total marks for this course.
You are required to submit to Moodle a SINGLE .zip folder containing a SINGLE Jupyter Notebook .ipynb file (preferred) and/or Python script. .py files and supporting .csv files (e.g. input data files, if any), together with a signed group coversheet. The name of this folder MUST be your group number (e.g. Group1.zip, where Group 1 is your group).
In your main script, either Jupyter Notebook .ipynb file or Python .py file, you do not have to retype the question for each task. However, you must clearly label which task (e.g. 1.1, 1.2, etc) your subsequent code is related to, either by using a markdown cell (for .ipynb files) or by using the comments (e.g. #1.1 or ‘‘‘1.1’’’ for .py files). Provide only ONE answer to each task. If you have more than one method to answer a task, choose one that you think is best and most efficient. If multiple answers are provided for a task, only the first answer will be marked.
Only ONE of the group members is required to submit the work for your group. Your submission .zip folder MUST be submitted electronically via Moodle by the 6th March 2025 noon/12pm (UK time). Email submissions will NOT be considered. If you have any issues with uploading and submitting your group work to Moodle, please email Carole Holroyd at [email   protected] BEFORE the deadline for assistance with your submission.
Please ensure that ALL members of the group who have contributed to the group work have signed the group coursework coversheet before your coursework is submit-ted. Group members who have not signed the coversheet are deemed to have not contributed to the group submission and will be awarded a zero mark.
This assignment is AI Assessment AMBER (i.e. Generative AI tools can be used in an assistive role). Please refer to the University position page: University position on Artificial Intelligence for more details about AI Assessment RAG categories. If you use AI to assist your work, you are required to submit an AI appendix.
The following penalties will be applied to all coursework that is submitted after the specified submission date:
Up to 3 days late - deduction of 10 marks
Beyond 3 days late - no marks awarded
Every student is required to submit a peer evaluation form. electronically via Moodle to evaluate their group members’ participation and contribution to this empirical assign-ment. Deadline for peer evaluation submission is 7th March 2025 noon/12pm (UK time), i.e. one day after the Group Project’s deadline.
Good Luck!
Question 1: 
The SP100 index is a market capitalization-weighted index of 100 leading stocks listed in the US stock exchanges. The csv data file ‘SP100-Feb2023.csv’ lists the constituents of the SP100 index as of February 2023 with the following information:
❼ Ticker: Company’s stock symbol or ticker
❼ Company: Company’s name
❼ Sector: Sector in which the company belongs
❼ Market Value: Company’s market capitalization
Import the data file to an object called “Index” in Python and perform. the following tasks.
Task 1: Descriptive Analysis of SP100 index (Σ = 25 marks)
1.1: How many unique sectors are there in the SP100 index? Print the following statement: ‘There are ... unique sectors in the SP100 index, namely ...’, where the first ‘...’ is the number of unique sectors, and the second ‘...’ contains the names of the sectors alphabetically ordered and separated by commas. (2 marks)
1.2: Write code to create a dictionary with keys being the unique sectors in the SP100 index sorted in alphabetical order, and values being lists of tickers, also alphabetically ordered, in each sector.
Hint: An example of a key-value pair of the required dictionary is ‘Materials’: [‘DOW’, ‘LIN’].                        (3 marks)
1.3: Modify code in Task 1.2 to create a dictionary with keys being the unique, alphabetically sorted sectors in the SP100 index, and values being tuples of two elements: the first being the number of tickers in each sector, and the second being the list of alphabetically ordered tickers in each sector.
Hint: An example of a key-value pair of the required dictionary is ‘Materials’: (2,[‘DOW’, ‘LIN’]).                           (3 marks)
1.4: Add a column called “Weighting” to the “Index” object that computes the weight (in percentages, rounded to 3 decimal places) of each company in the SP100 index.                            (3 marks)
1.5: Write code to find the company having the largest index weight and the one with the smallest weight. Print the following statements:
Company ... (ticker ..., sector ...) has the largest index weight of ...%.
Company ... (ticker ..., sector ...) has the smallest index weight of ...%.
The range of the weights is ...%. (3 marks)
1.6: Write code to produce the following pie chart that shows the SP100 index weighting by sectors. Only show the percentage weighting labels for sectors whose weights are larger than 1%.

Print the following statement:
Sector ... has the largest index weight of ...%, and Sector has the smallest index weight of ...%. (6 marks)
1.7: Write code to classify the SP100 companies into 3 groups: “Large cap” when market value ≥ 100m, “Mid cap” when 100m > market value ≥ 30m, and “Small cap” when market value < 30m. Add a column called “Group” to the “Index” object to capture this grouping information. (2 marks)
1.8: Write code to produce the following pie chart that shows the SP100 index weighting by company grouping. (3 marks)

Task 2: Portfolio Allocation (Σ = 30 marks)
2.1: Using your group number (e.g. 1, 2, 3, etc.) as a random seed, draw a random sample of 5 stocks (i.e. tickers) from the SP100 index excluding stocks ABBV, AVGO, CHTR, DOW, GM, KHC, META, PYPL and TSLA.1 Sort the stocks in alphabetical order, and then import daily Adjusted Close (Adj Close) prices for the 5 stocks between 01/01/2009 and 31/12/2024 from Yahoo Finance. Compute the simple daily returns for the stocks and drop days with NaN returns. (3 marks)2.2: Create a data frame. to summarize key statistics (including sample size, mean, standard deviation, minimum, quartiles, maximum, skewness, kurtosis, Jarque-Bera statistic, Jarque-Bera pvalue and Normality) for the daily returns of the five stocks over the above sample period. Jarque-Bera statistic is the statistic for the Jarque-Bera normality test that has the formula  where T is the sample size, Sb and Kb are sample skewness and kurtosis of data, respectively. Under the null hypothesis that data is normally distributed, the JB statistic follows a χ2 distribution with 2 degrees of freedom. Jarque-Bera pvalue is the pvalue of the JB statistic under this χ2 distribution. Normality captures the conclusion of the Jarque-Bera test - whether daily returns of a stock are normally distributed (Yes) or not (No), based on a 5% significance level. Your data frame. should look similar to the one below, but for the five stocks in your sample.



(4 marks)
2.3: Using and/or modifying function get_efficient frontier() from the file Eff_Frontier_functions.py on Moodle, construct and plot the Efficient Frontier for the five stocks based on optimization based on data over the above period. In your code, define an equally spaced range of expected portfolio return targets with 2000 data points. Mark and label the locations of the five stocks in the Efficient Frontier plot. Also mark and label the locations of the Global Minimum Variance portfolio and the portfolio with the largest Sharpe ratio, assuming the annualized risk-free rate is 0.01 (or 1%).                                           (5 marks)
2.4: What are the return, volatility, Sharpe ratio and stock weights of the portfolio with the largest Sharpe ratio? Write code to answer the question and store the result in a Pandas Series object called LSR port capturing the above statistics in percentages. Use the words ‘return’, ‘volatility’, ‘Sharpe ratio’, and stock tickers (in alphabetical order) to set the index of LSR port. (3 marks)
2.5: Paul, a mean-variance optimizer, is interested in the five stocks in your sample. He has an expected utility function of the form. U(Rp) = E(Rp) − 0.5Aσp2, where Rp and σp2 are respectively the return and variance of the portfolio p, and A is Paul’s risk-aversion coefficient. Assume A = 4. Also assume that Paul does not have access to a risk-free asset (i.e. he cannot lend or borrow money at the riskfree rate) and he would like to invest all of his wealth in the five stocks in your sample. How much, in percentages of his wealth, should Paul invest in each of the stocks in your sample to maximize his expected utility? Write code to answer the question and store the result in a Pandas Series object called Paul port respectively capturing the return, volatility, Sharpe ratio and the stock weights of Paul’s portfolio. Set the index of Paul port correspondingly as in Task 2.4. (4 marks)
2.6: Paul is interested in knowing how the expected return of his optimal (i.e. maximum-utility) portfolio changes with his risk-aversion level A, when he does not have access to a risk-free asset. Write code to produce a similar plot to the following for your stock sample, setting A between 0 and 10. What can you conclude from the plot?

(5 marks)
2.7: Now suppose that Paul has access to a risk-free asset and can borrow and lend money at the risk-free rate. In this case, he will choose the efficient portfolio with the largest Sharpe ratio in Task 2.4 as his optimal risky portfolio and will divide his wealth between this optimal portfolio and the risk-free asset to maximize his expected utility. He could also borrow money (i.e. have a negative weight on the risk-free asset, which is assumed to be capped at -100%; that is, the maximum amount that he can borrow is equal to his wealth) to invest more in the risky assets. What will be his portfolio compositions in this case, assuming that his risk-aversion coefficient A = 4? Write code to answer the question and store the result in a Pandas Series object called Paul port rf respectively capturing the return, volatility, Sharpe ratio, the stock weights and risk-free asset weight of Paul’s portfolio. Set the index of Paul port rf correspondingly. (6 marks)
Task 3: Factor models (Σ = 25 marks)
3.1: Denote P be the portfolio formed by combining the five stocks in your sample using equal weights. Compute the daily returns of the portfolio P over the considered time period from 01/01/2009 to 31/12/2024. (3 marks)
3.2: Using data from Kenneth R. French website, estimate a Carhart four-factor model for portfolio P over the above period. Test if portfolio P possesses any abnormal returns that cannot be explained by the factor model. (4 marks)
3.3: Conduct the White test for the absence of heteroskedasticity in the residuals of the above factor model and draw your conclusion using a 5% significance level.    (3 marks)
3.4: Conduct the Breusch-Godfrey test for the absence of serial correlation up to order 10 in the residuals of the above factor model and draw your conclusion using a 5% significance level. (3 marks)
3.5: Based on results in the above two tasks, update the Carhart four-factor regression model and re-assess your conclusion on the pricing of portfolio P according to the factor model in Task 3.2. (3 marks)
3.6: Compute the 4-year rolling window β estimates of the Carhart four factors for portfolio P over the sample period. That is, for each day, we compute β loadings for the three factors using the past 4-year data (including data on that day). Plot a 2×2 subplot figure similar to the following for your stock sample, showing the rolling window β estimates of the factors, together with 95% confidence bands. Provide brief comments. (9 marks)

Task 4: (Σ = 20 marks)
These marks will go to programs that are well structured, intuitive to use (i.e. provide sufficient comments for me to follow and are straightforward for me to run your code), generalisable (i.e. they can be applied to different sets of stocks, different utility functions for Paul with minimal adjustments/changes to the code) and elegant (i.e. code is neat and shows some degree of efficiency).





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
