+++
title = "A Shepherd Who Cannot Count"
date = 2026-11-02T12:58:06+00:00
draft = false
slug = "shepherd-who-cannot-count"
description = "A shepherd with a bag of pebbles can tell whether a sheep is missing without any number words, and that is nearly all a natural number is."
summary = "A shepherd with no number words keeps track of her flock with a bag of pebbles, and her trick turns out to be the foundation of what a natural number is. We follow it from pebbles to the sets that mathematicians use to build every number from nothing."
categories = ["Number theory"]
tags = ["definitions", "foundations", "counting"]
concepts = ["natural number", "one-to-one correspondence", "cardinality", "successor", "von Neumann construction"]
+++

A shepherd has a flock and no number words. Nobody ever taught her "forty", yet every evening she has to know whether all her sheep came back through the gap in the wall.

She has a leather bag and a heap of pebbles. In the morning, as each sheep passes through the gap, she drops one pebble into the bag. In the evening, as each sheep comes back, she takes one pebble out of the bag and returns it to the heap. If the bag is empty when the last sheep is in, nobody is lost. If two pebbles are still rattling at the bottom, two sheep are out on the hill.

{{< figure src="/img/shepherd-who-cannot-count-1.png" alt="A row of sheep drawn above a row of pebbles, each sheep joined to the pebble below it by a short vertical line. The last two pebbles at the right end of the pebble row have no line going up to any sheep." >}}

That is the whole procedure, and it contains no number. She cannot tell you how many sheep are missing, only that the leftover pebbles match them one for one. The bag has become a stand-in for the flock.

## A quarrel over two flocks

Her neighbour has a flock too, and the two of them argue about whose is bigger. Neither can count. Before you read the next paragraph, decide what you would do. You may use sheep, pebbles, a wall with gaps, and nothing else.

The answer is the shepherd's trick again, with the pebbles removed. Open two gaps side by side, and send one sheep from each flock through at the same moment, then another pair, then another. Whichever flock still has animals waiting when the other has run dry is the bigger flock. If both run dry together, the flocks are the same size, and nobody has said a number.

The matching has a name, and I will use it once: a one-to-one correspondence. Every member of one collection is paired with exactly one member of the other, and nothing is left over on either side. Everything that follows leans on that single phrase.

## What the pairings share

Take the bag with its forty pebbles. Plenty of other collections can be paired off with it exactly: the sheep, but also the days of a forty-day fast, or forty stones laid along a road. These collections have nothing in common as objects. They share only the fact that each can be matched against the bag without leftovers.

So here is a way to say what a number is. It is the thing shared by every collection that pairs off with a given bag. "Forty" is a name we gave to that shared thing, and the shepherd got along without the name. Georg Cantor was the mathematician who pushed this to the front: sameness of size, tested by pairing, comes before counting and before numbers.

This inverts the order they taught you in school, where you counted first and compared afterwards. The shepherd compares first, and numbers fall out as the things comparison keeps agreeing about.

## Counting, caught in the act

Counting is the same trick with a fixed, memorised bag. The bag is the sequence of words "one, two, three" and so on. You walk along a row of coins, pairing each coin with the next word, and the last word you reach is the answer.

Here is a second question to decide before reading on. You have seven coins on the table. You count them from left to right and end on "seven". Now you shuffle them, and count again in whatever order your finger happens to wander. Will you end on "seven" again?

Of course you will. Yet that sentence is a theorem. The order of the coins is arbitrary, and nothing in the procedure obviously stops one order from finishing on "seven" and another on "six". If that happened, the words one to seven and the words one to six could be paired off completely through the coins in between, and the shepherd's bag would have no leftover pebble. A bag of seven pebbles can never be matched exactly with six sheep, and that fact is what makes counting trustworthy. I am giving you the idea here, not a proof. The careful version goes by induction, and it is less trivial than it feels.

{{< figure src="/img/shepherd-who-cannot-count-2.png" alt="The same seven coins drawn twice. In the left drawing they sit in a line labelled 1 to 7 from left to right. In the right drawing they are scattered and labelled 1 to 7 in a different order, with arrows showing that both drawings end at the label 7." >}}

