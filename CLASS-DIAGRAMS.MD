
# Class Diagrams


## Class Diagram for Product Service

```

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
  -description: string

  /* getter and setters */

}

ProductService -- Product


```

## Class Diagram for Cart Service

```

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


```

## Class Diagram for Order Service

```


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


```

