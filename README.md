The diagram below shows the architecture of the stock market simulator

![image](https://github.com/jashdalal/Stock-Market-Matching-Engine/assets/33259149/0a4af1bc-946c-4045-bd8d-01963576b3fc)

How does the matching engine work?

•	The system matches buy orders with sell orders when the buy price is greater than or equal to the sell price – when that happens the orders match and an execution is generated at the sell price.

•	The matching engine processes orders in a first in first out (FIFO) manner i.e. orders at the same price that arrive earlier get execution earlier

•	In case that the complete order cannot be executed (filled) at a certain point, a partial execution will be generated.

To implement the matching engine, a **Python-based heap framework** was used to match buy and sell orders placed by authorized clients. You can read more about this [here](matching%20engine/Matching_Engine_Core_integer_time.py) 

We use the **FIX** protocol for the Matching Engine to communicate with Real Time Markets and Execution Links. 
