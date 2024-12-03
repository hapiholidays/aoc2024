# December 3rd: Corrupt program evaluatiopn

## Part 1
Given a chunk of corrupt code try to evaluate, by locating all mul(n1,n2) statements, and sum all the resultes (n1*n2).

### Implementation
This would be easy if Hapi had regular expressions, unfortunately the lazy git implementing hapi and its standard lib has not gotten around to this yes, so we have to do our own dirty work.

This requires our Process method (by using the submethod FindMuls) to constantly test if we are currently at a "mul(" substring, and if so proceed to test if it can find n1 then comma, then n2 and finally an endparenthesis - implemented bt the submethods FindN1 and FindN2.

Not a super implementation - but it gets the job done.

## Part 2
We are now required to recognize the extra don't() and do() statements, which
discards the mul statements between them.

### Implementation
For part 2, we could simply remove the substrings between don't() and do()'s by using a vim macro or something, but sol2.pi has been extended such that it recognizes the extra statements, and uses an 'on' boolean argument to keep track of when to include the results in the sum and when to ignore them.
