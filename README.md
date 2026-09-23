CANTEEN – FOOD ORDERING

Feature Set III

A simple Canteen Food Ordering System designed as a college assignment. This project demonstrates the basic concepts of Algorithm, Flowchart, and ER (Entity-Relationship) Diagram for a food ordering system.

---

📌 Project Overview

The Canteen Food Ordering system manages customer details, menu items, food orders, discounts, and the final bill.

The system includes:

1. Customer Details
2. Menu Items
3. Order Details
4. Discount
5. Final Bill

---

👨‍💻 Features

- Enter customer details
- Display available menu items
- Select food items
- Enter quantity
- Calculate amount for each item
- Calculate total order amount
- Check discount eligibility
- Calculate discount amount
- Calculate final bill
- Display the final bill

---

📝 Algorithm

CANTEEN – FOOD ORDERING

1. START

2. Enter Customer ID, Customer Name, and Phone Number.

3. Display available menu items with Item ID, Item Name, Category, and Price.

4. Select a food item.

5. Enter the quantity.

6. Calculate the amount for the selected item.
   
   Item Amount = Price × Quantity

7. Ask whether the customer wants to select more items.

8. If YES, repeat Steps 4 to 7.

9. If NO, calculate the total order amount.
   
   Total Amount = Sum of all Item Amounts

10. Check whether the customer is eligible for a discount.

11. If YES, enter/apply the discount percentage.

12. Calculate the discount amount.

Discount Amount = Total Amount × Discount Percentage / 100

13. Calculate the final bill.

Final Bill = Total Amount − Discount Amount

14. Display the Final Bill.
15. STOP

---

🔄 Flowchart

The flowchart follows these steps:

              ┌─────────────┐
              │    START    │
              └──────┬──────┘
                     ↓
          ╱────────────────────╲
         ╱ Enter Customer       ╲
        ╱       Details          ╲
        ╲────────────────────────╱
                     ↓
          ╱────────────────────╲
         ╱   Display Menu       ╲
        ╱       Items            ╲
        ╲────────────────────────╱
                     ↓
             ┌───────────────┐
             │ Select Food   │
             │     Item      │
             └───────┬───────┘
                     ↓
          ╱────────────────────╲
         ╱   Enter Quantity     ╲
        ╲────────────────────────╱
                     ↓
             ┌───────────────┐
             │ Calculate     │
             │ Item Amount   │
             └───────┬───────┘
                     ↓
                ◇───────────◇
               ◇ More Items? ◇
                ◇─────┬─────◇
                   YES│    │NO
                      │    ↓
                      │  ┌────────────────┐
                      │  │ Calculate Total │
                      │  │     Amount     │
                      │  └───────┬────────┘
                      │          ↓
                      │     ◇──────────────◇
                      │    ◇ Discount       ◇
                      │   ◇   Eligible?     ◇
                      │    ◇──────┬─────────◇
                      │       YES │     │ NO
                      │           │     │
                      │           ↓     │
                      │    ┌───────────────┐
                      │    │Calculate       │
                      │    │Discount Amount │
                      │    └───────┬───────┘
                      │            │
                      └────────────┘
                                   ↓
                         ┌──────────────────┐
                         │ Calculate Final  │
                         │      Bill        │
                         └────────┬─────────┘
                                  ↓
                       ╱────────────────────╲
                      ╱  Display Final Bill  ╲
                      ╲──────────────────────╱
                                  ↓
                           ┌─────────────┐
                           │    STOP     │
                           └─────────────┘

Flowchart Symbols

Symbol| Meaning
Oval| Start / Stop
Parallelogram| Input / Output
Rectangle| Process / Calculation
Diamond| Decision
Arrow| Flow Direction

---

🗃️ ER Diagram

Entities

1. CUSTOMER

- Customer_ID (PK)
- Customer_Name
- Phone_Number

2. MENU_ITEM

- Item_ID (PK)
- Item_Name
- Category
- Price

3. ORDER

- Order_ID (PK)
- Order_Date
- Customer_ID (FK)
- Total_Amount

4. ORDER_DETAILS

- Order_Detail_ID (PK)
- Order_ID (FK)
- Item_ID (FK)
- Quantity
- Item_Total

5. DISCOUNT

- Discount_ID (PK)
- Order_ID (FK)
- Discount_Percentage
- Discount_Amount

6. FINAL_BILL

- Bill_ID (PK)
- Order_ID (FK)
- Total_Amount
- Discount_Amount
- Final_Amount

---

🔗 Relationships

CUSTOMER
    │
    │ 1:M
    ↓
  PLACES
    │
    ↓
  ORDER
   /   \
  /     \
1:M       1:1
↓          ↓
CONTAINS   GETS
↓          ↓
ORDER      DISCOUNT
DETAILS

MENU_ITEM
    │
    │ 1:M
    ↓
APPEARS IN
    │
    ↓
ORDER_DETAILS

ORDER
  │
  │ 1:1
  ↓
GENERATES
  │
  ↓
FINAL_BILL

Main Relationships

- Customer → Places → Order — One customer can place many orders (1:M).
- Order → Contains → Order Details — One order can contain many order-detail records (1:M).
- Menu Item → Appears in → Order Details — One menu item can appear in many order-detail records (1:M).
- Order → Gets → Discount — One order can have one discount record (1:1).
- Order → Generates → Final Bill — One order generates one final bill (1:1).

---

💰 Billing Formulas

Item Amount

Item Amount = Price × Quantity

Total Amount

Total Amount = Sum of all Item Amounts

Discount Amount

Discount Amount = Total Amount × Discount Percentage / 100

Final Bill

Final Bill = Total Amount − Discount Amount

---

📊 Database Structure

CUSTOMER
   │
   │ 1:M
   ↓
ORDER ────────────────┐
 │                    │
 │ 1:M                │ 1:1
 ↓                    ↓
ORDER_DETAILS       DISCOUNT
 ↑
 │ M:1
 │
MENU_ITEM

ORDER
  │
  │ 1:1
  ↓
FINAL_BILL

---

🎯 Objective

The main objective of this assignment is to understand how a basic food ordering system can be represented using:

- Algorithms
- Flowcharts
- Entities and Attributes
- Primary Keys and Foreign Keys
- Relationships
- Cardinalities
- Billing calculations

---

🛠️ Technologies / Concepts Used

This assignment mainly uses:

- Algorithm Design
- Flowchart
- ER Diagram
- Database Concepts
- Basic Mathematical Calculations

---

📁 Project Structure

Canteen-Food-Ordering/
│
├── README.md
│
├── Algorithm/
│   └── algorithm.txt
│
├── Flowchart/
│   └── flowchart.png
│
└── ER-Diagram/
    └── er-diagram.png

---

🎓 Academic Assignment

Project: Canteen – Food Ordering
Feature Set: III
Topic: Algorithm, Flowchart and ER Diagram

This project is created for educational and academic purposes.
