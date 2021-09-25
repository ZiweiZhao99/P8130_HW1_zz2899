Homework1
================
Ziwei Zhao

``` r
library(tidyverse)
```

### Problem 1

**a)**  
qualitative, ordinal

**b)**  
qualitative, binary

**c)**  
qualitative, nominal

**d)**

quantitative, continuous

**e)**  
quantitative, discrete

### Problem 2

**a)**

``` r
c1 <- c(45, 39, 25, 47, 49, 5, 70, 99, 74, 37, 99, 35, 8, 59)
summary(c1)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##    5.00   35.50   46.00   49.36   67.25   99.00

``` r
sd(c1)
```

    ## [1] 28.84603

mean = 49.36  
median = 46  
range = 99-5 = 94  
SD = 28.85

**b)**

``` r
boxplot(c1)
```

![](Homework1_ZiweiZhao_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

The data is mostly symmetric but slightly right-skewed. There is no
outlier. 50% of the data are between \~35 (Q1) and \~67 (Q3), and the
range is from 5 to 94, so the data is very likely to be a bell-shaped
unimodal distribution.

**Additionally, …**  
**a)**

``` r
c2 <- c(67, 50, 85, 43, 64, 35, 47, 97, 58, 58, 10, 56, 50)
df1 <- data.frame(Score = c1, Type = c("bike crash"))
df2 <- data.frame(Score = c2, Type = c("car crash"))
All <- rbind(df1, df2)

boxplot(Score~Type,
        data=All,
        main="Boxplot of the Depression Score",
        xlab="Type of Accident",
        ylab="Depression Score"
)
```

![](Homework1_ZiweiZhao_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

**b)**  
The box plot of bike crash has been described in part b) (The data is
mostly symmetric but slightly right-skewed. There is no outlier. 50% of
the data are between \~35 (Q1) and \~67 (Q3), and the range is from 5 to
94, so the data is very likely to be a bell-shaped unimodal
distribution). For car crash, the data is symmetric and not skewed.
There are two outliers, which means 11/13=84.6% of the data are between
\~35 and \~90, and 50% of the data aggregated beteween \~47 (Q1) and
\~64 (Q3), so the data is a bell-shaped unimodal distribution.

**c)**  
Although the box plot for the data of bike crash appears to have larger
range and interquartile range, its median is smaller and it is
right-skewed. So the group of bike crash appears to have a lower typical
depression score.

### Problem 3

**a)**  
*P*(*A*) = 6/12 = 50%

**b)**  
*P*(*B*) = 1/12 = 8.33%

**c)**  
*P*(*B* ∪ *A*) = *P*(*B*) + *P*(*A*) − *P*(*B* ∩ *A*)  
*B* ⊂ *A* ⇒ *P*(*B* ∩ *A*) = *P*(*B*)  
 ⇒ *P*(*B* ∪ *A*) = *P*(*B*) + *P*(*A*) − *P*(*B*) = *P*(*A*) = 50%

**d)**  
$P(A \\mid B) = \\frac{P(A \\cap B)}{P(B)} = \\frac{P(B)}{P(B)} = 1$  
*P*(*A*) = 50%  
*P*(*A* ∣ *B*) ≠ *P*(*A*)   (1)

$P(B \\mid A) = \\frac{P(A \\cap B)}{P(A)} = \\frac{P(B)}{P(A)} = 1/6$  
*P*(*B*) = 1/12  
*P*(*B* ∣ *A*) ≠ *P*(*B*)   (2)

By (1) and (2), and the definition of independent events, events A and B
are not independent.

### Problem 4

Given that *P*(*D*) = 5%, *P*(*D*<sup>*c*</sup>) = 95%,
*P*(*P* ∣ *D*) = 80%, *P*(*P* ∣ *D*<sup>*c*</sup>) = 10%, by LTP,  
then we have
