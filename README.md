# Econometric-Method-Project-in-R
## Introduction
The changing demographics, a large informal sector, and weakening
family support for the elderly are significant factors contributing to
old-age poverty in developing countries. As migration and declining
fertility lead to a reduction in the traditional multi-generational
household model that supported older people, those working in the
informal sector are at increased risk of old-age poverty due to the lack of
social protection coverage.
To address this issue, social pensions, in the form of cash transfers,
have been introduced to provide income security for the elderly who lack
social protection coverage. The Indian government implemented the
National Old Age Pension Scheme in 1995 to support poor older people
as part of the National Social Assistance Programme.
However, the targeting performance of the social pension scheme for
poor older people remains an under-researched topic in India. Existing
studies have limitations and do not focus on the effectiveness of the
social pension scheme in reducing old-age poverty among the poor older
people.
Therefore, this study focuses on evaluating the targeting performance
of the social pension scheme for poor older people. The success of the
social pension scheme in reducing old-age poverty depends on whether
it reaches the poor older people, which needs to be assessed accurately.
Firstly, we try to understand the extent to which social pensions are
reaching the poor elderly population, which is a crucial requirement to
evaluate the effectiveness of social pension schemes in developing
countries like India, which face similar targeting challenges.
Secondly, from a methodological standpoint, this study contributes to
existing targeting research by comparing targeting performance
indicators to a hypothetical random distribution of social pensions.
Furthermore, by utilizing panel data to investigate the factors that
affect access to social pension benefits, this study aims to minimize
potential omitted variable bias.
Dataset used : The IHDS dataset by the National Council of Applied
Economic Research and the University of Maryland (Desai et al., 2007,
2015).
## Approach
First we import the necessary packages and create a subset of the original dataset.
Then we create a subset of the original dataset for training the model.

The columns shown here are selected and stored in the df2 dataframe.

## Preprocessing Techniques used -
First step is to remove ‘useless’ columns from the dataset ,i.e , there are some variables such as time of interview, type of roof in household , animals kept in the house ,etc.
Since these variables are not directly affecting the pension earned by an individual we remove these from the dataset.
Next up we impute the missing  values in the resulting dataset since these can interfere with our regression results .

After studying the dataset we create new variables that are needed for understanding the regression analysis. For example -
 
Here we checked that RO3 was a variable that represents female category but the categorical variable took value 2 when the gender was female . But while doing regression we prefer the categorical variable to have values as 0 or 1 . So the code above does exactly this . 

Another example is the categorical variable ID11 representing the caste took values 1  for ‘hindu’ , 2 for ‘muslim’ , 3 4 and 5 for ‘SC’ ‘ST’ and ‘OBC’ respectively . So we created 5 new variables each representing the above 5 categories where each column takes a value of 0 or 1 .

The following for loop iterates over each numeric column and performs the following steps:

Creates a boxplot for the column using boxplot(my_data[[col]], horizontal = TRUE, main = col)

Identifies potential outliers using the interquartile range (IQR) method. This is done by calling boxplot.stats(my_data[[col]]), which returns the lower and upper whisker limits of the boxplot.Increments the row_count counter for each row that contains a potential outlier.

Finally, the code identifies rows that appear in more than 5 numeric columns using outlier_rows <- which(row_count > 5) and removes these rows from the dataset using my_data <- my_data[-outlier_rows, ].In summary, the code detects potential outliers in numeric columns using boxplots and the IQR method and removes rows that contain many outliers.

