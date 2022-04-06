# MLG - Laboratoire 3 - Model Selection	

> Auteurs: Noémie Plancherel & Lev Pozniakoff
>
> Date: 30.03.22

## hold_out_validation

> **Q1**. Determine where do we define all the parameters mentioned above.

> Observe that we run the evaluation procedure on four different problems. Each problem is a two-class two-dimensional problem, where the two sets are more and more overlapped (e.g., the synthetic datasets are randomly generated using variances of 0.4, 0.5, 0.6 and 0.7).

Dans le bloc 7 du notebook, la fonction `split_dataset` va permettre de séparer le dataset en deux parties en fonction du paramètre de la fonction qui va indiquer la proportion des partitions train/test. 

Le bloc de 8 du notebook déclare plusieurs constantes:

```python
N_INITS = 2
N_SPLITS = 10
DATASET_SIZE = 200
EPOCHS = 100
N_NEURONS = 2
LEARNING_RATE = 0.001
MOMENTUM = 0.7
TRAIN_TEST_RATIO = 0.8
DATA_PARAMS = np.arange(0.4, 0.71, 0.1)
```

Ces constantes vont permettre de définir les différents paramètres que l'on souhaite varier durant nos expérimentations. 

En observant les différents résultats en fonction des variances utilisées, nous voyons effectivement que lorsque le taux de diffusion est à 0.4, l'erreur quadratique moyenne (MSE) est plutôt concentrée, elle varie entre 0-0.1, cependant plus on augmente la variance, plus MSE est éparpilée. On peut le constater avec le taux de diffusion de 0.7 où le MSE varie entre 0.2-0.5.

> **Q2**. What are the cyan and red curves in those plots ? Why are they different ?

Les courbes cyan sont les erreurs des données d'entraînement et les courbes rouges sont les erreurs des données de test. 

<u>TODO - Why are they different</u>

> **Q3**. What happens with the training and test errors (MSE) when we have the two sets more overlapped ?



> **Q4**. Why sometimes the red curves indicate a higher error than the cyan ones ?

On peut expliquer cela par le fait qu'en général il y a moins de données dans le set de testing que dans le set de training.

> **Q5**. What is showing the boxplot summarizing the validation errors of the preceding experiments ?

Pour chaque taux de diffusion (*spread*), le boxplot présente leur MSE. Comme on a l'a déjà cité précédemment, plus le taux de diffusion augmente, plus le MSE est éparpillé.

## cross_validation

> **Q1**. Determine where do we define all the above mentioned parameters.

> **Q2**. What is the difference between hold-out and  cross-validation ? What is the new parameter that has to be defined for  cross-validation ?

> **Q3**. Observe the boxplots summarizing the validation  errors obtained using the cross-validation method and compare them with  those obtained by hold-out validation