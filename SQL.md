# 🗃️ SQL Comprehensive Guide

## 1. What is SQL and What is it Used For?

SQL is a query language designed for managing relational databases. It is the primary language for tasks like data retrieval, data manipulation, and database administration.

### Core Components

- **DDL (Data Definition Language)**: Defines and modifies database structure
- **DML (Data Manipulation Language)**: Adds, modifies, and removes data
- **DCL (Data Control Language)**: Manages permissions and access rights
- **TCL (Transaction Control Language)**: Handles commits and rollbacks

## 2. SQL vs NoSQL

| Characteristic | SQL | NoSQL |
|---------------|-----|-------|
| Database Type | Relational | Non-relational (document, key-value, graph) |
| Data Structure | Structured, Semi-structured | Unstructured, Semi-structured |
| Best Suited For | Complex Queries, Transactions | Real-time data, Flexible schemas |

## 3. WHERE vs HAVING Clauses

### Key Differences

```sql
SELECT 
    department, 
    AVG(salary) as avg_salary
FROM 
    employees
WHERE 
    employment_type = 'Full-time'  -- Filters before grouping
GROUP BY 
    department
HAVING 
    AVG(salary) > 50000;  -- Filters after aggregation
```

#### Comparison
- **WHERE**: 
  - Filters records before grouping
  - Works with individual rows
  - Cannot use aggregate functions

- **HAVING**:
  - Filters grouped data
  - Works with aggregated results
  - Can use aggregate functions like SUM, AVG, COUNT
