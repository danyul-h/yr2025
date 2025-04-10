![[Pasted image 20250327084323.png]]
there are n people. only two of them have purple skin. we want to select k people from the n people. rhs: by def. lhs: we partition by the number of purple skinned people we select. if we select none, there are 3rdC ways to select k people from the remaining n-2 people. If we select one, there are 2 ways to select one of the two purple skins, and for each of those ways there are 2ndC ways to select the remaining k-1 people from the nonpurple n-2 people. If we select both the two purple skins, there are 1stC ways to select the remaning k-2 people from the n-2 non purple people.
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
* partition by the number of blue people who get homes
* suppose exactly k blue people get homes, which is atleast one because there has to be someone with the castle
* there are C(n, k) ways to select k of the n blue people to have a home
* for each of the C(n, k) ways, there are k ways to select 1 person from the k blue people with homes to have a castle
* for each of those k ways, there are C(n, k) ways to select k of the n red people to be homeless, meaning the rest have homes

![[Pasted image 20250316231111.png]]
> this is famously known as the hockey stick lemma, related to pascal triangle and finding sums with a hockey stick shape
![[Pasted image 20250317230746.png]]

free vars: n, r
intro:
* there are n+1 pots in a line
* there are r+1 flowers
* while the left most pot is at position 1, while the right most pot is at position n+1 
claim:
* both sides count the amount of ways to put the flowers into the lined up pots
right:
* there are C(n+1, r+1) ways to choose r+1 pots to fill with flowers from the total n+1 pots
left:
* partition by the amount of pots to the left of the last flower, if the last flower will always have the greatest position out of all the flowers placed
	* so we already chose where to place 1 flower, meaning there are r left to place, and there can be at most n pots left if the last flower is placed at n+1
* suppose k is the amount of pots to the left of the last flower
* there are C(k, r) ways to choose r pots to fill the remaining k pots
### hw due 3/18, p.238
> 13, 18, 19

![[Pasted image 20250317220728.png]]
free vars: n, y
intro:
* there are n kids
* we have y different donut flavors
* we also have one ice cream flavor
* we want to give everyone but one kid to get a treat
* the treat can be either the ice cream or one of the y donut flavors
claim:
* both sides count they number of ways we divvy up the treats to the kids
left:
* choose one of the n kids to not get a treat
* there are (1+y)^(n-1) ways for all of the n-1 remaining children to select a treat from the 1+y options available to them
right:
* partition by the amount of people who don't get the ice cream
* let r be the number of people who don't get the ice cream
* there are C(n, r) ways to select r kids to not get the ice cream from the n total kids
* for each of the C(n, r) ways, there are r ways to choose one of the kids who don't get the ice cream to not get anything at all
* for each of those ways, there are y^(r-1) ways for all of the r-1 children who must be getting donuts to select from the y options of donut flavoring

![[Pasted image 20250316215602.png]]
free vars: n, r {0 <= r <= n}
intro:
* we have n+1 pots lined up
	* they're ordered such that the most left position is 1, while the right most is n+1
* we select r+1 of them fill with flowers
claim: 
* both sides count the number of ways we can select pots to insert flowers
rhs:
* choose select r+1 pots to fill with flowers from the total n+1 pots
lhs:
* partition by the amount of empty spaces in between the last flower and first flower
* let k be the amount of empty spaces in between the last flower and first flower
	* at most, k should be n-r, if the last flower is at the n+1 position, there are there are n positions to the left and r of those will be taken by the remaining flowers, so n-r empty spaces
	* n-r = (n+1 - 2) - (r+1  - 2)
* there are C(r+k, r) ways to choose where the remaining r flowers from the r+k range of pots
* with the way we partition,
	* note that the last flower should automatically be r+k positions to the right of the first flower

![[Pasted image 20250317230342.png]]
* n red people
* n blue people
* big party
* either they go or dont
* both sides count how many ways the 2n people can go to the party
* right
	* there is a way such that 1 person has already made their choice
	* and the rest have a binary choice
	* 
* left
	* we have a group of 2n+1 people
	* partition by how many people come overall
	* max of n
	* either 0, 1, 2, 3, ..., n-1, n people go
* 