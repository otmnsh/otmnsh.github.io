+++
title = "The Square Root That Had to Choose"
date = 2026-11-07T18:59:40+00:00
draft = false
slug = "square-root-had-to-choose"
description = "A square root that returns two answers is not a function, and fixing that one flaw produces the whole formal definition, empty function included."
summary = "Asking a machine for the square root of 4 exposes the rule that makes a function a function: every allowed input gets exactly one output. Taking that rule apart shows what each half protects, what was forced, what was chosen, and why a function with nothing in it exists."
categories = ["Foundations"]
tags = ["definitions", "foundations", "sets"]
concepts = ["function", "domain", "codomain", "empty function"]
+++

Build a machine with a slot on the left and a slot on the right. You post a number in, and the machine must post out a number which, multiplied by itself, gives back the number you posted. Feed it 4.

Decide what comes out before you read on.

Most people say 2. A few say $-2$, and they are right as well, because $(-2) \times (-2) = 4$ just as surely as $2 \times 2 = 4$. The machine has two honest answers and only one slot. A machine that picks between them at whim cannot be relied on, since the same input might give a different output tomorrow. Something has to give, and the interesting part is how much.

## A circle that answers too much

Here is a second machine with the same flaw, dressed differently. You post a number $x$, and it must post a number $y$ satisfying $x \times x + y \times y = 1$. Write each successful use as a pair of numbers $(x, y)$, the first being what went in and the second what came out. Plot every pair that works and you get a circle of radius 1. A vertical line drawn at your chosen $x$ asks the circle how many times it is crossed.

Post $x = 0.6$. The condition becomes $0.36 + y \times y = 1$, so $y \times y = 0.64$, and $y$ is $0.8$ or $-0.8$. Two answers again.

Now a prediction. How many answers does the machine have if you post 1, and how many if you post 2?

For 1, the condition leaves $y \times y = 0$, and only 0 multiplied by itself gives 0, so there is exactly one answer. For 2, it leaves $y \times y = -3$. A positive number multiplied by itself is positive, a negative number multiplied by itself is positive too (the two minus signs cancel), and 0 gives 0. Nothing will do. No answer.

So this machine gives two answers, one, or none, depending on where you stand. The vertical line crosses the circle twice at 0.6, grazes it at 1, and misses it altogether at 2.

## What the word was always asking for

The idea of a function grew up alongside calculus, at the end of the 17th century. The model was a varying quantity that depends on another: the position of a planet depends on the time. Name a moment and there is a position, and just one. For about two centuries the functions people actually considered were smooth ones, well behaved enough to have a slope at every point. Euler wrote $f(x)$ in 1734, the first use of that notation.

The demand had two halves all along, though it was seldom stated that way. Every input you are allowed to post must produce an answer: at least one. And it must never produce two: at most one. The machine fed with 4 broke the 'at most' half. The circle machine broke it at 0.6 and broke the 'at least' half at 2.

The founders of calculus put both halves into one word, 'assignment': each input is assigned an output. That was enough to work with, and it could not be turned into mathematics, because nobody had a definition of 'assignment' to stand on. The repair came at the end of the 19th century, and it came from the theory of sets.

Record every successful use of a machine as a pair $(x, y)$. The machine is then nothing more than its collection of pairs, and the two halves become two checks on that collection. Let $X$ be the set of inputs the machine is allowed to take, called its domain, and let $Y$ be the set the outputs are promised to come from, called its codomain. (Some books use 'range' for the codomain and others for the outputs actually reached, so I avoid the word.) A function from $X$ to $Y$ is a collection $R$ of pairs $(x, y)$, with $x$ from $X$ and $y$ from $Y$, such that:

