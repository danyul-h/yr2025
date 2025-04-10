
![[Pasted image 20250327084323.png]]
there are n people. only two of them have purple skin. we want to select k people from the n people. rhs: by def. lhs: we partition by the number of purple skinned people we select. if we select none, there are 3rdC ways to select k people from the remaining n-2 people. If we select one, there are 2 ways to select one of the two purple skins, and for each of those ways there are 2ndC ways to select the remaining k-1 people from the nonpurple n-2 people. If we select both the two purple skins, there are 1stC ways to select the remaning k-2 people from the n-2 non purple people.

p.237#15,10,3,12,9,11,14
![[Pasted image 20250326201000.png]]
Intro: 
	There are n roommates that share a house and a car. They need to form a shopping committee to go out and buy groceries for the week. At least one person has to be in the shopping committee and only one of the people in the committee will be selected as the driver.
Claim: 
	Both sides count the number of ways to create a shopping committee with the driver assigned from the n roommates
RHS: 
	There are n ways to select 1 of the n roommates to be the driver. For each of those n ways, there are $2^{n-1}$ ways to make the binary decision of whether or not each of the remaining n-1 roommates are in the shopping committee. So, there are $n2^{n-1}$ ways in total
LHS: 
	We partition the total ways to create a shopping committee by the number of people who will are in the shopping committee. Let k be the number of people in the shopping committee. $1 \leq k \leq n$. There are $\binom{n}k$ ways to select k of the n roommates to be in the shopping committee. For each of those ways, there are k ways to select 1 of the k people in the shopping committee to be the driver. So, there are $\sum\limits_{k=1}^n k \binom{n}k$ ways in total.
![[Pasted image 20250326203529.png]]
Intro:
	There are a white cars and we want to paint b of them red. Then, we also want to add stickers to c of the b cars we painted red.
Claim: 
	Both sides count the number of ways to paint and sticker the a white cars.
LHS: 
	There are $\binom{a}b$ ways to select b of the a cars to get painted red. For each of those ways, there are $\binom{b}c$ ways to sticker c of the b painted cars. So, there are $\binom{a}b \binom{b}c$ ways in total.
RHS:
	There are $\binom{a}{b-c}$ ways to select the b-c cars that only get painted red and don't get stickered from the a total cars. For each of those ways, there are $\binom{a-b+c}c$ ways to select c cars of the remaining a-b+c cars to paint red and sticker. So, there are $\binom{a}{b-c} \binom{a-b+c}c$ ways in total.

![[Pasted image 20250326204555.png]]
Intro:
	There is a big family of n red people and a big family of n blue people. Together they create a kingdom of 2n people. However, we need to select 2 people from the kingdom to be rulers.
Claim:
	Both sides count the number of ways to select 2 rulers from the 2n red and blue people.
LHS:
	By definition, there are $\binom{2n}2$ ways to select 2 people to be rulers from the 2n total people
RHS:
	We partition the total number of ways to select the 2 rulers by whether or not the 2 rulers are of the same color family. If the rulers are of the same color family, there are 2 ways to select which family they are from, red or blue. For each of those ways, there are $\binom{n}2$ ways to select 2 rulers from the selected family of n people. If the rulers are from different families, there are n ways to choose 1 ruler from the red family, and for each of those ways there are n ways to choose 1 ruler from the blue family, so $n^2$ ways. So, in total, there are $2 \binom{n}2 + n^2$ ways.

![[Pasted image 20250326205558.png]]
Intro:
	There are n cats and n dogs at the pet store. We want to adopt n of the 2n pets.
Claim: 
	Both sides count the number of ways we can adopt the 2n pets.
RHS:
	By definition, there are $\binom{2n}n$ ways to select n of the pets to adopt from the 2n total pets.
LHS:
	We partition the total number of ways we can adopt the 2n pets by the number of pets that are cats. Let k be the number of cats that we adopt. $0 \leq k \leq n$. There are $\binom{n}k$ ways to select k cats from the n total cats to adopt. For each of those ways, there are $\binom{n}k$ ways to select k dogs from the n total dogs to not adopt, while the rest do get adopted--this is because k spots were already taken by the cats, so we can't choose k dogs. So, in total there are $\sum\limits_{k=0}^n {\binom{n}k}^2$  ways.

![[Pasted image 20250326210639.png]]
Intro:
	There are n total workers, and there we select one of them to get a new office. We also select another, possibly same, worker to get a promotion.
Claim:
	Both sides count the number of ways we can give a new office and a promotion to the n workers.
