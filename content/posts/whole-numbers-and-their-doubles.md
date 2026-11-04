+++
title = "The Whole Numbers and Their Doubles"
date = 2026-11-04T04:47:53+00:00
draft = false
slug = "whole-numbers-and-their-doubles"
description = "A row of numbers and a row of their doubles pair off perfectly, yet one row sits inside the other. Sets split the word 'more' in two."
summary = "Writing the whole numbers above their doubles produces two honest answers to the question of which row is bigger. Sets and pairing show where the word 'more' splits in two, and where the usual rules of set theory run out."
categories = ["Foundations"]
tags = ["foundations", "infinity", "sets"]
concepts = ["set", "one-to-one correspondence", "cardinality", "power set", "continuum hypothesis"]
+++

Write the whole numbers in a row: 0, 1, 2, 3, and so on without end. Under each one write its double, so that 0 sits over 0, 1 over 2, 2 over 4, 3 over 6, and the second row goes on for ever as well.

Every number in the top row now has a partner underneath, and every even number appears underneath exactly once. Before you read on, commit to an answer: which row holds more numbers?

## Two answers

One answer says the top row. The bottom row holds only even numbers, so every odd number lives in the top row and nowhere below it. The bottom row is a part of the top row with pieces missing, and a part is smaller than its whole.

The other answer says neither. Draw a line from each number to its double and nothing is left over on either side: no number in the top row without a partner, no number in the bottom row without one. Two collections that pair off completely are the same size.

Both answers stand on something solid. The first stands on containment, on whether one collection sits inside another. The second stands on pairing. In a finite world the two tests agree and you never have to choose. Take the numbers 0 to 9 and the even ones among them, 0, 2, 4, 6 and 8. The evens sit inside the ten numbers, and when you try to pair them off with all ten, five numbers are left without a partner. Containment says smaller, pairing says smaller, and nobody argues.

Infinity is where the word 'more' splits in two.

## What a set is

To argue properly we need the thing being argued about. A set is a collection of different things, called its elements or members, and only membership matters. Repeating an element or rearranging the elements changes nothing, so the sets written between curly brackets as $\{1, 2, 2, 3\}$ and $\{3, 1, 2\}$ are the same set. Two sets are equal exactly when they have the same elements.

Mathematics does not define a set any further. It lists the rules that sets must obey, much as Euclid never gave a meaningful definition of a point and described how points behave instead. The word is a starting point, and everything else is built on it.

Pairing off completely, one member to one member, with nothing left on either side, is called a one-to-one correspondence. A set is finite when its members can be paired with the first $n$ natural numbers for some $n$, which is exactly what counting does, and then $n$ is its number of elements. I count 0 among the natural numbers here, as many authors do and many do not. A set for which no such $n$ exists is infinite. And two sets have the same cardinality, which is the word for 'size' that does not need counting, when a one-to-one correspondence exists between them.

That last sentence is a definition, which makes it a choice. Everything that follows from it is forced.

## A part as large as the whole

Apply the definition to the two rows. The rule 'double it', written $n \mapsto 2n$, sends 0 to 0, 1 to 2, 2 to 4, 3 to 6, and it hits every even number exactly once. So the natural numbers and the even natural numbers have the same cardinality, although the evens are a proper subset of the natural numbers: a subset that leaves something out.

This is no accident of the evens. A set is infinite exactly when it has the same cardinality as one of its proper subsets. Try it on a finite set and it fails: no part of the ten numbers 0 to 9 that leaves something out can be paired off with all ten. So on a finite set the two tests cannot disagree, and on an infinite set they always do.

Each answer was right about its own question. The first answer asked how much room a collection takes inside another. The second asked how many members it has, in the only sense of 'how many' that survives when counting runs out.

## A short line and an endless one

Another guess. Take a line segment one centimetre long and compare it with the whole endless line. Which has more points?

They have the same number. Any line segment has the same cardinality as the whole line, a result that came out of Cantor's study of infinite sets. I am not going to build that pairing here, because it needs a function I have not introduced, and I would rather say so than wave my hands.

Before the end of the nineteenth century a line was not treated as a set of points at all. It was treated as a place where a point may sit. Seeing a line as a collection of points is the move that makes the question above even askable.

## More than one infinity

Are all infinite sets the same size? No. The natural numbers are infinite, and the real numbers, the points of the number line, form an infinite set that is strictly larger.

Here is a way to feel the ladder. The power set of a set is the set of all its subsets, counting the empty set and the set itself. Take $\{1, 2, 3\}$ and write down its subsets. One more guess, and make it before you count: how many are there?

Eight: the empty set, the three subsets with a single element, the three with two, and the whole set. A set with $n$ elements has $2^n$ subsets, where $2^n$ means 2 multiplied by itself $n$ times, and $2^n$ is bigger than $n$ every time: 1 against 0, 2 against 1, 4 against 2, 8 against 3. Cantor's diagonal argument shows that the same thing holds for every set, finite or infinite: its power set always has the greater cardinality. I will not prove it here. What it implies is that no cardinality is the greatest, because the power set of anything is bigger. The real numbers turn out to have the same cardinality as the power set of the natural numbers, which is one way to see why they are more.

## A collection that cannot exist

Cantor began the mathematical study of infinite sets, and it produced statements that were hard to believe. Assuming that a set of all sets exists led to a contradiction, known as Russell's paradox, and that opened what is called the foundational crisis of mathematics. The resolution adopted generally is Zermelo–Fraenkel set theory, though much of mathematics does not need its full power.

One consequence is easy to see in the notation. Not every description defines a set. Some conditions cannot be used to collect elements, because no set has exactly the elements the condition picks out. One repair is to pick elements from a set you already have.

Sets spread through mathematics anyway. Euclid's theorem on the primes is often stated as 'the set of the prime numbers is infinite', and since the first half of the twentieth century every mathematical object is ultimately defined in terms of sets. David Hilbert said of it: 'No one will drive us from the paradise that Cantor created for us.'

## What the rules leave open

Cantor conjectured in 1878 that there is no set whose size lies strictly between the natural numbers and the real numbers. This is the continuum hypothesis. In 1963 Paul Cohen proved that it is independent of the standard axioms of set theory, which means the rules can neither prove it nor refute it. If the usual set theory is free of contradiction, then so is the same theory with the hypothesis added, and so is the same theory with its opposite added.

That is a statement that is neither forced nor forbidden, and the choice between its two sides is left to us. Is there a size between the whole numbers and the points on a line, and if the usual rules cannot tell us, what would count as a reason to choose?

Text licensed under CC BY-SA 4.0.
