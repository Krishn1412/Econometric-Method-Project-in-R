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

##Approach

First we import the necessary packages and create a subset of the original dataset.
Then we create a subset of the original dataset for training the model.

The columns shown here are selected and stored in the df2 dataframe.

Preprocessing Techniques used -

 First step is to remove ‘useless’ columns from the dataset ,i.e , there are some variables such as time of interview, type of roof in household , animals kept in the house ,etc.
Since these variables are not directly affecting the pension earned by an individual we remove these from the dataset.

Next up we impute the missing  values in the resulting dataset since these can interfere with our regression results . The 