1. for every $x$ in $X$ there is at least one $y$ with $(x, y)$ in $R$;
2. if $(x, y)$ and $(x, y')$ are both in $R$, then $y = y'$, where $y'$ is simply a second output.

In plain words: every allowed input gets an answer, and never two different ones. The word 'function' is the name for passing both checks.

## Taking out one check at a time

Remove check 2 and you have the machine fed with 4, and the circle machine. The damage goes beyond inconvenience, because the notation breaks. Writing $f(4)$ names a single number. With two answers the symbol would point at two things at once.

Remove check 1 and you get what mathematicians call a partial function, a machine that may refuse some inputs. This is milder, and in analysis the word 'function' often means exactly this, because for many machines the list of accepted inputs is hard to work out. Write $\sqrt{y}$ for the positive answer to 'what multiplied by itself gives $y$', so $\sqrt{4} = 2$ and $\sqrt{0.64} = 0.8$. The machine $\sqrt{1 - x \times x}$ works only when $1 - x \times x$ is at least 0, which happens exactly when $x$ lies between $-1$ and $1$, ends included. Post 2 and it refuses, since $1 - 4 = -3$.

That cleans up the circle. The positive answers, $y = \sqrt{1 - x \times x}$, trace the top half of the circle, and the negative answers, $y = -\sqrt{1 - x \times x}$, trace the bottom half. Check at $x = 0.6$: $1 - 0.36 = 0.64$, and the root is $0.8$. Each half is a function with inputs from $-1$ to $1$. Two honest functions stand where one dishonest machine stood.

Sometimes finding the accepted inputs is the entire difficulty. Take one divided by the value of a famous function called the Riemann zeta function. That reciprocal is defined exactly where the zeta function is not zero, so asking for its accepted inputs is asking where zeta is zero. Settling that is, more or less, the same task as proving or disproving the Riemann hypothesis, a major open problem. A rule that demands an answer for every input can be a rule you cannot afford to check.

## Forced and chosen

Back to the first machine. To keep check 2 it must pick one answer. Is any pick forced?

Take the machine that squares, posting $x \times x$ for input $x$. It posts 4 for both 2 and $-2$. A machine undoing it, given 4, would have to post both. That part is forced: two different inputs with the same output block every undoer, and no convention can repair it.

What can be done is shrink the squarer's allowed inputs to zero and above. Then no two inputs share an output. Suppose $a$ and $b$ are both at least 0 and $a \times a = b \times b$. Then $(a - b) \times (a + b) = a \times a - b \times b = 0$, so $a = b$ or $a + b = 0$. With both at least 0, the second case forces $a = b = 0$. Either way $a = b$. Every number from 0 upwards is reached by the shrunken squarer, which I am taking as known, and so it can be undone. The undoer is the square root.

That the undoer posts 2 rather than $-2$ is a choice. Shrink to zero and below instead, repeat the argument with the signs flipped, and the undoer posts $-2$. Nothing in the argument prefers the positive side; people did. Cosine gets the same treatment: restricted to inputs from 0 to $\pi$ (about 3.14) it can be undone, and the undoer is called arccosine. The other inverse trigonometric functions are defined in the same way.

Shrinking is not always available, and here I give the idea without a proof. Among the complex numbers, which include a number $i$ whose square is $-1$, the square root can be extended step by step from the positive numbers outwards. Take one route and $\sqrt{-1}$ comes out as $i$. Take the other and it comes out as $-i$. Two reasonable routes, two answers. One way out is to cut the plane along a curve and let the function jump across it, which keeps it a function. The other is to keep both values and call it multi-valued, which means giving up check 2 on purpose. Both are used. Check 2 is a price paid for convenience, and the bill sometimes arrives.

I have left out functions with several inputs, and the names for the ways a function can fail to be reversible. They need more room.

## The machine with no slot

The checks were written for collections of pairs, so they should cope with a strange case: a domain with nothing in it. Write $\varnothing$ for the set with nothing in it. How many functions go from $\varnothing$ to a set $Y$?

The collection must hold pairs whose first entry comes from $\varnothing$. There are no such pairs, so the only collection available is the empty one. Do the checks hold? Check 1 asks something of every input, and with no inputs there is nothing to fail. Check 2 asks about pairs that share an input, and there are no pairs. Both pass. So there is exactly one function from nothing to $Y$, whatever $Y$ is, called the empty function. Mathematicians keep it because without it many statements about sets would need a special exception for the empty set.

Now take $Y = \{1, 2\}$, the set holding 1 and 2, and $Y' = \{a\}$. Each has its own empty function, and both have exactly the same collection of pairs, namely none. Are they the same function?

The usual definition says no, because it counts a function as three things together: the domain, the codomain and the collection of pairs. The codomains differ, so the functions differ. A definition that kept only the pairs would call them equal. Neither answer is forced; the triple is a choice of definition, and this is one place where you can see its effect.

One case is left that the same two checks settle just as quickly, running the other way: a single number to feed in, and a codomain with nothing in it. What do the checks say?

Text licensed under CC BY-SA 4.0.
