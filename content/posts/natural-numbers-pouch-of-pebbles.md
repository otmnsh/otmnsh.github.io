+++
title = "Rebuilding the Natural Numbers From a Pouch of Pebbles"
date = 2026-11-03T05:12:32+00:00
draft = false
slug = "natural-numbers-pouch-of-pebbles"
description = "A pouch of pebbles and one move, 'next', rebuild size, order, addition and multiplication, and show exactly where the method runs out."
summary = "Starting from pairing and a single repeated move, we rebuild the natural numbers and the arithmetic that grows from them. Then we take Peano's rules apart one by one to see what each prevents, and ask what a number is made of."
categories = ["Number theory"]
tags = ["foundations", "definitions", "counting"]
concepts = ["natural number", "successor", "one-to-one correspondence", "peano axioms", "induction"]
+++

You stand at a pen gate with a leather pouch of pebbles and no words for any amount, because numbers have not been invented yet. Each morning the flock goes out onto the hill, and each evening you must know whether every animal came home.

## The gate

Here is your method. As each sheep walks out in the morning, you drop one pebble into the pouch. As each sheep walks back in at night, you take one pebble out.

The evening ends. The last sheep you can see is inside the pen, and the pouch is not empty. Decide before you read on: what do you know?

Some sheep are still on the hill, exactly as many as there are pebbles left in your hand. You cannot say how many, and you do not need to, because the leftover pile does the job a number would do. Had the pouch run dry while sheep were still filing through the gate, you would know the opposite: strangers had joined the flock.

Nothing was counted. Each sheep was matched with one pebble, and the matching told you everything. Two collections that can be paired off completely, one object to one object with nothing left on either side, have the same size, and you can know that without knowing what the size is. Mathematicians call such a pairing a one-to-one correspondence. It also gives you a comparison for free: the collection that runs out first is the smaller one, and the one with leftovers is the larger.

{{< figure src="/img/natural-numbers-pouch-of-pebbles-1.png" alt="A pen gate with five sheep walking through it, drawn in a row. Under each sheep a pebble is drawn, and a thin line joins each sheep to its own pebble. A sixth pebble sits alone at the end of the row with no line attached to it and no sheep above it." >}}

## A row of piles

Suppose you want to carry an answer around without carrying the sheep. On a flat stone you lay out piles. First an empty spot, with no pebbles. Then a pile made by adding a single pebble to the empty spot. Then a pile made by adding a single pebble to that one, and so on along the stone for as long as you have patience.

Every pile after the first is built by one move: take the pile before it and add a pebble. The result is called the successor of the pile before it. I will call the move 'next'.

These piles are the natural numbers. The empty spot is named 0, the single pebble 1, and if $n$ stands for any pile on the stone, the pile right after it is named $n + 1$. Authors disagree about whether the empty spot counts as a natural number. The international standard for mathematical notation includes it, and so does this post.

Notice what the stone gives you. A pile tells you how many, and its spot on the stone tells you which place. A size and a position are the two jobs a number does, and here they are the same pebbles seen from two sides.

{{< figure src="/img/natural-numbers-pouch-of-pebbles-2.png" alt="A flat stone seen from above carrying a row of pebble piles from left to right. The leftmost spot is empty and labelled 0. The next spot holds one pebble and is labelled 1, the next holds two pebbles and is labelled 2, and so on up to a pile of five. Between each pair of neighbouring piles a curved arrow points to the right and is labelled next." >}}

## Pouring

Pouring one pile into another gives addition. You pour the second pile into the first one pebble at a time, and each pebble is one 'next' applied to the first pile. So $3 + 2$ means: start at 3, step to the next pile, step again, and arrive at 5. Addition is 'next' repeated as many times as the second pile has pebbles.

Multiplication is the same trick one level up. To compute $3 \times 2$, start from the empty spot and pour in a pile of 3 twice, which leaves you at 6. As a rule: multiplying by 0 gives 0, and multiplying by the number after $b$ means taking the result for $b$ and adding one more copy of the pile. Multiplication is addition repeated, and addition is 'next' repeated.

