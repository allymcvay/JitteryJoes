# Team 7 Mist 4610 Group Project 1

## Team Name:
 21479 Group 7
  
## Group Member
  1. Ally McVay
  2. Sydney Pratt  https://github.com/scp31975/Jiterry-Joe-s-
  3. Casey Whichard  https://github.com/caseywhichard/Team-7-MIST-4610-Group-Project-1
  4. Mino Guzman https://github.com/Mino-Guzman/JitteryJoes
     
## Problem Description
The problem we have been tasked to solve is to design a data model and build a database that represents the relationships in operations of a global, multi‑location coffee chain. For this company, the Store serves as the central entity, since it is the physical center that connects customers to the products the coffee shop offers. The database also models the menu items and merchandise offered, suppliers of inventory, customer loyalty programs, and orders customers make. Using this data model, we generated realistic sample data that aligns with these entities and their relationships. By doing this, we are creating a database that allows us to perform relevant SQL queries that provide meaningful business insights that managers would be interested in, including company sales revenue, customer trends, and inventory levels.

## Explanation of Data Model 
As mentioned above, our model is based on the structure of a global coffee chain. The Store is the central entity that represents each physical coffee shop location. Each store hires many employees, so we established a one‑to‑many relationship between the Store and Employees entities. Also, several pieces of inventory and equipment are assigned to one store, so there is a one‑to‑many relationship with the Store and Inventory and with the Store and Equipment entities as well. Finally, one store can take many orders from customers, so we created a one-to-many relationship between the Store and Order entities. 

What drives this business is sales, so customers interact with the business through order purchases. These purchases can consist of orders of food, drinks, and merchandise. We concluded that one customer can place many orders, so we created a one‑to‑many relationship between the Customers and Order entities. Orders can consist of merchandise as well, so using the same idea that one customer can purchase several pieces of merchandise, we placed a one-to-many relationship between the Customers and Merchandise entities. Finally, customers typically participate in the loyalty program to earn points with the hopes of getting deals on future purchases. Each customer can only have one loyalty account attached to their name, so this is modeled as a one‑to‑one relationship between the Customers and Loyalty entities.

Customers can make several payments on order purchases, since they can return to the store whenever they would like.So, we established a one-to-many relationship between the Customers and Payment entities. We also assume that each order only consists of one payment, so we created a one-to-one relationship between the Order and Payment entities. 

The company requires supplies on hand that go into inventory. In order to generate supplies, the company requires a supplier or suppliers to supply these items. Each supplier can ship several supplier items, which led us to establish a one-to-many relationship between the Suppliers and SupplierItem entities.

Overall, the data model, as shown below, successfully captures the relationships between the activities that take place in a global coffee chain. It provides a detailed understanding on the customer orders, inventory and equipment levels, the payment process, and hiring distributions. 

<img width="641" height="647" alt="Screenshot 2026-03-31 at 9 31 34 AM" src="https://github.com/user-attachments/assets/03afe27d-a25b-4341-b278-34fab233a74d" />


## Data Dictionary 
### Customers
<img width="623" height="611" alt="Screenshot 2026-03-31 at 1 04 39 PM" src="https://github.com/user-attachments/assets/44a6ab8f-cc26-48fb-870c-0ef11535b54c" />

### Employees
<img width="644" height="621" alt="Screenshot 2026-03-31 at 1 04 59 PM" src="https://github.com/user-attachments/assets/1af5ba35-a235-427e-bf1e-659aa9f55c6b" />

### Equipment
<img width="637" height="552" alt="Screenshot 2026-03-31 at 1 05 19 PM" src="https://github.com/user-attachments/assets/0e81dcc8-0e5f-405c-bcd9-a311f9c886d1" />

### Inventory
<img width="645" height="624" alt="Screenshot 2026-03-31 at 1 07 50 PM" src="https://github.com/user-attachments/assets/6310ca44-7dec-4f31-83f7-232e28d4556e" />

