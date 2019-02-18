# Shopping-List.py
This code takes a shopping list, and computes the total price, and updates the stock level based on the order.

# This project uses lists and dictionaries in the context of shopping. For loops perform a defined function on each item in the list and dictionary, and the data is updated in response to changes in the environment by altering the stock level.
#

shopping_list = ["banana", "orange", "apple"]
# Stock dictionary with the item as the key and stock level as the value.
stock = {
  "banana": 6,
  "apple": 0,
  "orange": 32,
  "pear": 15
}
# Price dictionary containing the item as a key and the price as the value.
prices = {
  "banana": 4,
  "apple": 2,
  "orange": 1.5,
  "pear": 3
}

# The function below computes the shopping list and uses a for loop to count the total and update the stock level.
def compute_bill(food):
  total = 0
  for item in food:
    if stock[item] > 0:
      total = total + prices[item]
      stock[item] = stock[item] - 1
  return total

print compute_bill(shopping_list)


# Dynamic shopping interface courtesy of out_liar consulting