LHS:
	There are n ways to select 1 of the n workers to get a new office and for each of those ways, there are n ways to select 1 of the n workers to get a promotion. So, in total, there are $n^2$ ways.
RHS:
	We partition the total number of ways we can give a new office and a promotion to the n workers by whether or not the same person gets the new office and a promotion. If 2 different people get the office and promotion, there are $\binom{n}2$ ways to select 2 workers from the n workers to be awarded. For each of those ways, there are 2 ways to select which of workers to be awarded will get the office and for the other to get the promotion. If the same person gets the office and promotion, there are $\binom{n}1$ ways to select 1 of the n workers to be awarded both. So, there are $2 \binom{n}2 + \binom{n}1$ ways in total.

![[Pasted image 20250326211434.png]]
Intro:
	There are n people. We're a free ice cream stand that only has 3 flavors, vanilla, chocolate, and mint. Each person gets only 1 ice cream flavor that we select.
Claim:
	Both sides count the number of ways we can give out the ice cream to the n people
RHS:
	Since we have to select 1 of the 3 flavors for each of the n people, there are $3^n$ ways we can give out the ice cream
LHS:
	We partition by the number of people who aren't given mint. Let k be the number of people who aren't given mint. There are $\binom{n}k$ ways to select k of the n people to not be given mint, the others will automatically be given mint. For each of those ways, there are $2^k$ ways to select 1 of the 2 remaining flavors (vanilla and chocolate) for each of the k people who don't get mint. So in total there are $\sum\limits_{k=0}^n \binom{n}k 2^k$ ways. 

![[Pasted image 20250326212400.png]]
![[Pasted image 20250326212942.png]]
Intro:
	There are n+1 red tulips and k blue tulips. We plant them in a row, left to right, and can create different color patterns of the line of tulips.
Claim:
	Both sides count the number of different patterns of tulips we can create.
RHS:
	By definition, there are $\binom{n+k+1}k$ ways to select where to put the k blue tulips in the row with n+k+1 total spots, and it is also the total number of patterns we can create.
LHS:
	We partition by the number of blue tulips left after the first red tulip. Let j be the number of blue tulips left after the first red tulip--recall we plant left to right. $0 \leq j \leq k$. This means that there are n+j remaining spots after the first red tulip--all the ones before the first red tulip must be blue, as the first red tulip, is, duh, the first red tulip. So, there are $\binom{n+j}j$ ways to select where to put the remaining j blue tulips in the remaining n+j spots after placing the first red tulip. So, there are $\sum\limits_{j=0}^k \binom{n+j}j$ total ways.
### hw due 3/17, p.237
> 17, 16, 8

![[Pasted image 20250316213934.png]]
free vars: k, n
Intro: 
	There are k red people, 1 purple person, and n blue people. We can only select k people from the total people to go to the rainbow party
Claim:
	Both sides count the amount of ways to select k people to go to the rainbow party
LHS: 
	We partition the possible # of ways of people going to the rainbow party by the # of people that came and are red. If j party-goers must be red, then there are $\binom{k}j$ ways to pick j people from the k red people. For each of those $\binom{k}j$ ways, there are $\binom{n+1}{k-j}$ ways to pick k-j people from the n+1 remaining people that are not red (comprised of blue people and the purple person) to fill out all spots of party-goers. So there are $\sum\limits_{j=0}^k \binom{k}j \binom{n+1}{k-j}$ total ways.
RHS:
	We partition the possible # of ways of people going to the rainbow party by the # of people that came and are red or purple. If j party-goers must be red or purple, then there are $\binom{k+1}j$ ways to pick j people from the k+1 red or purple people. For each of those $\binom{k+1}j$ ways, there are $\binom{n}{k-j}$ ways to pick k-j people from the n remaining not red or purple people (meaning blue) people to fill out all spots of party-goers. So there are $\sum\limits_{j=0}^k \binom{k+1}j \binom{n}{k-j}$ total ways.

![[Pasted image 20250316224137.png]]
free vars: n
Intro:
	There are n red people and n blue people. Together they make a kingdom of 2n people. n people in the kingdom will have a home, everyone else is homeless. 1 of the n people with homes will live in a castle, but it has to be a blue person.
Claim:
	both sides count the ways to select people with homes and the castle
RHS:
	There are n ways to choose one of the n blue people to live in a castle. For each of the n ways to select the person with the castle, there are $\binom{2n-1}{n-1}$ ways to choose the remaining n-1 people with homes from the remaining 2n-1 people in the kingdom. So in total there are $n \binom{2n-1}{n-1}$ ways.
