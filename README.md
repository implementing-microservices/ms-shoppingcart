# ms-shoppingcart

Shopping Cart Microservice

## Jobs To Be Done

Template: 

```
When <circumstance>, $actor wants to <motivation> so that they <goal>
```

### Jobs:

1. **When** shopper finds an item they like, **they want to** add it to a cart
   **so that** they can later buy it
1. **When** shopper changes their mind about buying an item in a cart, **they
   want to** remove it from the cart **so that** they can avoind buying it
1. **When** shopper decides where to ship items in their cart, **they want to**
   update shipping information **so that** purchase can be shipped to the
   correct address
1. **When** shopper changes their mind about where to ship the purchase, **they
   want to** remove shipping information **so that** the items don't get shipped
   to the wrong address, and so that they can later add the correct shipping
   information
1. **When** shopper decides how to pay for the items in their cart, **they want
   to** update payment information **so that** correct payment instrument gets
   charged
1. **When** shopper changes their mind about how to pay for the items in their
   cart, **they want to** update shipping information **so that** wrong payment
   instrument doesn't get charged
1. **When** shopper is ready to finalize their purchase, **they want to** click
   "purchase now" button **so that** they can finalize the purchase and
   eventually receive the items purchased.

### Actions:

1. Add item to cart
  - Inputs: customer_id, product_id, product_customizations
  - Response: guid of the item in the cart
  - Expected result: product with indicated customizations (e.g. color) added
  to the cart
1. Remove item from cart
  - Inputs: customer_id, guid of the item in the cart
  - Response: success or error
  - Expected result: product removed from the cart
  