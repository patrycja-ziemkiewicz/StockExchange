
# Stock Market Simulation

This app was developed as an assignment during OOP course as a part of the Computer Science Bachelor’s Studies at the Faculty of Mathematics, Computer Science, and Mechanics, University of Warsaw. In this project, the main goal is simulating the stock market system and investors.

## Overview

### How to run simulation
- Download everything from this folder
- Compile the project (with IntelliJ for example)
- Run main with two parameters: `path_to_input_file` `number_of_rounds`

## Inputs

Inputs template (text in angle brackets describes subsequent data, while text in parentheses describes their types):

```
<investors: each R lub S>
<stock companies <name>: <starting price>>
<investor's wallet: <funds> <stocks <name>: <count>>
```

For example, inputs given in the original task look like [this](https://raw.githubusercontent.com/SmerfTV/StockMarket/refs/heads/main/input.txt).

## Types of Investors

### RANDOM
An investor making random investment decisions (implement any strategy, e.g., random order type for buy/sell, random company, random number of shares, random price limit). The randomization occurs according to the specified conditions.

### SMA
An investor making decisions based on technical analysis of individual stocks using the Simple Moving Average (SMA n) - the arithmetic mean of prices over the last n rounds (in our task, we use n=5 and n=10). The price in a given round is taken as the price of the last transaction for that stock, which occurred in one of the previous rounds (if there are no transactions for several rounds, the stock price remains unchanged).  
A buy signal occurs when the shorter average - SMA 5 crosses from below the longer average - SMA 10, while a sell signal occurs when SMA 5 crosses from above SMA 10.

## Output

The simulation will print the final state of the portfolio for each investor after completing all rounds of the simulation.

## Original Task Description

[Original task description (in Polish)](https://github.com/SmerfTV/StockMarket/blob/main/task_desc.pdf)
