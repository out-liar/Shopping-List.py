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


# Online shopping code using classes:

class ShoppingCart(object):
  """Creates shopping cart objects
  for users of our fine website."""
  items_in_cart = {}
  def __init__(self, customer_name):
    self.customer_name = customer_name

  def add_item(self, product, price):
    """Add product to the cart."""
    if not product in self.items_in_cart:
      self.items_in_cart[product] = price
      print product + " added."
    else:
      print product + " is already in the cart."

  def remove_item(self, product):
    """Remove product from the cart."""
    if product in self.items_in_cart:
      del self.items_in_cart[product]
      print product + " removed."
    else:
      print product + " is not in the cart."

      
my_cart = ShoppingCart("Cane")
my_cart.add_item("Scythe", 2)



# ReturningCustomer inherits class from Customer class:

class Customer(object):
  """Produces objects that represent customers."""
  def __init__(self, customer_id):
    self.customer_id = customer_id

  def display_cart(self):
    print "I'm a string that stands in for the contents of your shopping cart!"

class ReturningCustomer(Customer):
  """For customers of the repeat variety."""
  def display_order_history(self):
    print "I'm a string that stands in for your order history!"

monty_python = ReturningCustomer("ID: 12345")
monty_python.display_cart()
monty_python.display_order_history()


