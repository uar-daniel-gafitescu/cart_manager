[![Build Status](https://travis-ci.org/alexandrubagu/cart_manager.svg?branch=master)](https://travis-ci.org/alexandrubagu/cart_manager) [![Coverage Status](https://coveralls.io/repos/github/alexandrubagu/cart_manager/badge.svg?branch=master)](https://coveralls.io/github/alexandrubagu/cart_manager?branch=master)

# Cart
**Create, manage baskets**

## Supervisor tree
![Supervision tree of Cart Manager](https://raw.githubusercontent.com/alexandrubagu/cart_manager/master/images/supervisor_tree.png)


## Usage
#### Create new basket using user_id
```elixir
basket_id = Basket.Manager.create_basket_or_return_basket_id(Basket.Manager, user_id)
```

#### With basket_id created we can get the basket pid
```elixir
basket_pid = Basket.Manager.get_basket(Basket.Manager, basket_id)
```

#### With basket_pid we can add_product, delete_product, purchase through Basket(Agent) functions
```elixir
 Basket.add_product(basket_pid, product_id)
 Basket.delete_product(basket_pid, product_id)
 Basket.purchase(basket_pid)
```
