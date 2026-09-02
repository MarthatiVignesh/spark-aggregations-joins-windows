# Output

The application prints five main sections to the terminal.

## Example 1: Sales Analysis

- Sales Data
- Simple Aggregation
- Grouping Aggregation by Product
- Customer Aggregation
- Window Aggregation - Running Total per Customer
- Window Ranking - Orders Ranked by Amount per Customer

## Example 2: Join + Execution Plan

- Customers DataFrame
- Orders DataFrame
- Inner Join result
- Customer totals after join
- Extended execution plan

## Final Exercise

The final result contains:

```text
customer_id | customer_name | city       | order_id | amount | total_spending | order_rank
1           | Chintan       | Hyderabad  | 101      | 50000  | 75000          | 1
1           | Chintan       | Hyderabad  | 103      | 25000  | 75000          | 2
2           | Rahul         | Mumbai     | 106      | 40000  | 60000          | 1
2           | Rahul         | Mumbai     | 102      | 20000  | 60000          | 2
3           | Priya         | Bangalore  | 104      | 30000  | 30000          | 1
4           | Amit          | Delhi      | 105      | 15000  | 15000          | 1
```

The program also prints the extended Spark execution plan for the join and final result.
