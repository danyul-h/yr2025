### hw due 3/17, p.237
> 17, 16, 8

![[Pasted image 20250316213934.png]]
free vars: k, n
intro: 
* k red people,
* 1 purple person,
* n blue people,
* we can only select k people to go to the rainbow party
claim:
* both sides count the amount of ways to select k people to go to the rainbow party
left: 
* we partition the possible # of ways of people going to the rainbow party by the # of people that came and are red
* if j party-goers must be red, then there are C(k, j) ways to pick j people from the k red people
* for each of those C(k, j) ways, there are C(n+1, k-j) ways to pick k-j people from the n+1 blue or purple people to fill out all spots of party-goers
right:
* we partition the possible # of ways of people going to the rainbow party by the # of people that came and are red or purple
* if j party-goers must be red or purple, then there are C(k+1, j) ways to pick j people from the k+1 red or purple people 
* for each of those C(k+1, j) ways, there are C(n, k-j) ways to pick k-j people from the n blue people to fill out all spots of party-goers

![[Pasted image 20250316224137.png]]
free vars: n
intro:
* there are n red people
* and n blue people
* together they make a kingdom of 2n people
* n of them will have a home
* 1 of the n people with homes will live in a castle, but it has to be a blue person
claim:
* both sides count the ways to select people with homes and of those with a home, one with a castle
right:
* choose one of the n blue people to live in a castle
* for the n ways to select the person with the castle, there are C(2n-1, n-1) ways to choose the remaining n-1 people with homes from the remaining 2n-1 people in the kingdom
left:
* partition by the amount of people that are blue and we select to have homes
* let k be the amount of people that are blue and we select to have homes
* there are C(n, k) ways to select k of the n blue people to have a home
* for each of the C(n, k) ways, there are k ways to select 1 person from the k blue people with homes to have a castle
* for each of those k ways, there are C(n, k) ways to select k of the n red people to be homeless, meaning the rest have homes

![[Pasted image 20250316231111.png]]
free vars: n, r
intro:
* there are n+1 cars
* we want to paint r+1 of those cars
claim:
* both sides count the amount of ways to paint the cars
right:

### hw due 3/18, p.238
> 13, 18, 19

![[Pasted image 20250316215602.png]]
free vars: n, r {0 <= r <= n}
intro:
* we have n+1 cars
* we select r+1 of them to paint with mr. rose's face on it
claim: both sides count the number of ways we can select cars to paint
rhs:
* choose r+1 cars from our n+1 total cars to paint
lhs:
* partition by the difference in the amount of cars we have and the amount of cars we want to paint
* let k be the difference
* so there are C(r+k, r) ways to paint r cars from the r+k cars
