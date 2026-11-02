+++
title = "Why 1 Is Not Prime"
date = 2026-11-02T12:15:34+00:00
draft = false
slug = "why-one-is-not-prime"
description = "The textbook definition of a prime lets 1 in. Twelve shows what breaks if we allow it, and why the door was shut on purpose."
summary = "A student follows the textbook definition of a prime and concludes that 1 qualifies. Factoring 12 shows what that choice would cost, and why mathematicians made the opposite choice on purpose."
categories = ["Number theory"]
tags = ["primes", "factorization", "definitions", "foundations"]
concepts = ["prime number", "unique factorization", "multiplicative identity", "empty product"]
+++

A student writes "yes" next to the question "Is 1 prime?" and the mark is taken away. At home she opens the textbook and reads the definition twice: a prime is a number whose only divisors are 1 and itself.

Her number is 1. It has exactly one divisor, which is 1, and which is also itself. Applied as written, the rule lets her answer through.

The textbook sentence is missing something, and you can find out what by spending ten minutes with the number 12.

## Twelve, broken up

Take 12 and write it as a product of smaller numbers, then keep going until no piece can be split. One route: $12 = 3 \times 4$, then $4 = 2 \times 2$, which leaves $3 \times 2 \times 2$. Another route: $12 = 2 \times 6$, then $6 = 2 \times 3$, which leaves $2 \times 2 \times 3$.

The routes differ. The leftovers do not: two 2s and one 3, in a different order. Call a collection of pieces like this a bag. The pieces that cannot be split any further are the primes, the numbers 2, 3, 5, 7, 11 and their relatives.

Before reading on, commit to a number. If you tried every possible route through 12, how many different bags could you end up with?

One. It is always the same bag.

Try a bigger number to see whether that was luck. $60 = 6 \times 10 = 2 \times 3 \times 2 \times 5$, and also $60 = 4 \times 15 = 2 \times 2 \times 3 \times 5$. Two routes, one bag: two 2s, one 3, one 5.

This holds for every whole number bigger than 1, and it is the central fact about primes. Stated once, properly: every whole number $n > 1$ is a product of primes, and any two ways of writing $n$ as such a product use the same primes the same number of times. The proof takes a page or two in a number theory course, and I am leaving it out. What matters here is what the fact gives you. A bag works as a fingerprint. Multiply a bag and you recover the number; take the number and exactly one bag comes back.

## The student's version

Now do what the student did and accept 1 as a prime. A bag is any collection of primes whose product is the number, so 1 is allowed in.

The old bag for 12 is still fine: $2 \times 2 \times 3 = 12$. But look at $1 \times 2 \times 2 \times 3$. Every piece is prime under the student's rule, and the product is still 12. So is $1 \times 1 \times 2 \times 2 \times 3$.

Guess again. How many bags does 12 have now?

Infinitely many.

Multiplying by 1 changes nothing, so you can slip in as many 1s as you like, anywhere, for free. Add none or add a million: the number stays 12 and the bag stays legal. The fingerprint has stopped being a fingerprint, because one number now owns a whole crowd of different bags.

{{< figure src="/img/why-one-is-not-prime-1.png" alt="Three horizontal rows of square boxes, each row multiplying to 12. The top row holds the boxes 2, 2, 3. The middle row holds 1, 2, 2, 3. The bottom row holds 1, 1, 2, 2, 3. The boxes labelled 1 are shaded a different colour from the others, so the eye sees the same core 2, 2, 3 repeated in every row with extra shaded boxes added on the left. To the right of each row the text reads: product is 12." >}}

Ordinary questions go sour. How many prime factors does 12 have? With the 1s allowed there is no answer, because any number from three upward is as correct as any other.

## Two ways out

There are two repairs, and both work.

The first keeps 1 as a prime and rewrites the theorem: every number has one bag, once you throw away the 1s. Then every later statement about primes needs a footnote, "other than 1", and the footnote follows primes everywhere they go.

The second repair spends its effort once, in the definition. A prime is a whole number bigger than 1 whose only divisors are 1 and itself. In plain words, it is the textbook sentence with a bouncer at the door.

Mathematicians took the second. Nothing in the numbers forced the choice, and I would rather you hear that from me than discover it later and feel tricked. The first repair is logically fine. It is just clumsy, and a definition is allowed to be chosen for the reason that it makes the theorems short.

Choices like this get revisited. In Giuseppe Peano's original axioms for the counting numbers, the count began at 1. He later revised them so that it began at 0.

## The empty bag

There is a better answer to the student's question, and it comes from asking what the product of no numbers at all should be. Guess before you read the next line.

The answer is 1.

Here is why. Build a product by keeping a running total and multiplying in one piece at a time. After multiplying in a single piece, say 7, the total should be 7. But the total is the starting value times 7, and the only starting value that gives 7 is 1. An empty bag multiplies in nothing, so the total stays at its starting value, which is 1. It is the same reason $2^0 = 1$: zero copies of 2 multiplied together leave you where you began.

Now go back to the number 1 and ask for its bag. Any nonempty bag of primes, as we now define them, holds pieces that are all at least 2, so it multiplies to at least 2. The only bag that multiplies to 1 is the empty one. So the theorem already covers the number 1, with a perfectly good and unique bag that holds nothing. The student asked whether 1 belongs inside the bags, and the bags have an answer ready: 1 is what you get when you put in nothing.

## Older doors

Ancient philosophers had a different reason for keeping 1 apart. The Pythagoreans considered numbers to be plural, so a single unit did not count as a number at all. It was the place numbers came from. The Neopythagorean Nicomachus of Gerasa wrote the same, that one is the source of number and not a number itself.

Their reason was about what counting is, and bags did not enter into it. Whether they would have accepted the bag argument I cannot say.

## A bag that is not unique

The fingerprint property is a gift that the whole numbers happen to carry. Other number systems do not have it.

Build numbers out of whole numbers together with $\sqrt{-5}$, a number whose square is $-5$. In that system $6 = 2 \times 3$, and also $6 = (1 + \sqrt{-5})(1 - \sqrt{-5})$, since the second product is $1 - (-5) = 6$. None of the four pieces can be broken down any further. I checked this, and the check fits in a paragraph that I am leaving out.

Two different bags, and no stray 1 to blame. What would you want to change in a system like that to get the bag back?

Text licensed under CC BY-SA 4.0.
