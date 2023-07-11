# Online Shopping System

## Case Study: Online Shopping System

### Microservice 1: Product Service
- Responsible for managing the products available in the online store.
- Functionalities:
  - Retrieve a list of available products.
  - Get details of a specific product.
  - Add a new product.
  - Remove a product.

### Microservice 2: Cart Service
- Handles the management of the user's shopping cart.
- Functionalities:
  - Add a product to the cart.
  - Remove a product from the cart.
  - Update the quantity of a product in the cart.
  - Calculate the total cost of the products in the cart.

### Microservice 3: Order Service
- Manages the order processing and fulfillment.
- Functionalities:
  - Place a new order.
  - Retrieve order details by order ID.
  - Update the order status (e.g., processing, shipped, delivered).
  - Cancel an order.

## Scenario
Sarah is an online shopper who wants to purchase a laptop from an online store.

1. Sarah visits the online store and browses the available laptops in the product catalog.
2. She selects a laptop and adds it to her cart using the Cart Service.
3. Sarah proceeds to checkout and provides her shipping and payment details.
4. The Order Service receives the order request and generates a unique order ID for Sarah's purchase.
5. Sarah's payment is processed, and the order status is set to "processing."
6. The Order Service notifies the Product Service to reduce the laptop's stock quantity.
7. Sarah can track her order status using the Order ID provided during checkout.
8. Once the laptop is shipped, the Order Service updates the order status to "shipped" and provides a tracking number.
9. Sarah receives the laptop and marks the order as "delivered" in the system.
10. The Product Service updates the laptop's stock quantity, reflecting the successful sale.

In this case study, the three microservices work together to facilitate the online shopping experience for Sarah. The Product Service manages the available products, the Cart Service handles the shopping cart functionality, and the Order Service manages the order processing and fulfillment. Each microservice has its specific functionalities and interacts with the others to ensure a seamless online shopping experience for Sarah.
