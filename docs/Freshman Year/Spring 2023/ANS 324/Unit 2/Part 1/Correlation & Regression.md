[[2023-02-15]], [[2023-02-17]]

1. Correlation measures the strength of the relationship between two variables
	1. Is one trait of an animal associated w/ another?
	2. Ex: 
		1. Is height at withers in beef cattle associated w/ body length?
		2. Is weight of a dairy cow related to amount of milk produced?
2. Correlation coefficient r measures the degree of association between two variables (traits) in a sample from a population
	1. Measures the degree of tightness in the relationship between two traits
	2. Range = -1.0 to +1.0
		1. Correlation of +1.0 indicates that for each standard unit increase in one variable, there is a standard unit increase in the correlated trait
			1. Strong positive correlation
			2. Positive indicates that they increase or decrease together
				1. Negative = as one trait increases, other trait decreases
		2. A significant correlation (statistically speaking) means that there is a high probability of a real association between the traits
			1. A star next to a correlation value indicates that the number is significant and has been tested
		3. Low: r = 0.1-0.2
		4. Medium: r = 0.21-0.4
		5. High: r = 0.41-0.99
	3. Gene linkage and pleiotropy create correlation
		1. One of these are responsible for any correlation between traits
	4. Correlation is unitless 
		1. Unlike regression, which takes on the unit of the trait
3. Correlation cannot be used to predict the level of one variable based on the second
	1. No basis for cause and effect determination
		1. Correlation does not automatically indicate causation
		2. r proves no evidence as to which variable is the cause and which is the effect
4. Correlation Ex
	1. Hip height vs weight                          | +
	2. Milk (lbs) vs Fat %                              | -
	3. Weight vs heart girth                         | +
	4. Weaning weight vs yearling weight   | +
	5. Lean cuts vs backfat                           | -
	6. Other examples of correlated traits. . .![[Pasted image 20230215102319.png]]
		1. Maternal calving ease = ---
		2. Direct calving ease = ---
5. Correlation Coefficient Formula
	1. $$r = \frac{\sum XY - \frac{\sum X\sum Y}{N}}{\sqrt[2](({\sum X^{2} - \frac{(\sum X^{2})}{N})(\sum Y^{2}-\frac{(\sum Y)^{2}}{N}))}}$$
	2. List Xs and Ys first then list XYs then list X^2s and Y^2s
	3. After listing these values, sum all
	4. Then plug in formula
		1. Don't forget to find the sqrt of the denominator
	5. The result should always fall within -1.0 to +1.0
6. Correlation Summary![[Pasted image 20230215103516.png]]
	1. Ex of correlation does not equal causation
		1. People who drowned after falling out of a fishing boat and Marriage rate in Kentucky
	2. Ex of animal correlations
		1. Correlation between fleece weight in lambs and weaning weight
		2. Correlation between scrotal circumference and age at puberty in cattle
7. Most common correlations in animal breeding
	1. Phenotypic correlation = measures the strength of relationship between performance (phenotypic value) in one trait and performance in another trait
		1. $r_p$ = phenotypic correlation
	2. Genetic correlation = Measures strength of relationship between BV for one trait and BV for the other
		1. One breeding value correlates with another breeding value
		2. More important then phenotypic correlation
			1. Important bc the concept of correlated response to selection
				1. Selection for one trait leads to selection on another trait
		3. Ex: feed conversion and weight gain in swine
			1. r between SC at age of puberty is -0.9
			2. If a breeder selects for large SC in bulls, they can expect to have a younger age at puberty for both male and female offspring
		4. $r_g$ = genetic correlation
	4. Environmental correlation = measure of strength of relationship between environmental effects
		1. Often used for management purposes 
		2. Ex: env correlation between avg daily gain and back fat thickness in swine is +0.4
			1. Suggests that env is conductive for rapid weight gain to produce fatter pigs
		3. $r_e$ = env correlation
8. Regression Coefficient
	1. Measures the change in Y response per unit change in X within the given range of values
		1. Regression can be used to predict one value based on another (unlike correlation)
	2. Can be + or -
	3. Has representative units for the traits of interest (unlike correlation)
	4. Regression Formula $$\frac{\sum XY - \frac{\sum X\sum Y}{n}}{\sum X^{2}-\frac{(\sum X)^{2}}{n}}$$
		1. This is just one part of the correlation formula
			1. $$r = \frac{\sum XY - \frac{\sum X\sum Y}{N}}{\sqrt[2](({\sum X^{2} - \frac{(\sum X^{2})}{N})(\sum Y^{2}-\frac{(\sum Y)^{2}}{N}))}}$$
			2. The numerator is the same
			3. The denominator just contains the first segment (no sqrt)
	5. Variables![[Pasted image 20230217102215.png]]
		1. Y (predicted) = bX + a
			1. a = Y (mean) - bX (mean)
			2. b = slope (regression coefficient)
				1. The greater the slope, the closer the association between two traits
				2. b = 0 = no association between traits
				3. b = 0.7 = relatively close association
					1. Same scale as correlation
			3. a = y-intercept
			4. X = the independent variable
				1. X is X observation
				2. X (mean) of X observations
					1. More observations is better
					2. Degree of variation among observations (less is better)
				3. Determines what will happen to Y (the dependent variable)
		2. Y (mean) = avg of Y observations
		3. This is the equation of a straight line
	6. Regression is more useful than correlation bc you can make prediction
		1. Regression is tot applicable outside range of values used
			1. Always very specific to the population you are taking values from 
	7. Regression is the avg or expected change in variable Y per unit change in X (both expressed in terms of their original units of measure)
		1. $b_{yx}$ = regression of Y on X
		2. There is an assumption of cause vs effect
		3. Variation in trait X influences variation in trait Y
	8. X = "cause" variable (independent), while Y = "effect" variable (dependent)
		1. Ex: weaning wgt in beef cattle
			1. *Age* is the *cause* of variation in *weight*
				1. Age = X (cause)
				2. Weight = Y (effect)
			2. Y (weaning wgt) = a + b (regression coefficient) * X (age)
	9. Regression is used when we want to predict the numerical value of one trait from the phenotypic value of another
		1. May be difficult or expensive to measure Y directly
		2. Ex: yield grade or cutability for pork carcasses
			1. Allows you to predict the yield grade before you cut in
	10. Regression examples
		1. The estimate of regression of fleece wgt at the 60 day weighing wgt in lambs: 0.04 lb per 1 lb
			1. For every pound increase in weaning wgt, there will be a 0.04 lb increase in fleece wgt
			2. Can use to make decisions about which animals to cull and which to keep
		2. Regression of BV for age at puberty and that of SC in cattle: -8.5 days per centimeter
			1. Fer every centimeter in scrotum circumference, the progeny of that animal will reach puberty 8.5 days earlier