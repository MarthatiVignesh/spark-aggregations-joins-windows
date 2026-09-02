# Spark Execution Plan

The application uses:

```scala
joinedData.explain(true)
```

and:

```scala
finalResult.explain(true)
```

With `explain(true)`, Spark displays multiple stages of query planning:

1. **Parsed Logical Plan** - the unresolved plan created from the DataFrame operations.
2. **Analyzed Logical Plan** - Spark resolves columns, expressions, and data types.
3. **Optimized Logical Plan** - Catalyst applies logical optimizations.
4. **Physical Plan** - Spark chooses the physical operators used to execute the query.

For the join and window examples, the physical plan can include operations such as joins, exchanges, sorts, aggregates, and window execution. These operators show how Spark turns high-level DataFrame code into an executable plan.

## Key Idea

DataFrame transformations are lazy. Calling `show()` or another action causes Spark to execute the required plan. Calling `explain(true)` lets us inspect how Spark has planned the query without needing to manually construct the execution stages.
