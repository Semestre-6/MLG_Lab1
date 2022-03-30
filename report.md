# MLG - Laboratoire 3 - Model Selection	

> Auteurs: Noémie Plancherel & Lev Pozniakoff
>
> Date: 30.03.22

## hold_out_validation

> **Q1**. Determine where do we define all the parameters mentioned above.
>
> Observe that we run the evaluation procedure on four different problems. Each problem is a two-class two-dimensional problem, where the two sets are more and more overlapped (e.g., the synthetic datasets are randomly generated using variances of 0.4, 0.5, 0.6 and 0.7).

> **Q2**. What are the cyan and red curves in those plots ? Why are they different ?

> **Q3**. What happens with the training and test errors (MSE) when we have the two sets more overlapped ?

> **Q4**. Why sometimes the red curves indicate a higher error than the cyan ones ?

> **Q5**. What is showing the boxplot summarizing the validation errors of the preceding experiments ?



## cross_validation

> **Q1**. Determine where do we define all the above mentioned parameters.

> **Q2**. What is the difference between hold-out and  cross-validation ? What is the new parameter that has to be defined for  cross-validation ?

> **Q3**. Observe the boxplots summarizing the validation  errors obtained using the cross-validation method and compare them with  those obtained by hold-out validation