# Chapter 03 Storage and Retrieval

## Section 02 Transaction Processing or Analytics?

| Property             | Transaction Processing Systems (OLTP)             | Online Analytic Systems (OLAP)            |
| -------------------- | ------------------------------------------------- | ----------------------------------------- |
| Main read pattern    | Small number of records per query, fetched by key | Aggregate over large number of records    |
| Main write pattern   | Random-access, low-latency writes from user input | Bulk import (ETL) or event stream         |
| Primarily used by    | End user/customer, via web application            | Internal analyst, for decision support    |
| What data represents | Latest state of data (current point in time)      | History of events that happened over time |
| Dataset size         | GB or TB scale                                    | TB or PB scale                            |



### Data Warehousing

A <i>data warehouse</i> is a separate database that analysts can query to their hearts' content, without affecting OLTP operations.

#### The divergence between OLTP databases and data warehosues

### Stars and Snowflakes: Schemas for Analytics

| schema    | description                                                                                                                                                                    |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| star      | when the table relationships are visualized, the fact table is in the middle, surrounded by its dimension tables; the connections to these tables are like the rays of a star. |
| snowflake | a variant of "star" schema, where dimensions are futher broken down into subdimensions.                                                                                        |
