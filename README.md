# Time-series-econometrics

The project was programmed in __Markdown__ so the file in __TAUCH Lukas IF 1 TD 5.Rmd__ but you can see an overview by saving the file in __TAUCH-Lukas-IF-1-TD-5.html__ in your __folders__

Here are the steps of my project and the __step-by-step questions__ that are __answered and interpreted__ in the project :

# DATA SETTING

- Load the Advance Retail Sales - namely the Retail Trade from the Federal Reserve of Saint Louis
- Check the status of the imported data and transform it into a right object if necessary. 
- Plot the data. Observation of the data. Determination type of __seasonal pattern__. Computation the __filters__ to clean the retail sales.
- Run the required filter to cut the seasonal pattern. Choose between the seasonal regression, the moving average filter and the decompose function (this function is based on moving
average seasonal filters as well).
- Grab the filtered data and check using the right tool the seasonal pattern has been deleted. Is this
filtered data be modeled using an ARMA(p,q) approach ?

# UNIT ROOT TESTS

- Load the "urca" package. Summarize quickly the step-wise approach of the Dickey Fuller test.
Compute the Augmented Dickey Fuller test using the right function on the filtered data (note that
the selection of the number of lags can be performed on a discretionary way or automatically).
- Determine then the integration degree of the data ?
- Compute the Phillips and Perron test on the filtered data. Does it confirm your previous result ?
- Compute the KPSS test using one of the artificial data generated previously. Do we find the same
conclusion ?
- Find the degree of integration of the US retail sales using the KPSS test. Does it validates the
previous result ?

# MODELING

- Given the results derived from the previous sections, propose the most relevant ARMA(p,q) framework to model the retail sales dynamics. Is there an alternative to the ARMA(p,d) approach ?
- Having choose the correct specification, justify the relevance of your choice with the required tests.

# ESTIMATING AN ARIMA (p,d,q)

- Determine the degree of integration of the Johnson & Johnson stock prices.
- Determine the order of the ARIMA model, i.e the values of p, d, q to be used to model the stock
prices. Note first, the assessment of p and q cannot be performed on the data expressed in level.
Note besides, the determination of the values of p and q can be performed using different methods
(graphical approach vs information criteria).
- Estimate the corresponding ARIMA(p,d,q) model to the values of p,d,q selected previously. Check
the estimated coefficients and compute the fit of the model. Plot (within the same chart) the
estimated values of the stock price and the observed one.
- Calculate the residual of the model, given as the difference between J&ˆ J and J&J. Compute the
required quality checks on the residuals.
- Using the estimated coefficients, generate a forecast over the next 3 months. Calculate the confidence interval of the forecasted points .

# UNIT ROOT TEST ZIVOT AND ANDREWS

In this exercise, we propose to introduce a new unit root test : the test of Zivot and Andrews (1992). On
of the weakness of the ADF unit root tests is their potential confusion of structural breaks in the series
as evidence of non-stationarity. In other words, they may fail to reject the unit root hypothesis if the
series have a structural break.

Zivot and Andrews (1992) endogenous structural break test is a sequential test which utilizes the full
sample and uses a different dummy variable for each possible break date. The break date is selected where
the t-statistic from the ADF test of unit root is at a minimum (most negative). Consequently a break
date will be chosen where the evidence is least favorable for the unit root null.

The Zivot-Andrews (1992) tests state the null hypothesis is that the series has a unit root with structural
break(s) against the alternative hypothesis that they are stationary with break(s). We reject Null if tvalue statistic is lower than tabulated critical value

- Present the Zivot and Andrews (1992) test paying attention to the nature of the breaks. Explain
the strategy of the test.
- Generate 3 new random walks. The first one is a pure random walk, the second is a random walk
with a break in level and the third on will be a random walk with both a break in level and in the
trend.
- Compute the appropriate Zivot and Andrews (1992) test for the generated random walk. Summarize your output within a table.
- Is it relevant to use such test for the filtered retail sales. Justify. Compute the Zivot and Andrews
(1992) unit root test using the US retail sales.

# MODELING THE BUSINESS CYCLE

Based on all your knowledge, propose the most appropriate specification to model the quarterly US GDP
dynamics‘
. Produce a forecast of the US business cycle for the next three quarters. We are expecting a
complete study with illustrating charts, detailed and motivated comments and relevant results.
