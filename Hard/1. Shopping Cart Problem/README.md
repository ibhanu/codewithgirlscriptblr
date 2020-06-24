# Shopping Cart Problem - Hard

> Date : Jun 21' 2020

Kudos to you! We have an exciting problem that will make you a true Ninja!
Proceed with this section only on completing the [Easy](../../Easy/1.%20Shopping%20Cart%20Problem/README.md) and [Hard](../../Hard/1.%20Shopping%20Cart%20Problem/README.md) section.

## Problem Statement

In this section, ‘Gadget Guru’ features two exclusive modes:

1. ‘Vendor mode’ which allows the admin to perform various tasks like adding shopping items, viewing and filtering customer’s orders and changing the status of the orders.

2. ‘Customer mode’ is for the user to create new orders taking into account additional parameters like distance and Order ID(for the customers to track the status of their orders). The functionality for checking the status of previous orders should be added.The customer should be able to retrieve data after restarting the app.

The app has to generate a bill accordingly containing all the details provided by the user and the total amount. The appropriate status of the orders has to be included.

### Vendor mode

- Vendor can do the following tasks:
  - Add shopping category
  - Add shopping item
  - View all customer orders and filter & sort them with status (status can be ‘in progress’, ‘completed’, ‘canceled’), billing date, total amount, delivery option.
  - View all shopping category and filter & sort them with name.
  - View all shopping items and filter & sort them with name, category, original price, discount price.
  - Change order status.
- All the shopping item, category and orders should have unique IDs.
- Shopping items must include
  - Name
  - Original price
  - Discount price
  - Weight in grams
- All the data should be stored in such a way that it is retrieved even after the app restarts. (It can be achieved by using file storage, database storage, etc).

### Customer mode

- Customer can perform the following tasks
  - Create a new order
  - Check the status of a previous order

#### Creating an order

- When the application runs, the user must be asked the following.
  - Name
  - Phone no
  - Payment method `(cash/card/online)`
  - Select multiple shopping item and it’s quantity.
    `For Example, the user can select 3 basshead earphones & 2 bluetooth computer mouse`
  - Takeaway / Home delivery
  - Distance from shop to the delivery address in KM. (if Home delivery is selected)
- The shopping items should be displayed category wise.
- While listing the shopping items, the application should display the original price, discount price, and the amount saved by the user if he/she buys that product.
- The shop doesn’t provide home delivery to addresses more than 50KM away. If the user selects more than 50KM, an appropriate message should be displayed.
- The app should generate a bill for the selected item, including a 6% tax on the total amount.
- The total amount should include a shipping charge if Home delivery is selected. The shipping charge is to be calculated as:
  | Distance | Price |
  |----------|-------------|
  | <= 5 KM | Free |
  | <= 20 KM | Rs. 30 |
  | <= 50 KM | Rs. 60 |
  | > 50 KM | No delivery |
- The bill should show the total amount saved by the user if he/she bought any discount products.
- The bill should contain all the other details provided by the user.
- The bill should contain the shop details as well as the billing date and time.
- Each order should have a unique ‘Order ID’ such that the user can use to check the status.
- The default status of the order should be ‘in progress’
- All the data should be stored in such a way that it is retrieved even after the app restarts. (It can be achieved by using file storage, database storage, etc).

#### Checking order status

- The customer should enter the order ID and the app should return the bill (as in ‘create order’) along with the order status.

### Inputs

Input can be in any format or variation but it must include the following.

#### Vendor - Add shopping category

- Name

#### Vendor - Add shopping item

- Name
- Original price
- Discount price
- Weight
- Category ID

#### Vendor - Change order status

- Order ID
- New status (‘in progress’, ‘completed’, ‘canceled’)

#### Vendor - List shopping category

All the filtering & sorting parameters for listing categories. The vendor may or maynot select these parameters.

- Name

#### Vendor - List shopping item

All the filtering & sorting parameters for listing shopping items. The vendor may or maynot select these parameters.

- Name
- Original price
- Discount price
- Weight
- Category ID

#### Vendor - List orders

All the filtering & sorting parameters for listing orders. The vendor may or maynot select these parameters.

- Order ID
- Order status
- Billing date
- Total amount
- Delivery option

#### Customer - Create order

- Name
- Phone no
- Payment method (cash/card/online)
- Selected items and it's quantity
- Takeaway / Home delivery
- Distance from shop to the delivery address in KM. (if Home delivery is selected)

#### Customer - Check order status

- Order id

### Output

Output will be a bill based on the given input. The bill can be in any format but it must include the following

#### Vendor - Add shopping category

After adding the shopping category, the app should display the added category.

- Name
- Category ID

#### Vendor - Add shopping item

After adding the shopping item, the app should display the added item.

- Name
- Original price
- Discount price
- Weight
- Category ID

#### Vendor - Change order status

After changing the order status, the app should display the following parameters of the order.

- Order ID
- Customer name
- Billing date & time
- Total amount
- Delivery option
- New status (‘in progress’, ‘completed’, ‘canceled’)

#### Vendor - List shopping category

The list should include all the categories with all the parameters of shopping category.

- Name
- Category ID

#### Vendor - List shopping item

The list should include all the items with all the parameters of shopping item.

- Name
- Original price
- Discount price
- Weight
- Category ID

#### Vendor - List orders

The list should include all the orders with all the parameters of the order.

- Order ID
- Order status
- Billing date
- Total amount
- Delivery option
- Order status (‘in progress’, ‘completed’, ‘canceled’)

#### Customer - Create order/check order status

##### Static data

- Shop name: `Gadget Guru`
- Shop address: `311/5 Akshay nagar, Bangalore, Karnataka, India`
- Shop contact no: `+91 7849626879`

##### Variable data

- Customer name
- Customer phone no
- Items bought, it's quantity, price & discount price
- Total tax
- Total shipping charge
- Total amount saved
- Sum amount to be paid
- Payment method used
- Billing date and time
- Order status

#### Customer - Check order status

Same as above.

## Requirements for submission

- Last Submission Date : Jul 02' 2020

## How to submit solution?

Follow the steps mentioned in [this](../../CONTRIBUTION.md) file to submit your solution.

## Stuck somewhere?

Then you might want to solve these versions of the problem first.

- [Easy](../../Easy/1.%20Shopping%20Cart%20Problem/README.md)
- [Medium](../../Medium/1.%20Shopping%20Cart%20Problem/README.md)
