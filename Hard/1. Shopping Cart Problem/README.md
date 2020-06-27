# Shopping Cart Problem - Hard

> Date : 1st July 2020

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

### Vendor Inputs & Output

Input & output can be in any format or variation but it must include the following.

| Sl. No. | Feature                    | Input                                                                                                                                                                                                        | Output                                                                                                                                                                                                      |
| ------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1.**  | **Add shopping category**  | - Name                                                                                                                                                                                                       | The added shopping category:<br><br>- Name<br>- Category ID                                                                                                                                                 |
| **2.**  | **Add shopping item**      | - Name<br>- Original price<br>- Discount price<br>- Weight<br>- Category ID                                                                                                                                  | The added shopping item: <br><br>- Name<br>- Original price<br>- Discount price<br>- Weight<br>- Category ID                                                                                                |
| **3.**  | **List shopping item**     | All the filtering & sorting parameters for listing shopping items. The vendor may or may not select these parameters.<br><br>- Name<br>- Original price<br>- Discount price<br>- Weight<br>- Category ID     | A list of shopping items with the following parameters<br><br>- Name<br>- Original price<br>- Discount price<br>- Weight<br>- Category ID                                                                   |
| **4.**  | **List shopping category** | All the filtering & sorting parameters for listing shopping categories. The vendor may or may not select these parameters.<br><br>- Name                                                                     | A list of shopping categories with the following parameters<br><br>- Name<br>- Category ID                                                                                                                  |
| **5.**  | **List orders**            | All the filtering & sorting parameters for listing orders. The vendor may or may not select these parameters.<br><br>- Order ID<br>- Order status<br>- Billing date <br>- Total amount <br>- Delivery option | A list of orders with the following parameter<br><br><br>- Order ID<br>- Order status<br>- Billing date <br>- Total amount <br>- Delivery option<br>- Order status (‘in progress’, ‘completed’, ‘canceled’) |
| **6.**  | **Change order status**    | - Order ID<br>- New status (‘in progress’, ‘completed’, ‘canceled’)                                                                                                                                          | The added order:<br><br>- Order ID<br>- Order status<br>- Billing date <br>- Total amount <br>- Delivery option<br>- Order status (‘in progress’, ‘completed’, ‘canceled’)                                  |

### Customer Inputs & Output

Input & output can be in any format or variation but it must include the following.

| Sl. No. | Feature                | Input                                                                                                                                                                                                                   | Output                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------- | ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1.**  | **Create order**       | - Name <br>- Phone no<br>- Payment method (cash/card/online)<br>- Selected items and it's quantity <br>- Takeaway / Home delivery<br>- Distance from shop to the delivery address in KM. (if Home delivery is selected) | A generated bill which contains the following.<br><br>Static data<br>- Shop name: `Gadget Guru`<br>- Shop address: `311/5 Akshay nagar, Bangalore, Karnataka, India`<br>- Shop contact no: `+91 7849626879`<br><br>Variable data<br>- Customer name<br>- Customer phone no<br>- Items bought, it's quantity, price & discount price<br>- Total tax<br>- Total shipping charge<br>- Total amount saved<br>- Sum amount to be paid<br>- Payment method used<br>- Billing date and time<br>- Order status |
| **2.**  | **Check order status** | - Order ID                                                                                                                                                                                                              | Same as above                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

## Requirements for submission

- Last Submission Date : `30th July 2020`

## How to submit solution?

Follow the steps mentioned in [this](../../CONTRIBUTING.md) file to submit your solution.

## Stuck somewhere?

Then you might want to solve these versions of the problem first.

- [Easy](../../Easy/1.%20Shopping%20Cart%20Problem/README.md)
- [Medium](../../Medium/1.%20Shopping%20Cart%20Problem/README.md)