A guess. Pour a pile of 3 into a pile of 2, or pour a pile of 2 into a pile of 3. Does the order matter?

You said no, and so would anyone who has held pebbles. Now look at the rule we actually wrote down. It treats the two piles differently, adding the second to the first one pebble at a time, and nothing in it promises that $3 + 2$ and $2 + 3$ agree. They do, for every pair of piles. That the order never matters is one of several properties the operations turn out to have, and it follows from the definitions instead of being part of them. I will not prove it here.

Hermann Grassmann suggested in the 1860s that the natural numbers could be defined by exactly this kind of recursion, and concluded that they were not really natural at all, only a consequence of definitions. Leopold Kronecker, in the same century, summed up his own belief like this: 'God made the integers, all else is the work of man.'

## Five rules, taken apart

Giuseppe Peano's name is on a short list of rules, the Peano axioms, that any natural numbers must obey, though the version usually given is not quite the one he published. In 1881 Charles Sanders Peirce wrote down the first axioms for the arithmetic of natural numbers. Richard Dedekind proposed another set in 1888, and in 1889 Peano published a simplified version of Dedekind's. In pebble language the rules read:

- The empty spot is a pile.
- Every pile has a next pile, and that is a pile too.
- The empty spot is not the next pile of anything.
- If two piles have the same next pile, they are the same pile.
- If a claim is true of the empty spot, and its truth for any pile forces its truth for the next pile, then the claim is true of every pile.

The last rule is called induction. Take the rules away one at a time and watch the stone misbehave. Without the second, the row could simply end. Without the third, stepping 'next' from some pile could land you back on the empty spot, and the stone would curl into a loop. Without the fourth, two different piles could flow into the same next pile, and the row would merge into itself.

Without the fifth, nothing stops piles from sitting on the stone that you could never reach by stepping from the empty spot. Here is the rule at work against that. Take the claim 'this pile can be reached by stepping from the empty spot'. It is true of the empty spot, and if it is true of a pile then it is true of the next one. By the last rule it is true of every pile. In plain words: if you can stand on the first rung of a ladder, and you can always climb from one rung to the one above, you can reach any rung you like.

## What the pouch cannot do

Another guess. Take 5 pebbles out of a pile of 3. What is left?

Nothing on the stone matches that situation. The pouch runs empty and two removals are still owed, and the answer is a negative number, which is not a pile. Share 7 pebbles equally between two people and you hit the same wall from the other side: 3 each, and one pebble nobody can fairly keep. Subtraction and division only sometimes give an answer inside the row.

Each refusal turned out to be an invitation. Insist that the difference of any two natural numbers is a number, and the integers appear, with their negatives. Insist that the quotient of any two integers is a number, and the rational numbers appear, with their fractions. The natural numbers are the part of the story that never needed an insistence.

## Where the pebbles fail

The pairing idea looks so solid that Gottlob Frege tried to turn it straight into a definition: a natural number is the class of all sets that can be matched one to one with a particular set. That plan led to paradoxes, Russell's paradox among them. The repaired version defines a natural number as one particular set, and says any set that can be matched with it has that many elements.

A variety of particular sets have been proposed, and the standard one is John von Neumann's. Zero is the empty set. The next number is the old set with itself added as a new member, so $1 = \{0\}$, $2 = \{0, 1\}$, $3 = \{0, 1, 2\}$, and every number $n$ is a set with $n$ elements, each one a smaller number. Look at where it starts: the empty set, which is the empty spot on your stone.

## The line, not the pebbles

Nothing about pebbles was special. The letters of an alphabet would serve as positions in a sequence just as well. The philosopher Paul Benacerraf put the consequence bluntly: to be the number 3 is no more and no less than to come after 2 and 1, and perhaps 0, and before 4 and 5, and any object can play that role. The pebbles in the third pile are not three. The place is.

If three is a place in a line and not a thing, what is the line made of?

Text licensed under CC BY-SA 4.0.
