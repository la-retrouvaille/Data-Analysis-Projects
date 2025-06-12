# 🍴 Restaurant Order Analysis

*A deep dive into the Taste of the World Café's new menu performance and customer behavior.*

---

## 📋 Table of Contents

1. [✨ Project Overview](#-project-overview)  
2. [📂 Data](#-data)  
3. [🚀 How to Open & Use](#-how-to-open--use)  
4. [🔍 Key Findings](#-key-findings)  
5. [📁 Folder Structure (Git Repo)](#-folder-structure-git-repo)
6. [💻 Tech Stack & Dependencies](#-tech-stack--dependencies)
7. [💡 Next Steps & Optional Enhancements](#-next-steps--optional-enhancements)  
8. [👩‍💻 Licence & Credit](#-licence--credit)
9. [📧 Contact](#-contact)

---

## ✨ Project Overview

### Situation:

The *Taste of the World Café* has rolled out a brand-new menu at the start of the year. 

### Goal: 

Leadership wants to know which menu items are doing well (or poorly), and what do our top-spending customers prefer?

### Tasks:

- Explore the `menu_items` table to understand the new offerings.  
- Explore the `order_details` table to profile order activity.  
- Combine both tables to analyze customer behavior and identify top-spend orders.

---

## 📂 Data

All data is loaded into two tables in a SQL database:

- **`menu_items`**  
  | Column          | Description                       |
  |-----------------|-----------------------------------|
  | `menu_item_id`  | Unique item identifier            |
  | `item_name`     | Name of the dish/beverage         |
  | `category`      | e.g. Appetizer, Main Course, etc. |
  | `cuisine`       | e.g. Italian, Asian, Mexican      |
  | `price`         | Per‐item price (USD)              |

- **`order_details`**  
  | Column               | Description                             |
  |----------------------|-----------------------------------------|
  | `order_details_id`   | Unique line-item ID                     |
  | `order_id`           | Unique order identifier                 |
  | `order_date`         | Date of the order                       |
  | `order_time`         | Time of the order                       |
  | `item_id`            | Foreign key -> `menu_items.menu_item_id` |

The schema and sample data are created via the **`create_restaurant_db.sql`** script.

---

## 🚀 How to Open & Use

1. **Clone the repository**

   ```bash
   git clone https://github.com/la-retrouvaille/data-analysis-projects.git
   cd data-analysis-projects/restaurant-order-analysis

2. **Initialize the database**

   - **SQLite**

   ```bash
   sqlite3 restaurant.db < create_restaurant_db.sql
   ```

   - **PostgreSQL**
     
   ```bash
   psql -d your_database -f create_restaurant_db.sql
   ```

   - **MySQL**
     
   ```bash
   mysql -u your_username -p your_database < create_restaurant_db.sql
   ```

3. **Execute analysis scripts**
   
   - **SQLite**

   ```bash
   sqlite3 restaurant.db < menu_items_analysis.sql
   sqlite3 restaurant.db < order_details_analysis.sql
   sqlite3 restaurant.db < customer_behavior_analysis.sql
   ```

   - **PostgreSQL**
     
   ```bash
   psql -d your_database -f menu_items_analysis.sql
   psql -d your_database -f order_details_analysis.sql
   psql -d your_database -f customer_behavior_analysis.sql
   ```

   - **MySQL**
     
   ```bash
   mysql -u your_username -p your_database < menu_items_analysis.sql
   mysql -u your_username -p your_database < order_details_analysis.sql
   mysql -u your_username -p your_database < customer_behavior_analysis.sql
   ```
   
---

## 🔍 Key Findings

- **Menu Composition**

  - **Total items on the menu:** 32
  - **Price range:** Edamame (Asian) - $5.00 … Shrimp Scampi (Italian) - $19.95
  - **Italian dishes (9 total):** Spaghetti - $14.50 … Shrimp Scampi - $19.95
  - **By category:**
    
    | Category | # Items | Avg. Price |
    |---------:|--------:|-----------:|
    | American |       6 |     $10.07 |
    | Asian    |       8 |     $13.48 |
    | Italian  |       9 |     $16.75 |
    | Mexican  |       9 |     $11.80 |


- **Order Patterns**
  
  - **Date range:** Jan 1 2023 - Mar 31 2023  
  - **Total orders:** 5,370
  - **Total items:** 12,234
  - **Largest order:** #4305 (14 items)
  - **Orders > 12 items:** 20  


- **Customer Behavior & Spend**

  - **Least ordered:** Chicken Tacos (Mexican) - 123 purchases
  - **Most ordered:** Hamburger (American) - 622 purchases

    **Top 5 Spend Orders**  

    | Rank | Order | Date       | Spend   |
    |-----:|------:|-----------:|--------:|
    |    1 |   440 | 2023-01-08 | $192.15 |
    |    2 |  2075 | 2023-02-04 | $191.05 |
    |    3 |  1957 | 2023-02-02 | $190.10 |
    |    4 |   330 | 2023-01-06 | $189.70 |
    |    5 |  2675 | 2023-02-14 | $185.10 |

    **Order 440 Breakdown**  

    | Category | Items |
    |---------:|------:|
    | Italian  |     8 |
    | American |     2 |
    | Asian    |     2 |
    | Mexican  |     2 |

    **Combined Top 5 Breakdown**
    
    | Category | Items |
    |---------:|------:|
    | Italian  |    26 |
    | Asian    |    17 |
    | Mexican  |    16 |
    | American |    10 |

> *Insight:* Italian cuisine dominates high-spend orders.  
    
---

## 📁 Folder Structure (Git Repo)

- **Restaurant-Order-Analysis/**

  - [create_restaurant_db.sql](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Restaurant-Order-Analysis/create_restaurant_db.sql) <- Script to create the restaurant database

  - [menu_items_analysis.sql](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Restaurant-Order-Analysis/menu_items_analysis.sql) <- Script to analyze menu items

  - [order_details_analysis.sql](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Restaurant-Order-Analysis/order_details_analysis.sql) <- Script to analyze orders
  - 
  - [customer_behavior_analysis.sql](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Restaurant-Order-Analysis/customer_behavior_analysis.sql) <- Script to analyze customer behaviour

  - [.gitignore](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Restaurant-Order-Analysis/.gitignore) <- Git rules: files/directories to ignore

  - [README.md](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/Restaurant-Order-Analysis/README.md) <- This file  

---

## 💻 Tech Stack & Dependencies

SQL: SQLite / PostgreSQL / MYSQL

---

## 💡 Next Steps & Optional Enhancements
 
- Build an interactive dashboard
- Time-series & revisit–rate analysis
- Automate periodic reports

---

## 👩‍💻 Licence & Credit

This project is licensed under the **MIT License** - see the [LICENSE](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LICENSE) file for details.

- **Data Source:** Maven Analytics
- **Emojis & Icons:** [Emojipedia](https://emojipedia.org/)

---

## 📧 Contact

Egi Aliaj

[GitHub](https://github.com/la-retrouvaille) | [LinkedIn](https://www.linkedin.com/in/egialiaj/)

*Thank you for exploring this project! Feel free to ⭐ the repo if you found it helpful.*  
