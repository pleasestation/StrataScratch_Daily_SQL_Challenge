# Customer Interaction and Content Analysis

## Objective

This project calculates the total number of interactions and the total number of contents created for each customer. The goal is to include all interaction types (such as `click`, `view`, `like`, etc.) and content types (like `comment`, `review`, and `post`) in the calculations.

### Expected Output

The output will include the following information for each customer:
- **customer_id**: Unique identifier for the customer
- **total_interactions**: Total number of interactions for the customer
- **total_contents**: Total number of contents created by the customer

## Data

### Interactions Table
The `customer_interactions` table stores the interaction data for customers. Below is the schema for the `customer_interactions` table:

| **Column Name**         | **Data Type** | **Description**                  |
|-------------------------|---------------|----------------------------------|
| **interaction_id**       | bigint        | Unique identifier for the interaction |
| **customer_id**          | bigint        | Unique identifier for the customer |
| **interaction_type**     | text          | Type of the interaction (e.g., `click`, `view`, `like`) |
| **interaction_date**     | date          | Date when the interaction took place |

Sample data:
| interaction_id | customer_id | interaction_type | interaction_date |
|----------------|-------------|------------------|------------------|
| 1              | 7           | click            | 2024-02-13       |
| 2              | 4           | view             | 2024-01-25       |
| 3              | 8           | like             | 2024-02-18       |
| 4              | 5           | like             | 2024-01-27       |
| 5              | 7           | view             | 2024-02-28       |
| 6              | 10          | view             | 2024-02-11       |
| 7              | 3           | view             | 2024-01-28       |
| 8              | 7           | like             | 2024-02-29       |
| 9              | 8           | like             | 2024-01-16       |
| 10             | 5           | click            | 2024-01-15       |
| 11             | 4           | click            | 2024-02-16       |
| 12             | 8           | like             | 2024-02-20       |
| 13             | 8           | view             | 2024-02-13       |
| 14             | 3           | view             | 2024-02-24       |
| 15             | 6           | click            | 2024-02-21       |

### User Content Table
The `user_content` table stores the content data created by customers. Below is the schema for the `user_content` table:

| **Column Name**         | **Data Type** | **Description**                  |
|-------------------------|---------------|----------------------------------|
| **content_id**           | bigint        | Unique identifier for the content |
| **customer_id**          | bigint        | Unique identifier for the customer |
| **content_type**         | text          | Type of the content (e.g., `comment`, `review`, `post`) |
| **content_text**         | text          | The content text |

Sample data:
| content_id | customer_id | content_type | content_text                           |
|------------|-------------|--------------|----------------------------------------|
| 1          | 2           | comment      | hello world! this is a TEST.           |
| 2          | 8           | comment      | what a great day                       |
| 3          | 4           | comment      | WELCOME to the event.                  |
| 4          | 2           | comment      | e-commerce is booming.                 |
| 5          | 6           | comment      | Python is fun!!                        |
| 6          | 6           | review       | 123 numbers in text.                  |
| 7          | 10          | review       | special chars: @#$$%^&*()              |
| 8          | 4           | comment      | multiple CAPITALS here.               |
| 9          | 6           | review       | sentence. and ANOTHER sentence!       |
| 10         | 2           | post         | goodBYE!                               |

## Query to Calculate Interactions and Contents

To calculate the total number of interactions and contents for each customer, use the following SQL query:

```sql
SELECT
    i.customer_id,
    COUNT(i.interaction_id) AS total_interactions,
    COUNT(c.content_id) AS total_contents
FROM
    customer_interactions i
LEFT JOIN
    user_content c ON i.customer_id = c.customer_id
GROUP BY
    i.customer_id
ORDER BY
    i.customer_id;
