## What are UNION, MINUS and INTERSECT commands
- **UNION** operator is used to combine the result of two table while removing duplicate entries

- **INTERSECT** operator is used to combine the result of both queries into a single row, but both SELECT query must have the same amount of rows.

- **MINUS** operator is used to return rows from the first query but not from the second query/

## What are some common clauses used with SELECT query in SQL
- **WHERE** clause filter records that are required depending on certain criteria
- **ORDER BY** clause is used to sort data in ascending order or descending
- **GROUP BY** used to group entries with identical data and may be used with aggregation method to summarise.


## What is OLTP?
OLTP, or online transactional processing, allows huge groups of people to execute massive amounts of database transactions in real time, usually via the internet. A database transaction occurs when data in a database is changed, inserted, deleted, or queried.

##  What is the difference between ‘HAVING’ CLAUSE and a “where” clause?
- Both are used to filter records, but having different context and purposes
- WHERE clause
    - used to filter rows before any groupings are made, and is used to filter records from a single table or multiple tables in a SELECT, UPDATE, DELETE statement.
    - The WHERE clause cannot be used with aggregate functions directly like COUNT()
- HAVING clause
    - The HAVING clause is used to filter groups after the GROUP BY clause has been applied.
    - It is specifically designed to filter aggregated data.

    ```
    #EXAMPLE
    SELECT department, COUNT(*)
    FROM employees
    GROUP BY department
    HAVING COUNT(*) > 10;
    ```

## What is the ACID principle in database transactions, and why is it important?
 - 	Acid Principle is a set of properties that ensure the reliability and consistency of database transaction,
    - **Atomicity** - Guarantees that transaction is a single unit, meaning that either all of its operations are successfully completed or none of them are, so there can be no transaction that have some of the transaction completed while the others have not
    - **Consistency** - Ensure that transaction modify DB from one valid state to another valid state, the DB remains in a consistent state before and after, adhering to define constraints, rules and relationship
    - **Isolation** - Ensure that the execution of multiple transactions concurrently does not interfere with each other, prevents dirty reads, non-repeatable reads and phantom reads
    - **Durability** - Ensure that once transaction has been committed, it is permanently stored in the DB and is not lost due to hardware failures, power outages etc.


## Can you briefly explain the CAP theorem
Cap theorem is a fundamental principle in distributed systems, that states that in a distributed system, it is impossible for a distributed data store to simultaneously provide all three following guarantees

 - **Consistency** - Every read operation on the data store returns the most recent write value or an error, so all nodes agree on the current state of the data at all times
 - **Availability** - Every request made to the data store receive a response, either success or failure, even if nodes fail, the whole system remains available
 - **Partition Tolerance** - System continues to operate and function correctly even if network partition occur, meaning message sent between node is lost or delayed

## How would you approach designing the schema for a new relational database?

- **Understand requirements**: Types of data, relationships, and usage patterns (read heavy, write heavy).
- **Identify Relationships**:
  - **Core entities**: Users, products, and orders.
  - **Supporting entities**: Categories, addresses, and payments.
- **Normalize schema**: Ensure no redundancy and anomalies.
  - Break down large tables into smaller tables.
- **Choose data types and constraints**: Indexing columns.
- **Document and test schema**: Check with stakeholders.

## What are the steps to ensure a successful DB migration?

1. **Plan and schedule migration**
2. **Backup data**
3. **Write migration scripts**
4. **Test migrations**
5. **Execute migrations**
6. **Communicate status updates**
7. **Perform post-migration checks**
8. **Monitor and optimize**
9. **Document changes**

## What is database normalization, and why is it important in database design?

Database normalization is the process of organizing the attributes and tables of a relational database to minimize redundancy and dependency. The goal is to produce a database schema that is free from anomalies, such as redundancy, update anomalies, and deletion anomalies. This usually involves decomposing large tables into smaller and more manageable tables. Reasons include:

- **Minimizing redundancy**: Helps reduce storage space and ensures data consistency.
- **Ensuring data integrity**
- **Improving query performance**
- **Facilitating maintenance and modification**
- **Supporting scalability**

## Could you describe how indexing works in databases and why it's beneficial?

Indexing is a technique used in databases to improve the speed of data retrieval operations, such as SELECT queries, by enabling faster lookup of rows.

#### How it works:

- Creation of indexes
- Data access with indexes: The DB engine consults the index to locate the rows.
#### Types of indexes:
- Single-column index
- Composite index: Indexes created on multiple columns.
- Unique index: Enforces uniqueness constraints on the indexed columns.
- Clustered index: The physical order of rows in the table is determined by the index key.
- Non-clustered index

#### Maintenance of indexes:

- Indexes need to be maintained and can result in write operations being a bit costly.

#### Advantages:

- Improved query performance
- Faster sorting and join operations
- Reduced disk I/O
- Support for constraints and data integrity
- Scalability and concurrency

### Common Methods for Optimizing Database Performance:

- Indexing
- Query optimization
- Database schema design
- Partitioning
- Caching
- Connection pooling

### Strategies for Ensuring Data Consistency in Distributed Systems:

- Use distributed transactions
- Consensus algorithms: Paxos and Raft.
- Replication and quorum-based techniques
- Eventual consistency
- Conflict resolution mechanisms
- Versioning and timestamping
- Synchronization protocols
