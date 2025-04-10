> notes on "Algorithmic monoculture and social welfare" by Jon Klienberg and Manish Raghavan

### the problem
* algorithmic monoculture
	* using algorithms for high-stakes screening decisions
		* such as employment or lending loans (the motivating scenarios in this paper)
	* they're more "accurate" than alternatives "case-by-case" but in a system?
	* is algorithmic monoculture susceptible to failures?
		* we know it is in biological settings
			* in agriculture, a monocultural system can be severely harmed during "unexpected shocks"--like pathogens
### findings
* even under "normal operations" quality of decisions decrease with algorithmic monoculture
	* we don't even need "unexpected shocks" to suffer from algorithmic monoculture
* so... the introduction of more accurate algorithms can still decrease social welfare because it drives the firms into a "unique equilibrium that is worse for society than the one that was present before the algorithm existed"
	* reference to "Braess's paradox" but for algorithmic decision-making
	* Braess's paradox: adding one or more roads to a road network can slow down traffic flow through it
	* note that harm is to overall performance
		* their results show that it would "be a mistake" to view the harm to specific applicants as balanced against the gains in overall accuracy
			* specific applicants, referring to those that are "locked out of the market" by the shared algorithms
### how it was done...
* focus on algorithmic hiring
	* recruiters make decisions based in part on scores or recommendations
	* these scores/recs are from data-driven algorithms
* the paper proposes and analyze their own stylized model of algorithmic hiring
* created a simplified hiring process
	* 2 firms, both have their own random, private rankings (human evaluator)
	* there's also the algorithmic ranking, which is public, so this ranking is same for both firms
	* if both select from algorithmic ranking, it is randomly selected which one gets the first, and then the other gets the second hire

![[Pasted image 20250316235008.png]]

### modeling ranking
![[Pasted image 20250317103331.png]]
![[Pasted image 20250317103233.png]]
* there are n candidates
* every i candidate has an x sub i intrinsic value
* employers will get this value from hiring candidate i
* candidate 1 will have x sub 1, and x sub 1 is greater than x sub 2 and so forth
* but these values are unknown, not linked to candidates, to the employer
	* they use a noisy procedure to rank the candidates
* a noisy permutation family, F theta
	* is a distribution of permutations--the rankings of the different candidates
	* distribution meaning these permutations have different probabilities of being chosen
		* as theta approaches infinity, then the true ranking--pi star--will 100% be chosen
		* theta is an "accuracy parameter"
		* greater thetas will always expect a better or as good first choice than lesser thetas, even after some candidates are removed
	* the probability for any permutation drawn for continuous and differentiable in theta 
* objective function
	* evaluates the effects of different approaches to ranking and selection
	* will consider each individual employer's utility
	* and the sum of employers' utilities
		* this is the social welfare, as it represents total quality of hired applicants
* modeling selection
	* each firm has same pool of n candidates
	* using the noisy permutation family, get a permutation pi
		* but first choose between...
		* private human evaluator, all firms have same theta H
			* but the ranking is independent of any other firm
		* algorithmically generated, has theta A
			* but the ranking is identical for all firms that choose this
	* in random order, each firm hires highest-ranked remaining candidate according to their ranking
	* sets up a "game-theoretic setting"
		* both firms know the accuracy parameters
		* they also know all the values of the candidates, but don't know the identities of the candidates that those values belong to
			* mimics real life, many ranking models depend not just on accuracy, but also on underlying candidate values
* results
	* condition: preference for the first position
		* independently draw two permutations pi and sigma from same f theta
		* and suppose the first-ranked candidates are not the same in the two permutations
		* then, the first-ranked candidate in pi is strictly greater than the expected value of second ranked candidate in pi
		* **this means that with the human evaluator, the first ranked candidate is always strictly greater than the second ranked candidate**
	* condition: preference for weaker competition
		* suppose theta 1 > theta 2
		* draw pi from f theta 2
		* and sigma from f theta 1 
		* and tau from f theta 2 
		* one permutation of pi delete tau sub 1
		* and permutation of pi delete sigma sub 1
		* the first-ranked candidate of pi without the first-ranked candidate from the less accurate tau will be expected to be greater than the first-ranked candidate of pi without the second-ranked candidate from the more accurate sigma 
		* **so when a random candidate is removed from pi, the best remaining candidate is better when the candidate is chosen based on a noisier ranking**
	* theorem one
		* given candidate distribution d 
		* and noisy permutation family f theta
		* and that they satisfy both preferences above
		* then for any theta h, there exists a theta a such that using the algorithmic ranking is a strictly dominant strategy for both firms, but social welfare would be higher if both firms used human evaluators
	* preference for independence
		* preference for weaker competition (def 3)
			* it is better to have a worse competitor
			* the firm randomly selected to hire second is better off if the firm that hires first uses a less accurate ranking
		* preference for the first position (def 2)
			* when two identically distributed (equal accuracy) permutations disagree on their first element,
			* both will still be better than their second ranked candidates
			* this implies that firms in the model rationally prefer to make decisions using independent but equally accurate rankings
		* scenario
			* when both ranking mechanisms are equally accurate
			*  given that the competitor chose the algorithm
			* the firm selected to choose second will prefer an independent ranking mechanism from its competitor--the private human evaluator
		* intuition
			* a committee seeks to hire two candidates
			* they can meet and produce a ranking sigma
				* and then hire the best candidate according to sigma
			* then they can either hire sigma 2 or make an independent ranking pi and hire pi 1
				* difference? yes!
				* they should hire pi 1 because itll be strictly greater than pi 2
* the ranking models they used for instantiation
	* Random Utility Models (RUMs)
		* doesn't always satisfy conditions, but can under realistic parameterizations
		* restricted to 3 candidates due to difficulty to work analytically
		* need to use Gaussian or Laplacian noise distributions
		* but still some problems...
		* Laplacian
			* challenges intuition that independence is preferable
			* with 15 candidates, it is actually better in expectation for a firm to use same algorithmic ranking as its competitor
			* the expected value that the second firm will get considering that the first chose algorithmic and that the second firm chose algorithmic vs. human
		* questionable if it can extend to larger numbers of candidates under Gaussian
			* maybe it can maybe it cant
		* when using rum, the standard deviation for the noise for a particular value theta is 1/theta
		* so larger values of theta will reduce the effect of the noise, making them more accurate
	* Mallows Model
		* always meets conditions
		* so for any candidate distribution D and human evaluator accuracy theta H, there exists an accuracy parameter theta A such that a common algorithmic ranking with accuracy theta A decreases social welfare
		* but still, monoculture can produce arbitrarily large negative effects
		* because it does not depend on the underlying candidate values
* conclusions
	* it is possible that monoculture causes decisions of globally lower average quality
	* even in absence of shocks
	* it is also difficult to notice its negative effects
* expansion
	* here they were focused on two firms and only one single shared algorithm
	* maybe consider rother generalizations with more firms and more algorithms
	* maybe do a case study on real world companies
	* 