## Frege's shortcut, and the paradox behind it

If a number is what pairable collections share, why not define it as the collection of all those collections? Three would be the class of all trios: every three-apple bowl, every three-person jury, every trio of stones. Gottlob Frege proposed exactly this.

It broke. Bertrand Russell asked about the class of all classes that do not contain themselves, and whether that class contains itself. Either answer contradicts the other. Talking about "all collections" without restraint is too generous, and Frege's definition fell with it.

The repair is modest. Instead of taking all trios, pick one particular collection to stand for three, and say that any collection pairable with it has three members. The shepherd's bag, in other words. The question becomes what to make the bags of. We are building numbers, so we have nothing yet to put inside them.

## Building the bags from nothing

Begin with the emptiest bag possible, the one with no pebble in it. Write it $\{\ \}$ and call it $0$.

For a bag with one pebble, we need something to be the pebble, and the only thing we own is the empty bag. So $1$ is the bag containing it: $\{0\}$. For the next bag, we put in both things we have made so far:

$$2 = \{0, 1\}$$

and then

$$3 = \{0, 1, 2\} = \bigl\{\{\ \},\ \{\{\ \}\},\ \{\{\ \},\{\{\ \}\}\}\bigr\}.$$

Check the last one slowly. It has three things in it, and each of them is a bag we built earlier.

{{< figure src="/img/shepherd-who-cannot-count-3.png" alt="Five nested rounded boxes drawn from left to right. The first box, labelled 0, is empty. The box labelled 1 contains one copy of box 0. The box labelled 2 contains copies of boxes 0 and 1. The box labelled 3 contains copies of boxes 0, 1 and 2. The box labelled 4 is drawn with a question mark in place of its contents." >}}

Now the third prediction. What is $4$? Most people say $\{0, 1, 2, 3\}$ without hesitating, and they are right. The rule behind it is that the bag after $a$ is $a$ together with one extra item, which is $a$ itself. In symbols, that is $a \cup \{a\}$, where the cup means "everything in $a$, plus the following". John von Neumann made this choice, and it has a pleasant side effect. The number $n$ is a bag with exactly $n$ things in it, and those things are all the smaller numbers. Smaller means sitting inside: $2$ is a part of $3$, because $\{0,1\}$ is inside $\{0,1,2\}$.

Notice what happened to "the number of sheep". Pair the sheep with the bag $\{0,1,2\}$ and you have said there are three of them, with a bag that every flock in the world can be measured against.

## What I left out

Von Neumann's bags are one choice among several. Ernst Zermelo's version makes the bag after $a$ simply $\{a\}$, so $2$ is $\{\{\ \}\}$ with one thing inside it, and the successor rule still works. Nobody can say which is the true three. What every version agrees on is the role: a number is whatever sits in the right place in the chain, with a fixed first step and a fixed next step.

Whether the chain starts at $0$ or $1$ is a convention, and authors have gone both ways. I began with $0$ because the empty bag is the first one a shepherd owns, on the day she has no flock to track.

## The bag with no bottom

Everything above used a quiet assumption: a bag runs out. But pairing never asked for that. Write down the numbers $1, 2, 3, \dots$ with no end, and beside them the even numbers $2, 4, 6, \dots$ Pair each number $n$ with $2n$.

{{< figure src="/img/shepherd-who-cannot-count-4.png" alt="Two horizontal rows of dots continuing to the right with ellipses. The top row is labelled 1, 2, 3, 4, 5 and so on. The bottom row is labelled 2, 4, 6, 8, 10 and so on. Straight arrows join the number n in the top row to the number 2n in the bottom row, and no dot in either row is left without an arrow." >}}

Every number gets a partner, and every even number is somebody's partner. No pebble is left over on either side. By the shepherd's rule, the two collections are the same size, even though the evens are only half of the numbers, or so we would have said an hour ago. A bag that can be matched exactly against a part of itself is a bag her procedure was never built for, and nobody yet knows what the word "size" is allowed to promise about it.
Text licensed under CC BY-SA 4.0.
