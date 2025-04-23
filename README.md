# Marketing Overview Dashboard – Power BI

## Overview

This Power BI dashboard provides a comprehensive **Marketing Overview** for an online retail platform. It brings together multiple business-critical metrics to offer actionable insights across sales, logistics, supplier performance, and customer behavior.

The dashboard enables users to interactively explore the data, make data-driven decisions, and monitor key performance indicators (KPIs) across the business pipeline.

---

## 📊 Dashboard Snapshot

![Marketing Overview Dashboard](
https://github.com/SURESH745/online-shop-V1-Share-Public/blob/main/Screenshot%202025-04-23%20223514.png)

## Sample DAX

Completed_Payments_Ratio = 
VAR TotalOrders = CALCULATE(COUNTROWS(payment5), ALL(payment5[transaction_status]))
VAR CompletedOrders = CALCULATE(COUNTROWS(payment5), payment5[transaction_status] = "Completed")
RETURN IF(TotalOrders = 0, BLANK(), CompletedOrders / TotalOrders)

## Key Features

- **Sales Insights**
  - Total sales trend from Nov 2023 to Sep 2024
  - Last 30 days sales with growth indicator vs. target
  - Successful payments ratio with benchmark tracking

- **Logistics Metrics**
  - Average shipment duration by carrier (FedEx, DHL, UPS)
  - Average delivery time
  - Order fulfillment lead time

- **Supplier & Product Analytics**
  - Top 10 suppliers by sales volume and share
  - Best and worst selling products
  - Ratings by product category

- **Customer Segmentation**
  - New vs. returning customer filters
  - Product category-based filtering
  - Time-based slicers for custom analysis

---
![Marketing Overview Dashboard](https://github.com/SURESH745/online-shop-V1-Share-Public/blob/main/Screenshot%202025-04-23%20223514.png)

## Data Model Summary

The report integrates multiple data sources as follows:

| Table              | Description                                        |
|-------------------|----------------------------------------------------|
| `orders`           | Order details with timestamps                     |
| `order_items`      | Line item data including product info             |
| `products`         | Product categories, names, and prices             |
| `suppliers`        | Supplier names and contributions                  |
| `reviews`          | Category-wise product reviews                     |
| `shipments`        | Carrier-wise shipment durations                   |
| `payment`          | Payment status and success ratio                  |
| `customers`        | Customer segmentation and types                   |

---

![Marketing Overview Dashboard](https://github.com/SURESH745/online-shop-V1-Share-Public/blob/main/Screenshot%202025-04-23%20220735.png)

## KPIs Summary (Sample Data)

- **Total Sales:** €30.6M  
- **Last 30 Days Sales:** €2.87M  
- **Successful Payments Ratio:** 80%  
- **Average Delivery Time:** 7.59 days  
- **Order Fulfillment:** 3.06 days  
- **Top Supplier:** Next Level Systems (€2.45M)  
- **Top Product:** 4K Monitor (€738,175)

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/SURESH745/online-shop-V1-Share-Public.git
