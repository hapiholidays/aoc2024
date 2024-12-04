# December 4th: Word Search

## Part 1
Given a table of letters find the number of occurances of "XMAS" in any of the 8 directions.

### Implementation
There are many ways to implement this, but under time preassure I opted for the
simple but not very compact or maintainable solution to implement one service
for each direction
 - wordsearchLR: Searching horizontal text direction
 - wordsearchRL: Searching reverse horizontal text direction
 - wordsearchUD: Searching vertical text direction
 - wordsearchDU: Searching reverse vertical text direction
 - wordsearchULDR: Searching diagonal text direction
 - wordsearchDRUL: Searching reverse diagonal text direction
 - wordsearchURDL: Searching back-diagonal text direction
 - wordsearchDLUR: Searching reverse bac-diagonal text direction

## Part 2
In stead of searchin for XMAS we are now searching for MAS crosses.

### Implementation
This is somewhat simpler, and I used just a single service, and even
implemented an optimization to not fech the lines from the list multiple times.

We could consider optimizing the service for multicore utilization, but
execution takes about 0.2 seconds on my machine, so it is hardly worth the
efford at this point. So we save this joy for later puzzles.
