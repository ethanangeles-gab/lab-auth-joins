# lab-auth-joins

## SQL JOIN Types (used in this project)

- **INNER JOIN**  
  Returns rows when there is a match in both tables. Only rows with related data in both tables are included in the result set.

- **LEFT JOIN** (or LEFT OUTER JOIN)  
  Returns all rows from the left table and matched rows from the right table. If there is no match, NULL values are returned for columns from the right table.

- **RIGHT JOIN** (or RIGHT OUTER JOIN)  
  Returns all rows from the right table and matched rows from the left table. If there is no match, NULL values are returned for columns from the left table.

- **FULL JOIN** (or FULL OUTER JOIN)  
  Returns rows when there is a match in one of the tables. This means it returns all rows from both tables, with NULLs in places where a row from one table does not have a matching row in the other table.

> _Note: List and explain only the JOINs you actually use in this project. Remove any JOINs from the list above that you do not use._

---

## `/api/reports` Endpoints

| Endpoint                  | Purpose / Description                                                   |
|---------------------------|-------------------------------------------------------------------------|
| `/api/reports/users`      | Returns a report of all users with related data (e.g., roles, activity) |
| `/api/reports/logins`     | Lists login history or statistics                                       |
| `/api/reports/summary`    | Provides a summary report (customized per project needs)                |
| `/api/reports/<custom>`   | [Describe what this custom report returns]                              |

> _Note: Replace the example endpoints and descriptions above with the actual endpoints implemented in your project. List all `/api/reports/*` endpoints and briefly describe their purpose._

---

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/ethanangeles-gab/lab-auth-joins.git
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the project:
   ```bash
   npm start
   ```

---

## License

MIT