### Loyalty
<img width="687" height="607" alt="Screenshot 2026-03-31 at 1 08 11 PM" src="https://github.com/user-attachments/assets/e60e9a79-6975-48ec-8c8e-23d610b651af" />

### MenuItem
<img width="681" height="438" alt="Screenshot 2026-03-31 at 1 08 24 PM" src="https://github.com/user-attachments/assets/19fb839d-03e6-4f80-ad5c-f3c88c3f17e0" />

### Merchandise
<img width="616" height="578" alt="Screenshot 2026-03-31 at 1 08 52 PM" src="https://github.com/user-attachments/assets/ac15f640-714c-4451-8b8f-636ba1b6bb78" />

### OrderItem
<img width="678" height="637" alt="Screenshot 2026-03-31 at 1 12 47 PM" src="https://github.com/user-attachments/assets/0938a01d-553f-4d9c-b58a-c1e812c6071f" />

### Orders
<img width="610" height="652" alt="Screenshot 2026-03-31 at 1 14 07 PM" src="https://github.com/user-attachments/assets/920968f7-302e-4755-a576-3d6d2b5cf4f6" />

### Payment
<img width="631" height="646" alt="Screenshot 2026-03-31 at 1 16 39 PM" src="https://github.com/user-attachments/assets/54103c85-716c-4167-ae71-fb7505ecd5ac" />

### Store
<img width="622" height="312" alt="Screenshot 2026-03-31 at 1 16 58 PM" src="https://github.com/user-attachments/assets/49c09f7c-dec3-44d9-ba6e-c0b2c7c860de" />

### SupplierItem
<img width="651" height="453" alt="Screenshot 2026-03-31 at 1 17 09 PM" src="https://github.com/user-attachments/assets/18037b95-b169-4783-a909-c2b441b8e6f0" />

### Suppliers
<img width="624" height="397" alt="Screenshot 2026-03-31 at 1 17 25 PM" src="https://github.com/user-attachments/assets/98539d96-6abe-4d13-b098-61f5ca96175b" />


## Queries

<img width="628" height="381" alt="Screenshot 2026-03-31 at 8 26 03 PM" src="https://github.com/user-attachments/assets/83856489-b4f6-473d-8e84-a2f4da8d79a6" />

### 1. List all cafe managers that are seasonal
<img width="622" height="404" alt="Screenshot 2026-03-31 at 8 02 52 PM" src="https://github.com/user-attachments/assets/ba85b380-15cc-4c04-8247-ae8bd9d19134" />
This query allows leadership to quickly identify which café managers are employed on a seasonal basis. Seasonal managers typically work only during peak periods, such as the academic year or high‑traffic months. Knowing exactly who these managers are helps the organization anticipate staffing gaps when the season ends. This ensures that stores relying on seasonal leadership receive the necessary support, training, or replacement coverage ahead of time. By isolating seasonal managers, the café can better plan for continuity, maintain service quality, and allocate resources to locations that may need additional managerial oversight once seasonal staff depart.

### 2. Show all items on the menu that have never been ordered
<img width="628" height="418" alt="Screenshot 2026-03-31 at 8 03 12 PM" src="https://github.com/user-attachments/assets/54fea064-087e-4b65-83a7-d9cadeec12ea" />
This query helps managers identify which menu items have never been purchased. Items with zero orders may signal low visibility, poor appeal, or unnecessary complexity on the menu. By isolating these products, managers can decide whether to promote them, adjust pricing, or remove them to reduce waste and streamline inventory.

### 3.Show all orders and status
<img width="621" height="483" alt="Screenshot 2026-03-31 at 8 03 26 PM" src="https://github.com/user-attachments/assets/54e126e0-9d7f-4e7c-922b-7ddc462ea8ca" />
This query pulls information from the SupplierItem and Suppliers tables to show what items have been shipped, when they were shipped, and the status of the supplier. It provides visibility into the supply chain and helps track incoming inventory.

