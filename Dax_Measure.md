# DAX Measures

## Total Orders

```DAX
Total Orders = COUNT(Orders[Order_ID])
```

---

## Average Delivery Time

```DAX
Avg Delivery Time =
AVERAGE(Orders[Delivery_Time_Hours])
```

---

## On Time Delivery %

```DAX
On Time Delivery % =
DIVIDE(
    CALCULATE(
        COUNT(Orders[Order_ID]),
        Orders[Delivery_Status] = "On Time"
    ),
    COUNT(Orders[Order_ID])
)
```

---

## Customer Satisfaction %

```DAX
CST % =
AVERAGE(Orders[Customer_Satisfaction])
```

---

## Active Vehicles

```DAX
Active Vehicles =
CALCULATE(
    COUNT(Vehicles[Vehicle_ID]),
    Vehicles[Status] = "Active"
)
```
