tags: #notes #topic
creation date: [[2022-11-28 Monday]] 00:13:38
description::

listing all the hw feedback so i have all the right answers documented

[[CSCI243 hw5 latex.pdf]]
> [!HW5]
> 1c 
> 
> The next term in this series is 7. These could plausibly be either the fibonnaci numbers or the prime numbers (although 1 is generally not considered to be prime, and there is no closed form solution for the sequence of primes).
> 
> Or
> 
> Next term is 8
> 
> By inspection, the m-th Fibonnaci term in the sequence occurs 2m − 1 times.
> 
> So to find out how many numbers are in the series when the m-th Fibonnaci number completes, we can compute \sigma m i=1 (2i − 1) = m^2 (using the ”baby Gauss” summation formula of the arithmetic series).
> 
> So the last index n of the m-th Fibonacci will be n = m^2. The first index of the m-th Fibonacci is (m − 1)^2 + 1.
> 
> In the opposite direction, if we want to know which Fibonacci number to put in all positions between (m − 1)^2 + 1 and m^2, the answer is m = ⌈√n⌉, or an = Fib(⌈√n⌉).          
> 
> 4
> Let’s write the summants for any combination of i, j as a 2D array where j signifies the rows and k the columns.  Draw a table like the example on page 24 of All_lectures, and you will find if you sum each column separately, each columns sums to 1. Because there are n such columns, the total sum is n.       


i didnt do hw6 and i dont even have feedback for it bc i didnt turn anything in


[[CSCI243 hw7 latex.pdf]]
> [!HW7]
> Let’s call p =3.6E12. 
> 
> (b)  log42 n Answer: n = ⌊2p^(1/4) ⌋           -0.25
> 
> (d)  n log2 n Answer: We cannot solve this non-linear equation algebraically, but we don’t need to search 3e12 numbers. Notice that n < p and so logn < log p. Since p = nlogn < nlog p, we know that n > p/ log p. That gives us a shorter range to search. Regardless of ways to arrive to it, the answer is 98574774544.
> 
> (e)  nlog2 n Answer: Similarly logn > log p − 2loglog p. 231 < n < 232. By searching we get 3574557436.       -2
> 
> (f)  n2 Answer: ⌊√p⌋ = 1897366
> 
> (g)  (3n)3 Answer:⌊p1/3/3⌋ = 5108
> 
> (h)  2n Answer: ⌊log(p)⌋ = 41                      -0.75
> 
> (i)  n! Answer: Also non solvable, but factorials grow very fast. We can check the first few integers and we see 15! < p < 16!, so the answer is 15.
> 
> (j)  nn Answer: Similarly n cannot be 12 because 12^12 > p. So we try 11, and it works.                 -2
> 
> 4.Asymptotically it is the same as binary because log3(n) = log2(n)/log2(3) and log2(3) is a constant.


[[CSCI243 hw8 latex.pdf]]
> [!HW8]
> 1
> 
> pass1: 1,3,2,8,4,9
> pass2: 1,2,3,4,8,9
> pass3: 1,2,3,4,8,9
> pass4: 1,2,3,4,8,9
> 
> pass5: 1,2,3,4,8,9                                                     
> 
> 
> 2
> 
> 2a. 
> 
> The first loop is i from 0 to n-1, the second is from 0 to i, and the third is 1 to (n/2^j)
> 
> After calculating the inner summation and take n to outside, it will be geometric series inside.
> = 2n(n − (1 − 0.5n)/0.5) = 2n^2 − 4n(1 − 0.5^n) = Θ(n^2) 
> 
> 2b.  For I, it sums from 1 to n, for j, it sums from 1 to log I, and for k it sums from 1 to logn. Add three summations together and get Θ(n (log n)^2) 
> 
> 
> Adding 1 to logn can be approximated as nlogn, which ends like Θ(n (log n)^2)                                           -12
> 
> 
> 3 Answer:
> 
> We will prove that we can obtain all multiples of 5 prices after $140. Base case: We can obtain explicitly the following
> 25, 40,
> 50 = 25*2
> 65 = 40+25
> 75 = 50+25
> 80 = 40+40
> 90 = 65+25
> 95 –
> 100 =75+25 
> 
> 105 = 110 – 
> 
> 115 = 90+25
> 
> 120 = 3*40
> 
> 125 = 100+25
> 
> 130 = 105+25
> 
> 140 =  115+25 
> 
> I.H.: Assume that for any k,140 < 5k, any j ≤ k, with 115 ≤ 5j, can be written 5j = m25+n40.
> 
> I.S.: Consider k+1. 5(k+1) = 5k+5 = (5k−20)+25. 
> 
> However, (5k−20) is a multiple of 5 and by I.H. 
> 
> there exist m,n such that 5k−20 = m∗25+n∗40. Then 5(k+1) = (5k−20)+25 = (m+1)∗25+n∗40. QED.o           -8

![[Pasted image 20221128104142.png]]

[[CSCI243 hw9 latex.pdf]]
ok i got 49/50 for this one so basically perfect nothing to change
> [!HW9]
> 2(b)
> 
> Answer:
> 
> base:ε^R=ε .
> 
> Recursive: (wa)^R = aw^R for any word w. 
> 
> 2(c)
> 
> base: (w1ε)^R = w1^{R} = ε(w1)^{R} so it holds.
> I.H. Assume for some w2 it holds (w1w2)^R = w2^{R} w1^{R }.
> I.S. (w1(w2a))^R = ((w1w2)a)^R = definition of reversal = a(w1w2)^R = I.H. = aw2^R w1^R = definition of reversal = (w2a)^R w1^R . Proven   
> 
> -1        Prove in a more general way.