### 4. Revenue by payment type
<img width="622" height="402" alt="Screenshot 2026-03-31 at 8 03 47 PM" src="https://github.com/user-attachments/assets/eeeb02b3-ef6c-40d1-a72c-e7841089aa24" />
This query shows how much revenue comes from each card type, helping managers understand which cards customers use most. This makes it easier to plan for reliable payment processing, manage card‑related fees, and ensure the café’s systems support the most common payment methods efficiently.

### 5. Average order value by store
<img width="622" height="422" alt="Screenshot 2026-03-31 at 8 04 02 PM" src="https://github.com/user-attachments/assets/85a638e4-3e73-4572-bf51-b1574034560f" />
This query calculates the average order value for each store and pairs it with key performance metrics such as total orders received and total revenue generated. By comparing stores based on their average order value, managers can quickly identify which locations are driving higher‑value transactions. Sorting the results in descending order makes it easier to prioritize high‑performing stores and recognize those that may need additional support, pricing adjustments, or promotional strategies to improve their average order size.

### 6. Most popular menu items by total quantity sold
<img width="624" height="403" alt="Screenshot 2026-03-31 at 8 04 23 PM" src="https://github.com/user-attachments/assets/42d0b19d-38d4-4bf2-8130-3ac1d93c7f0e" />
This query ranks the popularity of each item based on the item’s total quantity sold. The query ranked each menu item by the number of units sold across all orders, while also calculating the total revenue generated from each item. The information provided became a useful way to identify bestsellers and top revenue-driving items

### 7. Stores above average revenue
<img width="627" height="433" alt="Screenshot 2026-03-31 at 8 04 49 PM" src="https://github.com/user-attachments/assets/5b2cdb1e-4a7a-458e-ae37-afb58bd975c5" />
This query identifies which stores generate more revenue than the overall average across all locations. By first calculating each store’s total revenue and then using a subquery to determine the average of those totals, managers can clearly see which stores are outperforming expectations. Highlighting above‑average stores helps leadership recognize strong performers, allocate resources effectively, and understand which operational practices may be contributing to higher revenue.

### 8. Stores with low inventory that need to reorder
<img width="622" height="431" alt="Screenshot 2026-03-31 at 8 05 36 PM" src="https://github.com/user-attachments/assets/4b2027fb-5733-4c73-b029-a6b518d893ff" />
This query identifies any item at a store whose current quantity has dropped below its designated reorder level. It also calculates how many additional units are needed to reach that threshold again. By sorting the results from most urgent to least urgent, managers can quickly see which stores and items require immediate restocking. This helps prevent stockouts, supports smoother operations, and ensures that high‑demand products remain available to customers.

### 9. Show the customer who spent the most
<img width="625" height="431" alt="Screenshot 2026-03-31 at 8 05 52 PM" src="https://github.com/user-attachments/assets/f389efb7-52cd-48b8-83d5-70771abcc3ae" />
This query identifies the customer with the highest total spending across all their orders. The subquery calculates each customer’s total amount spent, finds the maximum value, and then matches that amount back to the specific customer’s name and ID. This helps managers quickly recognize top‑spending customers, understand purchasing behavior, and potentially target these high‑value customers for loyalty rewards or personalized promotions.

### 10. What menu items generate above average revenue 
<img width="621" height="455" alt="Screenshot 2026-03-31 at 8 06 08 PM" src="https://github.com/user-attachments/assets/0148eda7-e643-42c5-87e1-946fe089c01a" />
This query identifies which menu items generate more revenue than the average item on the menu. Like the store‑level version, it calculates each item’s total revenue and compares it to the overall average, returning only the strongest performers. This helps managers quickly see which products drive the most sales, guiding decisions about promotion, pricing, and menu placement to maximize revenue.


## Assumption

LoyaltyID is stored redundantly to preserve the customer’s loyalty tier at the time of the order/payment, since loyalty status can change over time.
