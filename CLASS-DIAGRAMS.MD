
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

```
@startuml

class ProductService {
  +getAvailableProducts(): List<Product>
  +getProductDetails(productId: String): Product
  +addProduct(product: Product): void
  +removeProduct(productId: String): void
}

class Product {
  -productId: String
  -name: String
  -price: float
  -quantity: int
  +getProductId(): String
  +getName(): String
  +getPrice(): float
  +getQuantity(): int
}

ProductService -- Product

@enduml

```

```

@startuml

class CartService {
  +addToCart(productId: String): void
  +removeFromCart(productId: String): void
  +updateQuantity(productId: String, quantity: int): void
  +calculateTotalCost(): float
}

class CartItem {
  -productId: String
  -quantity: int
  +getProductId(): String
  +getQuantity(): int
}

CartService -- CartItem

@enduml

```

```

@startuml

class OrderService {
  +placeOrder(cartItems: List<CartItem>): Order
  +getOrderDetails(orderId: String): Order
  +updateOrderStatus(orderId: String, status: String): void
  +cancelOrder(orderId: String): void
}

class Order {
  -orderId: String
  -orderItems: List<CartItem>
  -status: String
  +getOrderId(): String
  +getOrderItems(): List<CartItem>
  +getStatus(): String
}

OrderService -- Order
Order -- CartItem

@enduml


```

