+++
title = "Why 1 Is Not Prime"
date = 2026-11-02T12:15:34+00:00
draft = false
slug = "why-one-is-not-prime"
description = "The sentence that defines a prime lets 1 in. Twelve shows what the opposite choice would cost, and why 1 is kept out by convention."
summary = "The textbook sentence that defines a prime number admits 1, yet mathematicians exclude it by convention. Factorising 12 shows what would happen if they did not, and the empty product shows where 1 really belongs."
categories = ["Number theory"]
tags = ["primes", "factorisation", "definitions", "foundations"]
concepts = ["prime number", "multiplicative identity", "empty product", "convention"]
+++

You open your maths book at the definition of a prime number: a number whose only divisors are 1 and itself. Then you test the number 1. Its only divisor is 1, which is also itself, so by the sentence you have just read, 1 qualifies.

It does not. Mathematicians treat 1 as not prime by convention, which means a choice was made and not a fact discovered. I will not pretend to tell you why the choice went the way it did. What I can do is show you what the opposite choice would cost, using ten minutes and the number 12.

## What 1 does

First, a small guess. What is $1^{50}$, the number 1 multiplied by itself fifty times?

It is 1. Multiplying by 1 leaves any number exactly as it was, so a chain of fifty of them changes nothing fifty times over. This is why 1 is called the multiplicative identity, and it holds for whole numbers and for the stranger kinds of number alike. Every power of 1, and its square root, is simply 1 again.

Keep that property in your pocket. It is about to cause trouble.

## Twelve, broken up

Take 12 and write it as a product of smaller numbers, then keep going until no piece can be split further. One route: $12 = 3 \times 4$, and $4 = 2 \times 2$, which leaves $3 \times 2 \times 2$. Another route: $12 = 2 \times 6$, and $6 = 2 \times 3$, which leaves $2 \times 2 \times 3$.

The routes differ and the leftovers do not. Two 2s and one 3, in either order. The pieces that cannot be split any further are the primes, and so far we have met 2 and 3.

Try a bigger number. $60 = 6 \times 10 = 2 \times 3 \times 2 \times 5$, and also $60 = 4 \times 15 = 2 \times 2 \times 3 \times 5$. Different routes, the same pieces: two 2s, a 3 and a 5. I have not proved that this happens for every number, and I will not claim it. In the two examples I tried, it does.

Now let the textbook sentence win and allow 1 to count as a prime. Before you read on, commit to a guess: how many different lists of primes can you now find whose product is 12?

There is no limit. The list $2 \times 2 \times 3$ still works. So does $1 \times 2 \times 2 \times 3$, and every piece in it is prime under the new rule. So does $1 \times 1 \times 2 \times 2 \times 3$, and the one with ten 1s, and the one with a million.

Multiplying by 1 changes nothing, so a 1 can be slipped into a product anywhere, any number of times, and the number stays 12. A simple question goes sour: how many prime pieces does 12 have? With 1 allowed, any count from three upwards is as correct as any other.

## A choice, not a law

Nothing in the arithmetic forbids calling 1 prime. The sentence in the textbook allows it, and the calculation above is perfectly valid. The exclusion is a convention, a decision people took, and 12 shows the price of the other decision: the same list of pieces, every time, would be lost, and with it the tidy answer to 'what is 12 made of?'

I find that more interesting than a law would be. A law gives you nothing to argue with. A choice has a cost you can compute, and then you can decide for yourself if you would have paid it.

## Multiplying nothing

There is a better home for 1, and it comes from asking what you get when you multiply no numbers at all. Guess first.

The answer is 1. Here is the reasoning. Build a product with a running total, multiplying in one piece at a time. After one piece, say 7, the total should be 7. But the total is the starting value times 7, and the only starting value that gives 7 is 1. An empty list of pieces multiplies nothing in, so the total stays at its starting value. This is called the empty product, and it equals 1.

The same reasoning explains why $2^0 = 1$: zero copies of 2 multiplied together leave you where you began.

Now ask what the prime pieces of 1 are. None. The factorisation of 1 is empty: nothing multiplied together. Under the convention, 1 needs no primes at all.

## Older doors

The Pythagoreans had a different reason for keeping 1 apart. They considered numbers to be plural, so a single unit did not count as a number. It was the place numbers came from. In their philosophy, odd numbers were male and even numbers female, and 1 was neutral because adding it turns even numbers into odd ones and odd ones into even: $4 + 1 = 5$ and $5 + 1 = 6$.

Test that against a different number. $4 + 3 = 7$, and $8 + 5 = 13$. Adding other odd numbers flips the camp too, so flipping alone does not seem to set 1 apart. I cannot say whether it was their only reason, and I would not want to put words in their mouths. Nicomachus of Gerasa, whose treatise reached Latin readers through Boethius, held that one is not a number but the source of number.

Where the list of natural numbers starts has been moved around as well. Giuseppe Peano's original axioms began the sequence at 1. He later revised them to begin at 0. In John von Neumann's construction, each number is the set of all the numbers before it, and 1 becomes the set containing only 0, written $1 = \{0\}$.

## One stroke

The mark you draw for 1 is a vertical stroke, and a single stroke is all a tally needs. The system that writes every natural number as a run of the same mark is called unary, and it is the simplest way to write them, although it is rarely used for counting because long runs are hard to read.

The shape itself has a path. The upright stroke for 1 can be traced back to the Brahmic script of ancient India, in the edicts of Ashoka around 250 BCE, and the shapes of that numeral system reached Europe through the Maghreb and Al-Andalus in the Middle Ages.

Every natural number is built by adding 1 to the one before it, and that includes 1 itself: $0 + 1 = 1$. The step that builds the whole list is also a number on the list. Which came first, the number 1 or the act of adding one?

Text licensed under CC BY-SA 4.0.
