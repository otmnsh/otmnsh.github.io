+++
title = "The Largest Number in a List That Never Ends"
date = 2026-11-16T18:41:59+00:00
draft = false
slug = "largest-number-endless-list"
description = "A pencil-and-paper recipe for the biggest number works on every finite list and fails in a revealing way on one that never ends."
summary = "A recipe for finding the largest number on a sheet of paper is taken apart piece by piece, and each piece is tested to see what breaks without it. Then the recipe is handed a sheet that never ends, which shows what a procedure must promise before it earns the name algorithm."
categories = ["Foundations"]
tags = ["algorithms", "computation", "proof", "history"]
concepts = ["algorithm", "well-defined", "heuristic", "algorism"]
+++

A sheet of paper carries four numbers: 7, 3, 9 and 4. Beside it lies a scrap the size of a stamp, with room for exactly one number at a time, and a pencil with a good eraser.

Your task is to finish with the largest of the four written on the scrap. The rule is that you may look at only one number from the sheet at a time, and you may compare it with whatever the scrap holds.

## The scrap of paper

Here is a recipe. Copy the first number from the sheet onto the scrap. Then take the remaining numbers in order. Each time the number in front of you is strictly bigger than the one on the scrap, rub the scrap out and write the new number. When the sheet runs out, the scrap holds your answer.

Before reading on, predict two things for the sheet 7, 3, 9, 4. How many times will you rub the scrap out, and what will be written on it at the end?

Run it. The scrap starts as 7. The number 3 is not bigger, so nothing happens. The number 9 is bigger, so out goes the 7 and in goes the 9. The number 4 is not bigger. One erasure, and the scrap says 9. The recipe is stingier with its pencil than it feels while you follow it.

A second prediction. Suppose the sheet holds a thousand numbers. How many comparisons does the recipe make? The first number is copied without being compared with anything. Every other number is compared exactly once. So the answer is 999. Call the length of the sheet $n$, and the count is $n-1$. For our sheet that is 3: the 3 against the 7, the 9 against the 7, the 4 against the 9.

## Why every number is looked at

Could a cleverer recipe look at fewer numbers? Suppose it skips one. Whatever it reports, I am allowed to have written an enormous number in the skipped place, bigger than everything else on the sheet, and the recipe would never find out. So any recipe that is always right must look at every number at least once. This is forced, not a custom: it follows from the way a single unseen number can overturn the answer. Our recipe looks at each number once, so on this point it cannot be improved.

## Taking the recipe apart

A recipe like this has parts, and the way to learn what each part does is to take it out.

Start with the first instruction, copying a number from the sheet. It might seem easier to begin with the scrap showing 0. Try it on a sheet reading $-5$, $-2$, $-8$. Nothing on the sheet is bigger than 0, so the scrap still says 0 at the end, a number that was never on the sheet. The scrap must begin with something that is on the sheet. That is forced. Which item you begin with is chosen. Start from the last number instead and walk backwards, and the sheet 7, 3, 9, 4 still ends on 9.

Next, the word 'strictly'. Replace it with 'bigger or equal' and run the recipe on a sheet reading 5, 5. The scrap holds 5 either way. For plain numbers this is a choice and a harmless one.

Then the blank sheet. The first instruction asks for a first number, and there is none. A blank sheet has no largest number, because there is nothing for a number to be the largest of. That is a fact, and it is forced. What the recipe reports about it is chosen. The usual written version of this procedure hands back a placeholder meaning 'nothing', and it could just as well raise an alarm.

One more part is easy to overlook: the answer can be checked. Anyone can confirm that 9 is on the sheet and that nothing on the sheet beats it. Every instruction is also well-defined, which I take to mean that two people following it with no judgement of their own will arrive at the same scrap. Compare this with the programs that choose which video to show you next. People often call them algorithms, but there is no correct video to check the choice against, so they rely on a heuristic instead: a rule of thumb for problems that have no well-defined right answer. A heuristic can be useful and still not be an algorithm in the strict sense.

## A sheet that never ends

Now hand the recipe a different sheet. It carries the whole numbers 1, 2, 3 and so on, with no last one. (Here the whole numbers start at 1.) Predict what the scrap says when the recipe finishes.

It never finishes. The scrap reads 1, then 2, then 3, rubbed out and rewritten at every step. Nothing is wrong with the recipe. This sheet has no largest number to find, since for any whole number $n$ the number $n+1$ is bigger. The recipe is not failing to find an answer. It is honestly refusing to stop, because there is none.

Try a sheet where an answer does exist: 1, 1, 1, forever. The largest number is plainly 1. The recipe still runs for ever, because, by the argument from earlier, it can never rule out an enormous number waiting further down the sheet. Having an answer and being able to stop are different properties, and a recipe needs the second one to be useful.

This is the missing piece. The recipe silently relied on a promise that was never written in it: the sheet is finite. With that promise it stops after $n-1$ comparisons. Without it, the same words describe a process that goes on indefinitely. An algorithm is a set of well-defined instructions that, when followed, stops after a finite number of steps with a solution to the problem. The stopping requirement is part of the definition itself. A program counts as an algorithm only if it stops eventually.

Is that requirement forced or chosen? Mostly chosen. Knuth gave the name 'computational method' to a procedure that has every property of an algorithm except finiteness, so the thing without the promise can be named and studied. Authors also disagree about related edges. Some hold that a procedure which rolls dice along the way is not an algorithm, others call the question debatable. The recipe here rolls no dice, so I did not need to settle it. What is forced is the reason for the choice: a procedure that never stops never hands you anything to read off the scrap.

## A name on a long road

The word began as a man's name. Around 825, al-Khwarizmi, a Persian scientist and polymath, wrote a book on Indian computation, using the numerals now called Hindu–Arabic, and a companion on addition and subtraction in the same system. In the early 12th century Latin translations of these appeared, attributed to John of Seville and to Adelard of Bath, and one of them opens with the words 'Dixit Algoritmi', which means 'Thus spoke al-Khwarizmi'. Algoritmi is his name, Latinised. A reader of that Latin met his name at the head of a method.

In English the word came to mean 'algorism': calculating with place value, where a digit's worth depends on where it stands, so the 3 in 30 is worth more than the 3 in 3. It appears in the Ancrene Wisse from about 1225. By the late 14th century Chaucer was describing augrym stones, counters used for the same kind of calculation. In the 15th century the Latin form was bent towards the Greek word for number, arithmos, and became algorithmus. By 1596 an English writer, Thomas Hood, had spelled it algorithm.

Al-Khwarizmi's other book, on calculation by completion and balancing, matters for the same reason our recipe does. It moved from answers to particular numerical problems towards general procedures for reducing and balancing equations. Our recipe does the same thing on a small scale. It does not answer 'what is the largest of 7, 3, 9 and 4'. It answers the question for every finite sheet at once.

I have left out how procedures are compared by cost and the many families they fall into, because one idea is enough for one sitting.

The recipe stops on every finite sheet, and we knew that before running it: it takes one step per number. Given a list of instructions with no such reason in sight, what would it take to know in advance that it stops?

Text licensed under CC BY-SA 4.0.
