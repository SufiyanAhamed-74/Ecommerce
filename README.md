# E-Commerce Delivery Analysis \| Power BI

## Project Overview

This Power BI project analyzes **E-commerce delivery performance**
across **JioMart, Swiggy Instamart, and Blinkit**. The interactive
dashboard compares order volume, delivery speed, on-time delivery, order
value, service ratings, delivery delays, refund requests, and customer
feedback.

The goal is to identify delivery-performance patterns and compare the
three platforms to support data-driven operational and
customer-experience decisions.

## Dashboard Preview

Upload your dashboard screenshot to the repository as `dashboard.png`,
then use:

``` markdown
![Quick Commerce Delivery Analysis Dashboard](Dashboard.jpg)
```

## Key KPIs

-   Total Orders
-   Average Delivery Time (Minutes)
-   On-Time Delivery (%)
-   Average Order Value (INR)
-   Average Service Rating
-   Delivery Delay (%)
-   Refund Requested (%)

## Dashboard Analysis

-   **Total Orders by Platform** --- compares order contribution across
    the three platforms.
-   **Average Delivery Time by Platform** --- compares delivery
    efficiency.
-   **On-Time Delivery (%) by Platform** --- evaluates orders delivered
    without delay.
-   **Delivery Time Distribution (%)** --- analyzes orders across
    delivery-time ranges.
-   **Delivery Delay (%) by Platform** --- compares late-delivery rates.
-   **Average Delivery Time by Product Category** --- compares delivery
    performance across product categories.
-   **Key Metrics by Platform** --- provides a consolidated KPI
    comparison.
-   **Customer Feedback & Refund Analysis** --- supports evaluation of
    customer experience and service issues.

## Interactive Filters

The dashboard includes slicers for: - Platform - Product Category -
Service Rating - Customer Feedback - Delivery Delay - Refund Requested

A **Clear Filters** button allows users to quickly reset selections.

## Tools & Technologies

-   **Power BI Desktop**
-   **Power Query** --- data cleaning and transformation
-   **DAX** --- calculated columns and measures
-   **Data Visualization** --- KPI cards, donut charts, clustered
    charts, matrix, slicers, and interactive filtering

## Sample DAX Measures

### Total Orders

``` dax
Total Orders =
COUNTROWS('Ecommerce Delivery Analysis')
```

### Delivery Delay %

``` dax
Delivery Delay % =
DIVIDE(
    CALCULATE(
        COUNTROWS('Ecommerce Delivery Analysis'),
        'Ecommerce Delivery Analysis'[Delivery Delay] = "Yes"
    ),
    COUNTROWS('Ecommerce Delivery Analysis')
) * 100
```

### Refund Requested %

``` dax
Refund Requested % =
DIVIDE(
    CALCULATE(
        COUNTROWS('Ecommerce Delivery Analysis'),
        'Ecommerce Delivery Analysis'[Refund Requested] = "Yes"
    ),
    COUNTROWS('Ecommerce Delivery Analysis')
) * 100
```

### Delivery Time Group

``` dax
Delivery Time Group =
SWITCH(
    TRUE(),
    [Delivery Time (Minutes)] <= 10, "0 - 10 mins",
    [Delivery Time (Minutes)] <= 20, "10 - 20 mins",
    [Delivery Time (Minutes)] <= 30, "20 - 30 mins",
    [Delivery Time (Minutes)] <= 40, "30 - 40 mins",
    "40+ mins"
)
```

## Key Insights

The dashboard helps answer questions such as: - Which platform receives
the highest number of orders? - Which platform has the fastest average
delivery time? - How do on-time delivery and delay rates compare? - How
are orders distributed across different delivery-time ranges? - How does
delivery time vary by product category? - How do refund requests,
ratings, and customer feedback vary by platform? - Which platform
performs best across the major operational KPIs?

## Dataset Features

The analysis uses order-level fields including: - Order ID - Customer
ID - Platform - Delivery Time (Minutes) - Product Category - Order Value
(INR) - Customer Feedback - Service Rating - Delivery Delay - Refund
Requested

## Conclusion

This project demonstrates practical skills in **Power BI, Power Query,
DAX, KPI analysis, data visualization, and interactive dashboard
design**. It provides a clear comparison of JioMart, Swiggy Instamart,
and Blinkit across delivery performance, customer experience, and
operational metrics.

## Author

**Sufi Ahamed**

Data Analytics \| Power BI \| SQL \| Python \| Excel
