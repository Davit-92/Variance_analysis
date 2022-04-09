# Variance_analysis
Variance analysis on selected variables and all combinations

What is Variance Analysis?
Variance analysis can be summarized as an analysis of the difference between planned and actual numbers. The sum of all variances gives a picture of the overall over-performance or under-performance for a particular reporting period. For each item, companies assess their favorability by comparing actual costs to standard costs in the industry.

For example, if the actual cost is lower than the standard cost for raw materials, assuming the same volume of materials, it would lead to a favorable price variance (i.e., cost savings). However, if the standard quantity was 10,000 pieces of material and 15,000 pieces were required in production, this would be an unfavorable quantity variance because more materials were used than anticipated.

More generally, the variance analysis is conducted to undestand the influeance of variation of different variables on end variable in different periods versus planned (budgeted ).
One of the most common and simplest examples of variance analysis is turnover change explanation through price and sales volume change effects.
For the example assume that the price of particular product in initial or base period is p_0 and sales quantity in same period was q_0, the total turnover for the period will be the product of p_0 and q_0. If the price and quantity for other period is p_1 and q_1, turnover is p_1 * q_1 the total absolute variance will be:

    variance = p_1 x q_1 - p_0 x q_0

In this case total variance is generated due to different price and sold quantity.
The sold quantity variance can be calculated by multiplying quantity change by base period price:
    
    q_i = p_0 x (q_1 - q_0)
    
    where q_i is quantity change absolute influence in variance.
In other words, q_i part of the variance is due to quantity change, or how much would be the change of turnover if only quantity would have been changed.
Same way the price variance influence is price difference scaled by base period quantity:
    
    p_i = q_0 x (p_1 - p_0)
    
    where p_i is price change absolute influence in variance.
In other words, p_i part of the variance is due to price change, or how much would be the change of turnover if only price would have been changed.

If you sum up q_i and p_i in real example, you will not get a number equal to variance. This is due to one more effect which also need to be calculated in this case. The difference is coming from the fact that price and quantity are changed together. This will not happen if one of the variables is not changed. To calculate this part of variance you will need to multiply quantity change with price change:

    pq_i = (q_1 - q_0) * (p_1 - p_0)
    
    where pq_i is price and quantity change absolute influence in variance

Finally:
    
    variance  = q_i + p_i + pq_i
    
Real life examples are much more complicated. Variance can be influenced by not only the mentioned variables but also product mix (if more than one product is sold by different price), channel mix (if the prodcuts are solld to different group of customers by different prices) etc.. If there are 3 variables (e.g. quantity, price, mix), 7 factors are calculated while in previous case quantity of factors were 3 (p_i, q_i and pq_i).
The total quantity of factors in particular case is the sum of quantity of combinations from 1 to number of variables from number of variables.

    number of factors = C1(n) + C2(n) + ... + Cn(n)
    
    where n is the number of variables.
    
This project is aimed to calculate and return all factors and visulaize them in bridge chart if requested.
Chart is sorted from in descending order of absolute values of factors, and some of the factors which have less influence than the defined threshold are grouped in "other".

The project is written in python (jupyter notebook).
