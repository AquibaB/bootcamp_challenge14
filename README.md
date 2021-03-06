# bootcamp_challenge14

## Tuning the Support Vector Machine model

### Widening the training window from 3 months to 12 months with the original dates

The dates chosen are the same as in the original model. 

A larger training dataset spanning 12 months (as opposed to the original 3 months) resulted in slightly better accuracy (56% versus 55% original). 

The model's prediction of positive returns improved with perfect recall (100%) and 56% precision.

However, the model's prediction of negative return deteriorated and failed in making any predictions (recall and precision were 0)

### Widening the training window from 3 months to 12 months at laters dates

The dates chosen are shifted 12 months forward

Beginning: 2016-04-02
Ending: 2017-04-02

Unfortunately, changing the training dates did not change the model in any meaningful way

### Conclusion

Even though the classification report after tuning the model showed a modest improvement in accuracy, the strategy backtest confirmed that the strategy's returns fit more closely to actual returns. Therefore, this strategy might be a good predictor of future actual returns.

<em>Original SVM Strategy Backtest</em>

![Original SVM](/Original_actual_strategy_cumreturns.png)

<em>Tuned SVM Strategy Backtest</em>

![Tuned SVM](/Tuned_actual_strategy_cumreturns.png)

## SVM model vs. Random Forest model

The Random Forest (RF) performed worse than the original (and tuned) SVM models. 

RF's accuracy was lower than SVM's at 52%. However, RF model did a much better job at predicting unprofitable trades (Signal = -1) compared to the SVM's model. The RF model predicted the signal correctly 35% of the time (recall) with a 44% precision (SVM model did not make any predicions for Signal = -1)

The backtest results show that the Random Forest performed worse than the original SVM model.

<em>SVM and RF Strategies Backtest</em>

![SVM-RF Comparison](/Comparison_actual_SVM_RF_cumreturns.png)