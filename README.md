## difflib2
### difflib2 is a copy of difflib plus one function named .ratio_min() at line 558

.ratio_min(self,m) is an extension of the function .ratio(). Equivalently to .ratio(), it returns a measure of two sequences' similarity (float in [0,1]).
In addition to .ratio(), it can ignore matched substrings of length less than a given threshold m. 

The score is calculated as 2.0*M_min / T.

Where T is the total number of characters (both sequences), and
M_min is the number of elements matched with every single match having length at least m. 

Equivalently to .ratio(), .ratio_min() is applied to the output of SequenceMatcher(None, a, b) where a, b are the two sequences compared.

Note that this is 1 if the sequences are identical, and 0 if
they have no substring of length m or more in common.
.ratio_min() is similar to .ratio(). 
.ratio_min(1) is equivalent to .ratio().

### Use example

s = SequenceMatcher(None, "abcd", "bcde")

s.ratio_min(4)

        
