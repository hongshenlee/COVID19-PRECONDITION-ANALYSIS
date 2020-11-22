# COVID19-PRECONDITION-ANALYSIS

This is A&A project for ADA course

## 1.Acknowleagement

### 1.1 Background

Coronavirus disease (covid-19) is a newly discovered infectious disease caused by a coronavirus. It is a kind of virus that is aimed at the respiratory tract of susceptible patients. According to WHO, this is the fourteenth worldwide pandemic. Due to the characteristics of today's world, the epidemic is the most widespread and is suffering almost all over the world.

Most people infected with covid-19 experience mild to moderate respiratory disease that can be cured without special treatment. Older people, as well as those with underlying diseases such as cardiovascular disease, diabetes, chronic respiratory disease, and cancer, are more likely to develop serious diseases.

Obviously, the virus has different degrees of impact on different physical conditions. I hope to be able to find out the relationship between the preconditions and the severity of symptoms after infection. This study will help us to make more informed decisions on what aspects we can consciously protect ourselves, how to protect specific vulnerable groups, and what degree of measures should be taken for people infected with the virus.

### 1.2 Dataset Description

This data-set was released by the Mexican government. This data-set contains 566,602 records of anonymised patient-related information.

## 2.Data Processing

### 2.1 Load And Clean Data

1. As mentioned above, `97`,`98`and `99` have no specific meanings

1. For most fields, `1` represents yes, `2` represents no

### 2.2 Data Exploration

Since there are many two-value(yes or no) fields, we can consider whether it's a valid
factor by comparing their counts in different `covid_res` groups.

## 3 Model

From the rough analysis above, we can take some fields as the important candidates to build our models.
They are `contact_other_covid`,`obesity`,`hypertension`,`pneumonia`,`diabetes`,`pregnancy`,`sex`,`icu`,`intubed`,`tobacco` and `age`.

I choose `lm` to build the model and do the analysis

## 4 Conclusion

Consistent with our previous analysis, these variables have an impact on the final result, because their p-values are less than 0.05, which means significant.

Different fields have different `Estimate ` and `F-vallue`, which means they would have different degree impacts on the `covid_res` results.

In conclusion, `obesity`, `pregnancy`,`intubed`,`tobacco`,`contact_other_covid` are relatively more Influential 