LHS:
	We partition the total number of ways by the number of blue people who get homes. Suppose exactly k blue people get homes, which is at least one because there has to be someone with the castle. There are $\binom{n}k$ ways to select k of the n blue people to have a home. For each of those ways, there are k ways to select 1 person from the k blue people with homes to have a castle. For each of those ways, there are $\binom{n}k$ ways to select k of the n red people to be homeless, meaning the rest have homes. So in total, there are $\sum\limits_{k=1}^n k{\binom{n}k}^2$ ways.

![[Pasted image 20250316231111.png]]
> this is famously known as the hockey stick lemma, related to pascal triangle and finding sums with a hockey stick shape
![[Pasted image 20250317230746.png]]

free vars: n, r
intro:
	There are n+1 pots in a line. There are r+1 of the same flower, we want to plant them in the pots. Note that while the left most pot is at position 1, while the right most pot is at position n+1.
claim:
	Both sides count the number of ways to put the flowers into the lined up pots.
right:
	There are $\binom{n+1}{r+1}$ ways to choose r+1 pots to fill with flowers from the total n+1 pots, this is by definition the total.
left:
	We partition by the amount of pots to the left of the last flower, if the last flower will always have the greatest position out of all the flowers placed. Suppose k is the amount of pots to the left of the last flower. So, we already chose where to place 1 flower, meaning there are r left to place, and $0 \leq k \leq n$. There are $\binom{k}r$ ways to choose r pots to fill the remaining k pots. So there are $\sum\limits_{k=0}^n \binom{k}r$ total ways.
### hw due 3/18, p.238
> 13, 18, 19

![[Pasted image 20250317220728.png]]
free vars: n, y
intro:
	There are n kids. We have y different donut flavors and also have one ice cream flavor. We want to give everyone but one kid to get a treat. The treat can be either the ice cream or one of the y donut flavors
claim:
	both sides count they number of ways we divvy up the treats to the kids
left:
	There are n ways to select one of the n kids to not get a treat. For each of those ways, there are $(1+y)^{n-1}$ ways since each of the remaining n-1 children have 1+y options for a treat. So in total there are  $n(1+y)^{n-1}$  ways
right:
	We partition by the amount of people who don't get the ice cream. Let r be the number of people who don't get the ice cream. There are $\binom{n}r$ ways to select r kids to not get the ice cream from the n total kids. For each of the those ways, there are r ways to choose one of the kids who don't get the ice cream to not get anything at all. For each of those ways, there are $y^{r-1}$ ways for each of the r-1 children who must be getting donuts to select from the y options of donut flavoring.

![[Pasted image 20250316215602.png]]
free vars: n, r {0 <= r <= n}
intro:
	We have n+1 pots lined up and they're ordered such that the most left position is 1, while the right most is n+1. We select r+1 of them fill with flowers
claim: 
	both sides count the number of ways we can select pots to insert with flowers.
rhs:
	There are $\binom{n+1}{r+1}$ ways to  select r+1 pots to fill with flowers from the total n+1 pots. This is by definition the total ways.
lhs:
	We partition by the amount of empty spaces in between the last flower and first flower. Let k be the amount of empty spaces in between the last flower and first flower. At most, k should be n-r, because if the last flower is at the n+1 position, there are there are n positions to the left and r of those will be taken by the remaining flowers, so n-r empty spaces. Furthermore, by the way we partition, the last flower should automatically be placed once the first flower is placed--it should be r+k positions to the right of the first flower. So, there are $\binom{r+k}r$ ways to choose where the remaining r flowers from the r+k range of pots. So there are $\sum\limits_{k=0}^{n-r} \binom{r+k}r$ ways in total. 

![[Pasted image 20250317230342.png]]
Intro: 
	We're an ice cream shop with 2n+1 customers, but we only have vanilla and chocolate flavor. Furthermore, we have to give more vanilla than chocolate.
Claim:
	Both sides count the number of ways we can give the 2n+1 customers ice cream.
LHS:
	We partition by the number of customers that get chocolate. Let r be the number of customers that get chocolate. $0 \leq r \leq n$, because we want to sell less chocolate so at most it can be n. So there are $\binom{2n+1}r$ ways to select r people from the 2n+1 customers to get chocolate ice cream. So in total there are $\sum\limits_{r=0}^n \binom{2n+1}r$ ways.
RHS:
	There are $2^{2n+1}$ ways to select how the 2n+1 customers get their ice cream since each of the 2n+1 of them have a decision between vanilla or chocolate. However, half the time the chocolate will sell more than the vanilla, so there is actually a total of $2^{2n}$ ways.