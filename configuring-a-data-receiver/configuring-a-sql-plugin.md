# Configuring a SQL Plugin

The customer may have machine data that is already being aggregated into a SQL datastore. The preferred handoff to Sight Machine is through a FactoryTX plugin that receives the SQL data, parses it into the JSON format, and saves it so it can be transmitted properly.

## SQL FTX Configuration File Sample

![](/configuring-a-data-receiver/Full FTX SQL Config File Code Sample w Lines.png)

## Creating a Polling Query and Adding Keywords

You will want the design of the SQL query to be as efficient as possible.

For example:

* Wherever possible, you want to use an index in your WHERE function to reduce load.

* In order to see if you are using an index, you may want to test your query using the EXPLAIN function. Use these references:

  * **PostgreSQL:**  
    [https://www.postgresql.org/docs/9.1/static/sql-explain.html](https://www.postgresql.org/docs/9.1/static/sql-explain.html)

  * **MySQL:**  
    [https://dev.mysql.com/doc/refman/5.7/en/explain.html](https://dev.mysql.com/doc/refman/5.7/en/explain.html)

  * **MS SQL Server:**  
    [https://www.red-gate.com/simple-talk/sql/performance/execution-plan-basics/](https://www.red-gate.com/simple-talk/sql/performance/execution-plan-basics/)



