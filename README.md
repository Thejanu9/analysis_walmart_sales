
# Walmart Retail Sales Analysis

![Walmart Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Walmart_logo.svg/1280px-Walmart_logo.svg.png)

## Project Overview

This retail analytics project systematically processes, transforms, and analyzes Walmart's sales data spanning 15 years (2001–2015) to uncover actionable business insights. Leveraging Python for data handling, advanced cleaning techniques (handling missing values, outlier correction, and feature engineering), and MySQL for efficient database management and visualization techniques to uncover retail business insights.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
 - [Prerequisites](#prerequisites)
 - [Installation](#installation)
- [Usage](#usage)
 - [Data Analysis](#data-analysis)
- [Key Insights](#key-insights)
- [Deployment](#deployment)
- [Future Enhancements](#future-enhancements)
- [Author](#author)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Features

- **Data Cleaning**: Processes raw Excel data, handles special characters, and formats dates
- **Database Integration**: Connects to MySQL database for efficient data storage and retrieval
- **Sales Growth Analysis**: Calculates year-over-year sales growth rates by state
- **Profitability Analysis**: Identifies most profitable product categories by region
- **Data Visualization**: Creates insightful visualizations of sales trends and profitability
- **SQL Optimization**: Utilizes advanced SQL queries including window functions and CTEs

## Project Structure

```
Walmartsalesanalysis/
├── Data/
│   └── WalmartRetailSales_Cleaneddata.csv
├── Analysis_Part/
    └── data.py
├── Visualtions/
│   └──Highest Profitsubcategory.png
    └── Most Profitablesub category.png
    └── top 5 most profitable.png
├── requirements.txt
├── README.md
├── LICENSE.md
└── .gitignore

                 
```

## Technologies Used

- **Python 3.XX**: Core programming language
- **pandas**: Data manipulation and analysis
- **pymysql**: MySQL database connector
- **sqlalchemy**: SQL toolkit and Object-Relational Mapping
- **matplotlib & seaborn**: Data visualization
- **MySQL**: Database management system

## Getting Started

### Prerequisites

- Python 3.9 or higher
- MySQL Server 5.7 or higher
- Git (for version control)

### Installation
  - Follow these clear steps to set up the Walmart Retail Sales Analysis Poject on your system:

   1. **Clone the repository**
  ```bash
  git clone https://github.com/Thejanu9/analysis_walmart_sales.git
  ```

   2. **Install required Python packages**
  ```bash
  pip install pandas pymysql sqlalchemy matplotlib seaborn
  ```
  - These packages provide essential functionality for data manipulation, database connections, and visualization.


   3. **Step 3: Set Up MySQL Database**
    i. **Install MySQL**
  ```bash
  sudo apt install mysql-server
  ```
   ii. **Secure MySQL Installation**
  ```bash
  sudo mysql_secure_installation
  ```
   - Follow the prompts to set a root password and secure your installation.
    
   iii. **Check MySQL Status**
  ```bash
  sudo systemctl status mysql
  ```
   - Ensure that MySQL is running (look for "active (running)")
    
   iv. **Set up MySQL database**
  ```bash
  mysql -u root -p
  ```
   - Enter your password when prompted, then run these SQL commands:
     
     
  ```sql
  CREATE DATABASE walmart;
  USE walmart;
  
  CREATE TABLE sales (
    `Row ID` INT,
    `Order ID` INT,
    `Order Date` DATE,
    `Order Priority` TEXT,
    `Order Quantity` INT,
    `Sales` DOUBLE,
    `Discount` DOUBLE,
    `Ship Mode` TEXT,
    `Profit` DOUBLE,
    `Unit Price` DOUBLE,
    `Shipping Cost` DOUBLE,
    `Customer Name` TEXT,
    `Customer Age` TEXT,
    `City` TEXT,
    `Zip Code` INT,
    `State` TEXT,
    `Region` TEXT,
    `Customer Segment` TEXT,
    `Product Category` TEXT,
    `Product Sub-Category` TEXT,
    `Product Name` TEXT,
    `Product Container` TEXT,
    `Product Base Margin` TEXT,
    `Ship Date` TEXT
  );
  ```

4. **Prepare your data**
  - Place  WalmartRetailSales.csv in the project root directory.
    Once these steps are completed, you can run the analysis scripts in sequence (cleaning → database operations 
    → analysis → visualization) to process the data and generate insights

## Usage



### Data Analysis

Run the data analysis module to generate insights:

```bash
python data_tools_project (1).py
```

This script will:
- Analyze yearly sales trends
- Calculate state-by-state sales growth
- Identify most profitable product categories by region
- Generate visualizations of key findings

## Key Insights

The analysis reveals several important business insights:

1. **Regional Performance**: Office Machines are the most profitable product category in both South and Central regions, while Binders and Binder Accessories lead in the East region.

2. **Sales Growth Patterns**: Several states show significant sales volatility, with Wyoming experiencing 687% growth in 2013 followed by a 87% decline in 2015.

3. **Yearly Trends**: Order volume increased dramatically in 2012-2015 compared to earlier years, with 2012 showing the highest number of orders.


### Database Operations Tests

```bash
python database_operations.py
```
Tests database connectivity, query execution, and data type handling.

### Data Analysis Tests

```bash
python data_tools_project (1).py
```
Validates analysis functions and visualization generation.

## Deployment

This project is designed for flexible deployment but still not deployed but can done by using GitHub CI/CD pipeline, flask/django framework, fastapi and aws server or heroku:

### Local Analysis

Follow the installation instructions to run locally for data analysis.

### Server Deployment

For server deployment:
1. Set up a server with Python and MySQL
2. Configure database connection parameters in the scripts
3. Schedule regular runs using cron or similar tools

### Dashboard Integration

The visualization components can be integrated with web frameworks:
1. Use Flask or Django to create a web interface
2. Embed visualizations in HTML templates
3. Deploy to a web server for team access

## Future Enhancements

Potential improvements for future versions:

- Implement machine learning for sales prediction
- Add interactive dashboards using Plotly or Dash
- Integrate with real-time data sources
- Expand analysis to include customer demographics
- Add automated reporting functionality

## Author

**Thejanu Meze**

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- Walmart for providing the retail sales dataset
