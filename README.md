# Advance-Decline-A-D-Line-BIST

The advance/decline line (or A/D line) is a technical indicator that plots the difference between the number of advancing and declining stocks on a daily basis. The indicator is cumulative. 

The A/D line is used to show market sentiment, as it tells traders whether there are more stocks rising or falling. There are ready to use indicators on TradingView etc. for NYSE but in this project we are calculating for Borsa İstanbul. If new IPO's will come it will be added.

### How to Calculate A/D

- Collect Data:

    - Obtain the list of stocks traded on BIST for the day.
    - For each stock, determine:
        - Advancing stocks: Stocks that closed higher than their previous closing price.
        - Declining stocks: Stocks that closed lower than their previous closing price.

- Calculate the Net Advances:
    * Net Advances = Number of Advancing Stocks − Number of Declining Stocks

- Add Net Advances to the Previous A/D Line Value:
    - Current A/D Line Value = Previous A/D Line Value + Net Advances

- Repeat Daily:
    - Update the A/D Line value each day by adding the Net Advances of the current day.


## Requirements

```Bash
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
```