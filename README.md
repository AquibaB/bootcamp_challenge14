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