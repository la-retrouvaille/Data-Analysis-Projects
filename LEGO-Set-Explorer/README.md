# 🧱 LEGO Set Explorer

*An interactive Power BI report for filtering and exploring LEGO sets by theme, age, price, and more.*

---

## 📋 Table of Contents

1. [✨ Project Overview](#-project-overview)  
2. [📂 Data](#-data)  
3. [🚀 How to Open & Use](#-how-to-open--use)  
4. [🔍 Key Features](#-key-features)  
5. [📁 Folder Structure (Git Repo)](#-folder-structure-git-repo)
6. [💻 Tech Stack & Dependencies](#-tech-stack--dependencies)
7. [💡 Next Steps & Optional Enhancements](#-next-steps--optional-enhancements)  
8. [👩‍💻 Licence & Credit](#-licence--credit)
9. [📧 Contact](#-contact)

---

## ✨ Project Overview

### Situation:

As a LEGO enthusiast, finding the perfect next set can be overwhelming due to the sheer variety of themes, pieces, and price points available.

### Goal: 

Create an interactive Power BI tool that helps users explore and filter thousands of LEGO sets using specific criteria such as theme, age range, number of pieces, and price.

### Tasks:

- **Data loading & prep**
  
  - Clean and filter for valid records (with age, price, pieces, and image)
  - Create custom columns: Age Range, Price Range
  - Add DAX measures for KPIs
    
- **Report design**
  
  - Create card visuals for key metrics (total sets, avg. price, avg. pieces)
  - Add slicers for filtering by theme group, theme, age range
  - Insert a data table with key columns and pricing tiers
  - Include visual interaction logic for clean filtering
    
- **Interactivity**
  
  - Add tooltips with LEGO set images
  - Configure a max price slider and filtering logic
  - Use bookmarks/buttons for filter resets
  - Include a Decomposition Tree for drill-down analysis
  
---

## 📂 Data

Source data was provided via CSV.

`lego_sets.csv`	LEGO set metadata (name, theme, age, price, pieces, image URL, etc.)

---

## 🚀 How to Open & Use

1. **Clone the repo**
   
   ```bash
   git clone https://github.com/la-retrouvaille/data-analysis-projects.git
   cd data-analysis-projects/lego-set-explorer
   
2. **Open the Power BI report**
   
   - Launch Power BI Desktop
   - Open `LEGO_Set_Explorer.pbix`
   - Verify data source settings
   - Refresh the model and explore the dashboard

---

## 🔍 Key Features

- **KPIs:**
  
  - Total Sets: 4,385
  - Avg. Pieces: 411
  - Avg. Price: $45
    
- **Filters:**

  - Theme Group
  - Theme
  - Age Range
  - Max Price slider (0-850)

- **Visuals:**

  - Card visuals for KPIs
  - Table of sets with sorting and filtering
  - Image and set details viewer
  - Decomposition Tree with breakdown by category, theme group, and name

![Dashboard main page.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/Dashboard%20main%20page.PNG)

![Dashboard page 2.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/Dashboard%20page%202.PNG)

---

## 📁 Folder Structure (Git Repo)

**/LEGO-Set-Explorer**

  - [LEGO_Set_Explorer.pbix](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/LEGO_Set_Explorer.pbix) <- PowerBI Dashboard

  - [Dashboard main page.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/Dashboard%20main%20page.PNG) <- A screenshot of the dashboard's main page

  - [Dashboard page 2.PNG](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/Dashboard%20page%202.PNG) <- A screenshot of the dashboard's 2nd page

  - [Lego_Logo.png](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/Lego_Logo.png) <- The LEGO logo used for this dashboard

  - [lego_sets.csv](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/lego_sets.csv) <- source file
   
  - [.gitignore](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/.gitignore) <- Git rules: files/directories to ignore

  - [README.md](https://github.com/la-retrouvaille/Data-Analysis-Projects/blob/main/LEGO-Set-Explorer/README.md) <- This file  

---

## 💻 Tech Stack & Dependencies

BI: Power BI Desktop

---

## 💡 Next Steps & Optional Enhancements
 
- **Add Set Count by Year:** Visualize trends over time
- **Include User Ratings or Reviews**
- **Add Randomizer:** Add a 3rd page where users are able to have a randomly selected set. Call it "Surprise Me!"
- **Optimize for mobile layout** (Power BI mobile view)
  
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
