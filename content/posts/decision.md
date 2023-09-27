+++
title = "decisions"
lastmod = 2023-09-27T18:44:41+09:00
draft = false
+++

## process {#process}

1.  select buy candidates

2.  for each candidate
    -   indicators produce (multiple) predictions

3.  prepare buy / sell (2nd level indicator)
    1.  combine multiple predictions on each candidate (weight them)
    2.  produce possible buy candidates

    3.  evaluate current holdings

        for each holding, 2nd level indicator evaluate holding

        We have bought this holding with this prediction data
        Is the prediction still valid? can you (indicator) evaluate the current standing?

4.  decide buy / sell

    With new candidates for buy, evaluations for current holdings


## update process {#update-process}

With prediction / evaluation, evaluate indicators / 2nd-level indicators


## indicators {#indicators}

decision unit


### performs following (api) {#performs-following--api}

1.  produce predictions

<!--listend-->

```python
def predict(self, stock_id: str, current_price: Price) -> Prediction:
    # uses RawData
    pass
```

1.  evaluate prediction on different time (how valid is the past prediction now?)

    if we made prediction on 3month granular, after 1 month, we'd be in position to evaluate that prediction

<!--listend-->

```python
def evaluate(self, stock_id: price: Price, str, buy_data: BuyData, evaluate_at: datetime) -> Evaluation:
    pass
```

1.  (supporting evaluation) how much I (indicator) can trust my previous prediction given data available after making the prediction

    I had **so and so** hypothesis when making predictions, and since they hypothesis turned out to be misplaced, I can re-evaluate my confidence on my previous prediction

2.  (supporting evaluation) self check

    I just made this prediction, but I also know this depends on my assumptions
    In future, if **this and this** happens, I would advice differently.


## 2nd-level indicators {#2nd-level-indicators}

aggregate multiple (selective) indicators

1.  lv2 indicator produce 2nd level Prediction / Evaluation data

2.  having access to multiple indicators can yield better decision

3.  Whether to let indicator directly talk to another indicator is an implementation chice


## data {#data}


### raw data for prediction {#raw-data-for-prediction}


#### raw data falls into following categories {#raw-data-falls-into-following-categories}

1.  Target data

    Target data is what we are trying to get, but unable to get perfectly
    It answers how much an investment is worth and how much we are paying for

    -   valuation (how much company value)
    -   price (how much company cost (eg, stock price))

2.  Target proxy data

    It is not directly related to the measurement of target data but it is a proxy

    -   eg, company buying its own stocks can signal a new valuation

3.  Environment data

    relavant data which affects interpretation of target data

    -   inflation
    -   interest rate

4.  Speculation data
    -   how people perceive market (people speculation)
    -   how I perceive market (own speculation)

5.  Past pattern data

    eg, MA trends analysis


#### Rawdata {#rawdata}

-   data type
-   data source
-   data acquisition date


### Prediction {#prediction}

1.  probability of going up / expected-amount (amount is in % unit)

2.  when is this prediction about
    -   prediction-horizon:
        -   when is this prediction about
        -   center and range (variance)

3.  what is the nature of the prediction
    -   valuation / speculation / environment

4.  PredictionReason

    serves two purposes

    1.  clearly represent the prediction logic when reviewing
    2.  clearly indicate what the actual code ran
        -   holds git commit hash and the function responsible for the prediction
        -   might be better to place them where future execution run time can find so that we can readily use that code (create override function with commit hash)
        -   when prediction / evaluation code is updated, it can indicate which previous versions it supercedes

5.  FutureEvaluationReason

    similar to PredictionReason but for evaluation purpose

    1.  clearly represent the evaluation logic at the time of prediction

In order to evaluate the prediction later, prediction has to show why (on what basis) we made the prediction by

-   I predict Prediction based on RawData at access-time using PredictionReason
-   and I think I can evaluate my prediction in future with FutureEvaluationReason


### Evaluation {#evaluation}

similar to Prediction, but holds evaluation data

We have current holding at price different from prediction.
We can evaluate current holding

1.  by asking if we made wrong prediction in the past given we have more data available
    -   it's as if we are asking, this looks bad but did we really make wrong decision? or do we hold on to it?
    -   It could be a simple rule to sell holdings
2.  by producing new prediction with new data

Both 1, 2 can be beneficial

solely relying on 1 might miss a new opportunity
solely relying on 2 might result in selling prematuarely

We also need to perform 1 for updating our PredictionReason / EvaluationReason


### BuyData, SellData {#buydata-selldata}

data stored when buying / selling takes place


#### BuyData {#buydata}

1.  purchase record (time, amount)
2.  BuyDecision
    -   2nd level indicator's buy decision data
        -   list of [Prediction, weight]
        -   2nd level indicator's DecisionReason


#### SellData {#selldata}

1.  selling record
2.  SellDecision
    -   list of [Evaluation, weight]


## whether to buy {#whether-to-buy}


### expectation {#expectation}

1.  probability of going up
2.  amount to win / lose

Indicator's Prediction data is combined (by 2nd-level indicator) to create the expectation


## how much to buy {#how-much-to-buy}


### kelly {#kelly}

F = P - (1-P) / R

F: % of investment (against total investment)
P: probability to win
R: expected-amount-to-win / expected-amount-to-lose


## how to measure risk {#how-to-measure-risk}


### expectation - base (0) {#expectation-base--0}

When expectation is high and above base, it's low risk
When investing long term, variance doesn't matter much


### variance {#variance}

higher fluctuation (of possible outcome) is higher risk
initial portfolio theory used variance as risk measurement


### consider {#consider}

high variance is mitigated if long term investment
when equal expectation, lower variance is lower risk


## how much to diversify {#how-much-to-diversify}


### when not prepared {#when-not-prepared}

diversify, start from index fund


### goal is to focus on relatively small # (5 or fewer) {#goal-is-to-focus-on-relatively-small--5-or-fewer}


## Current plan (ag1) {#current-plan--ag1}

decide if this is a good time to buy stock (index fund)
so we have only single candidate

-   decide which data to use


## <span class="org-todo todo TODO">TODO</span> index fund indicator {#index-fund-indicator}


### <span class="org-todo todo TODO">TODO</span> decide which raw data to use {#decide-which-raw-data-to-use}


### <span class="org-todo todo TODO">TODO</span> decide decision rule {#decide-decision-rule}
