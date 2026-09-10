# CMPS 2200 Recitation 02
## Answers

**Name:** Will Cunningam
**Name:**_________________________


Place all written answers from `recitation-02.md` here for easier grading.

- **4) (3 points)** Now, derive the asymptotic behavior of $W(n)$ using $f(n) = 1$, $f(n) = n$, and $f(n) = n^2$  with $a=2$ and $b=2$. Then, generate actual values for $W(n)$ for your code and confirm that the trends match your derivations.

$2W(\frac{n}{2})$ goes to $n^{\log_2 2} = θ(n)$

When $f(n) = 1$, $W(n) = θ(n)$

When $f(n) = n$, $W(n) = θ(n\log n)$

When $f(n) = n^{2}$, $W(n) = θ(n^{2})$

Examples are found in the pytests

- **5) (4 points)** Now that you have a nice way to empirically 
  generate values of $W(n)$, we can look at the relationship 
  between $a$, $b$, and $f(n)$. If $f(n) = n^c$, we can derive 
  a very nice result.
  
  The Master Method gives an easy formula for solving general 
  recurrences of the form: 

    $$T(n) = aT(n/b) + n^c$$

  Its three cases correspond to the relationship between $\log_b a$ 
  and $c$. Derive the asymptotic behavior of $T(n)$ by solving its 
  general recursion tree for each of the three cases. Show your 
  recursion tree and derivations from it.

  1. $\log_b a < c$, then $r < 1$, and $\frac{a}{b^{c}} < 1$

  $n^{c} + n^{c}r + n^{c}r^{2}$... so $θ(n^{\log_b a}) = θ(n^{c})$ because $c > \log_b a$

  2. $\log_b a = c$, then $r = 1$, and $\frac{a}{b^{c}} = 1$

  $n^{c} + n^{c} + n^{c}$... there are $\log_b n$ levels, so cost is $n^{c}\log_b n$ so $θ(n^{c}\log n)$

  3. $\log_b a > c$, then $r > 1$, and $\frac{a}{b^{c}} > 1$ 

- **7) (2 points)** Derive the asymptotic expressions for the span of the recurrences you used in problem 4 above. Confirm that everything matches up as it should. 
