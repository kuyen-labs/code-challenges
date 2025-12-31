# Fuul Backend Code Challenge

## Overview

Fuul is helping one of their projects that runs an NFT marketplace. You need to implement a checkout system that calculates the total price for a cart of items, applying various discount rules.

## Product Catalog

The marketplace currently sells 3 NFT products with the following base prices:

| Product Code | Product Name | Base Price |
|--------------|--------------|------------|
| APE          | Bored Apes   | 75 ETH     |
| PUNK         | Crypto Punks | 60 ETH     |
| MEEBIT       | Meebits      | 4 ETH      |

**Note:** Prices are obtained from an external source (like OpenSea) and can fluctuate. For this challenge, you should mock the price fetching functionality.

## Discount Rules

The marketplace offers two types of discounts:

### 1. 2-for-1 Promotion
- **Product:** APE
- **Rule:** Buy 2 APE, get 1 APE for free
- **Example:** 3 APE items = 2 × 75 ETH = 150 ETH (instead of 3 × 75 ETH = 225 ETH)

### 2. Bulk Purchase Discount
- **Product:** PUNK items only
- **Rule:** Buy 3 or more PUNK items, price per unit reduces 20%
- **Example:** 4 PUNK items = 4 × 48 ETH = 192 ETH (instead of 4 × 60 ETH = 240 ETH)

## Checkout Interface

The checkout process should allow items to be scanned in any order and return the total amount to be paid.

### Example Usage (Ruby)

```ruby
# Initialize checkout with pricing rules
co = Checkout.new(pricing_rules)

# Scan items in any order
co.scan("APE")
co.scan("APE") 
co.scan("PUNK")

# Get total price
price = co.total
```

## The Program

Using ruby, node, go or JAVA, implement a checkout process that fulfills the requirements.

```
Items: APE, PUNK, MEEBIT
Total: 139 ETH

Items: APE, PUNK, APE
Total: 210 ETH

Items: PUNK, PUNK, PUNK, APE, PUNK
Total: 267 ETH

Items: APE, PUNK, APE, APE, MEEBIT, PUNK, PUNK
Total: 298 ETH
```

#### The code should:

* Be written as production-ready code. You will write production code.
* Be easy to grow and easy to add new functionality.
* Have notes attached, explaining the solution and why certain things are included and others are left out.
* Mock the results of the call to the external price source integration. 
