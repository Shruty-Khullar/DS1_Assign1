# Data Science Assignment-1

## Shruty_101917187_3CSE8 
## Documentation on kaggle challenge : House Prices - Advanced Regression Techniques
Documentation for HousePrice Regression problem from preprocessing to model fitting [(Notebook Link)](https://www.kaggle.com/shrutykhullar/assign-da1/notebook) [(Github Link)](https://github.com/Shruty-Khullar/DS1_Assign1/blob/main/assign-da1.ipynb)

## Steps followed
 1. Pre-processing 
	 a. [Feature Selection](#feature-selection)

	 b. [Handling Null Values](#imputation)

	 c. [Transformation and scaling](#transformation-and-scaling)

 2. [Linear Regression](#linear-regression)

	 a. Built-in LinearRegression Class (various algorithms)

 3. [Validation Accuracy](#validation-accuracy)

 4. [Rank in Leaderboard](#rank-in-leaderboard)

---
### *Feature Selection*
Initial Dataset had 79 features (excluding ID and Output) and most were of object data-type.
I picked all features whose data-type matches one of the following :
 - `int64`
 - `int32`
 - `float64`
 - `float32`
 
Which resulted in 37 features. 
Input dataset shape (1460, 37) and
Rest of them are not so useful in training the model.


---
### *Handling Null Values*
In the input dataset there were few features which had null values. I used mean imputation for missing values.

---
### *Transformation and Scaling*
A lot of the features were skewed, I picked all the features whose skewness was outside the range of [-0.5, 0.5] and applied log transformation `log_e(1 + x)` as other transformations works efficiently only on data with moderate skewness but we need to work with the dataset having high as well as moderate skewness.

After correcting skewness, I applied StandardScaler class on Input data so as to mean-center the data and reduce bias towards any one feature.

---
### *Linear Regression*
I applied  built-in Regression model- LinearRegression .
I used 5 algorithms for LinearRegression Class
 - `svd`
 - `eig`
 - `qr`
 - `svd-qr`
 - `svd-jacobi`

---
### *Validation Accuracy*

|            | MAE      | MSE          | MSE          |
|------------|----------|--------------|--------------| 
| svd        | 0.831169 | 20421.084901 | 7.166733e+08 |
| eig        | 0.831169 | 20421.084901 | 7.166733e+08 |
| qr         | 0.831169 | 20421.084901 | 7.166733e+08 |
| svd-qr     | 0.831169 | 20421.084901 | 7.166733e+08 |
| svd-jacobi | 0.831169 | 20421.084901 | 7.166733e+08 |

### *Rank in Leaderboard*
Using only Built-in LinearRegression and achieved r2 score of approximately 83%
### I was placed at **4266** position.

Code: [Notebook Link](https://www.kaggle.com/shrutykhullar/assign-da1/notebook)
