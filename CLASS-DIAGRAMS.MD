
# Class Diagram: Product

```text
+------------------+
| Product |
+------------------+
| - id: string |
| - name: string |
| - price: float |
| - description: string |
+------------------+
| + getId(): string |
| + getName(): string |
| + getPrice(): float |
| + getDescription(): string |
| + setId(id: string): void |
| + setName(name: string): void |
| + setPrice(price: float): void |
| + setDescription(description: string): void |
+------------------+

```

# Class Diagram: Service Classes

```text

+------------------+                +-------------------+
|   ProductService |                |   CartService     |
+------------------+                +-------------------+
|                  |                |                   |
| - retrieveProducts()             | - addToCart()     |
| - getProductDetails()            | - removeFromCart()|
| - addProduct()                   | - updateQuantity()|
| - removeProduct()                | - calculateTotal()|
+------------------+                +-------------------+
          ^
          |
          |
+-------------------+
|   OrderService    |
+-------------------+
|                   |
| - placeOrder()    |
| - getOrderDetails()|
| - updateStatus()  |
| - cancelOrder()   |
+-------------------+

```


