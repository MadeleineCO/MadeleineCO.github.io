[[2023-02-13]]

1. Statistics
	1. Why study?
		1. Objective is the evaluation of numbers
		2. Population description
			1. Sample statistics
				1. Allows us to make predictions
				2. Can make inferences for the entire population from that sample
				3. Should not be biased (large, random, diverse, etc.)
					1. Random sampling
						1. Inferences from a population
						2. Ex: Weaning weight in Hereford cattle
							1. Must take a random sample then analyze data
							2. Allows you to infer weaning weight in population of Hereford cattle
			2. Ex: Backfat thickness in Hampshire hogs
		3. Allows us to estimate an unknown value
			1. Ex: breeding value
	2. Why do we need to measure traits?
		1. Variation
		2. "Raw material" breeder has available for herd improvement
2. Discontinuous variation 
	1. Qualitative traits
		1. Few, discrete genes
	2. Phenotype not greatly influenced by env
3. Continuous variation
	1. Quantitative traits (polygenic)
		1. Many genes
	2. May involve many small graduations that are almost imperceptible to one another
	3. Usually economically important traits
	4. Highly complex
4. Population parameter = a number that describes the population
	1. Numerical descriptive measure for a pop
	2. Ex: population mean & variance
		1. Mean = average
		2. Variance is the spread around the mean
	3. Sample statistics
		1. Numerical descriptive measures for a sample
			1. Estimate of population parameters
5. Central Tendency
	1. In normal distribution, values are clustered at the midpoint (of a range of values), thinning out symmetrically toward both extremes
	2. The central tendency involves a single value at the middle of the distribution 
	3. Ex: Bell curve
	4. Can move the mean in positive or negative direction through selection
		1. Shifting the curve
	5. Biological measurements tend to be normally distributed
	6. Three measures of central tendency
		1. Median = the value halfway between the two extreme values
		2. Mode = the class w/ the highest frequency
			1. Value that appears the most
		3. Mean = the avg of all measurements in the population
			1. From a sample
			2. Mean is the most useful stat for estimating central tendency in most pops 
			3. Samples from a normally distributed pop may show departure from normality
			4. Mean = Avg X = Sigma X/n
				1. Mean = (+ n1 n2 n3 ...) / total # of values
				2. Sigma = sum
		4. Ex: Test scores
			1. 95, 86, 78, 90, 62, 73, 89, 92, 84, 73
			2. Arrange in order of magnitude: 62, 73, 73, 78, 84, 86, 89, 90, 92, 95
			3. Median = (84 + 86)/2 = 85
			5. Range = the lowest to the highest = 62-95
			6. Mode = 73 (occurs twice while all others occur only once)
6. Variance (S^2)
	1. Measure of distribution (division about the mean)
	3. Defined as the avg squared deviation of observations from their mean
		1. Sqrt variance = standard deviation
		2. S^2 = (Sigma (X - Mean)^2)/(n-1)
		 $$Variance = s^{2} = \frac{\sum (X - \bar{X})^{2}}{n-1}$$
	4. To compute variance:
		1. Each observation in a pop sample first has the mean subtracted from it
		2. These deviations from the mean are first squared
		3. Then squared deviations are summed
		4. This sum of squared deviations is then divided by n-1
	5. Ex: weaning wgt - mean = 500 lbs
		1. See chart on canvas
		2. Subtract the mean from each observation then square
		3. Sum the squared deviations then divide by n-1
	6. Can be used to compare between different populations
		1. Ex: Comparing variance between Berry's cows and UGA's cows
		2. Only useful if you are looking at several pops
	7. Standard Deviation
		1. "Typical" Deviation, in abs value, of an observation drawn at random from the pop, from its mean
		2. s = sqrt(variance) = sqrt(s^2)
		3. Ex: variation = s^2 = 14,000 and mean = 500
			1. s = sqrt(14,000)
			2. Standard deviation = 118.3
			3. Range = 618.3-382.7
				1. Mean + or - 1 SD = 68% of population
					1. About two thirds of pop within 
					2. ---
				2. Mean + or - 2 SD = 95% of population
					1. ---
				3. Mean + or - 3 SD = 99% of population
					1. ---
		4. Allows you to get a range of values around the mean
			1. Individuals outside of this range may have problems
		5. How can s be used?
			1. Can describe variance in a pop
			2. Helps us picture how much variation actually exists for a trait
		6. Standard Error
			1. Refers to how accurately the mean has been estimated
			2. If the mean is computed again from a different sample of n individuals drawn at random from the same pop, how closely would the new estimate of the mean correspond to the former one?
			3. SE = SD/sqrt(n) = sqrt(variance)/sqrt(n)
