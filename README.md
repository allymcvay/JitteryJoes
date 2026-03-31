# Team 7 Mist 4610 Group Project 1

## Team Name:
  Group 7
  
## Group Member
  1. Ally McVay
  2. Sydney Pratt
  3. Casey Whichard
  4. Mino Guzman
     
## Problem Description
The goal of this project is to design and build a relational database that represents the core operations of Jittery Joe’s, a multi‑location coffee shop. The Store serves as the central entity, connecting employees, inventory, equipment, customers, and daily transactions. The database models how each store manages menu items, merchandise, suppliers, loyalty programs, and customer orders.
We aim to accurately represent these relationships, generate realistic sample data, and populate each entity accordingly. Once built, the database will support functional SQL queries that provide meaningful business insights into sales, inventory levels, customer behavior, and overall store performance.

## Explanation of Data Model 
Our model is based on the structure of a multi‑location coffee shop, Jittery Joe’s.
The Store entity represents each physical coffee shop location. Each store employs multiple workers, which is why we established a one‑to‑many relationship between the Store and Employees entities. Stores also manage their own equipment and inventory, so the Equipment and Inventory tables each have a one‑to‑many relationship with Store as well.

Customers interact with the business primarily through orders. Because a customer can place many orders, we created a one‑to‑many relationship between Customers and Order. Customers may also participate in the loyalty program, which is represented by the Loyalty entity. Since each customer can have at most one loyalty account, this is modeled as a one‑to‑one relationship between Customers and Loyalty.

Each order contains multiple items, and each menu item can appear in many different orders. To represent this many‑to‑many relationship, we created the OrderItem associative entity, which links Order and MenuItem. OrderItem also stores the quantity and unit price for each item purchased.

Inventory is replenished through shipments from suppliers. The SupplierItem entity represents items shipped by suppliers, and the Inventory table references these shipments to track which supplier deliveries contributed to current stock levels. Because a supplier can ship many items, but each shipment record corresponds to a single supplier, this is modeled as a one‑to‑many relationship between Suppliers and SupplierItem.

Payments are recorded in the Payment entity, which stores the payment method, amount, and date. Each order has exactly one payment associated with it, so we modeled a one‑to‑one relationship between Order and Payment. Payment also references the customer who made the purchase, allowing the business to analyze spending behavior.

Finally, the Merchandise entity represents retail items sold in stores, such as mugs or apparel. Merchandise is tied to specific store locations, so we included a one‑to‑many relationship between Store and Merchandise.

Overall, this data model captures the full operational flow of Jittery Joe’s—from customers placing orders, to inventory being supplied, to payments being processed—while maintaining clear relational structure that supports meaningful business insights.
