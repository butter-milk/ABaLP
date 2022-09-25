# Arbitrage betting as LP problem

## Introduction
Arbitrage betting, also known as sure bets, is a way in which you would presumably be able to make money (or break-even) on any bet you make. In this repository, we will propose a way to see arbitrage betting as a LP-problem. This is useful for multiple bets, since in plenty of sports apps, one can bet on more than 2 outcomes (think of win/loss/draw or a finite set of possible goal-outcomes in a soccer match), or even a finite amount of different goal possibilities.
## Problem definition
We define P= {p1...pn} a finite set of maximum payouts found on combination of sites, such that pi is the payout factor when qi occurs. We are now tasked to maximize the profit we make, whilst only being able to spend a limited amount of money (since we are all broke after all). This limit we call L.
## Resulting problem and conclusions
For this problem, we can define the following LP problem:<br />
Maximize: $rewards - losses$ <br />
$rewards \leq p_i*x_i \hspace{2cm} i\leq n$ <br />
$losses \geq \sum_i x_i$ <br />
$\sum_i x_i \leq L$ <br />
When the result is positive, you will make a profit on this game. and you could spend amount xi on that outcome. If the result turns out to be negative, it does mean that you could lose money. Note that it is of great importance that P covers all possible outcomes! Otherwise one could still lose money. 
Note that this LP problem does not take any transaction cost into account. Howwever, this would not be a problem, since most of the time there are only withdrawal fees present in those apps.
As there are plenty of algorithms and websites available to solve LP problems (e.g. https://online-optimizer.appspot.com/?model=builtin:default.mod), we will not provide any additional simplex algorithm implementation of our own. I hugely doubt on whether someone could actually find a good combination. However, I would love to hear if this actually helped you make money <3 

**GAMBLING AND LOTTERIES ARE TAXES FOR THE POOR**



