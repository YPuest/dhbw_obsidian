#Programmieren 

## Cases
*X* = 0:
	direction == 'L' 
		*false*
	*Y* == 0 || *Y* == 1: 
		direction == 'U'
			*false*
	*Y* == 8 || *Y* == 7:
		direction == 'D'
		  *false*

*X* = 8:
	direction == 'R'
		*false*
	*Y* == 0 || *Y* == 1:
		direction == 'U'
			*false*
	*Y* == 8 || *Y* == 7:
		direction == 'D'
		  *false*

## Checks
if moved *down*:
	- down (*Y* $\le$ 6)
	- left (*X* $\ge$ 2)
	- right (*X* $\le$ 6)

if moved *up*:
	- up (*Y* $\ge$ 2)
	- left (*X* $\ge$ 2)
	- right (*X* $\le$ 6)

if moved *right*:
	- up (*Y* $\ge$ 2)
	- down (*X* $\le$ 6)
	- right (*X* $\le$ 6)

if moved *left*:
	- up (*Y* $\ge$ 2)
	- down (*X* $\le$ 6)
	- left (*X* $\ge$ 2)

