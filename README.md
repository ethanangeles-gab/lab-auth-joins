# lab-auth-joins

A Node.js/MySQL reference project demonstrating various SQL JOIN types with practical API examples for authentication, user management, and reporting.

---

## SQL JOIN Types (used in this project)

- **INNER JOIN:**  
  Returns rows when there is a match in both tables. Only rows with related data in both tables are included in the result set.  
  _Example: Reporting users and their assigned roles._

- **LEFT JOIN (LEFT OUTER JOIN):**  
  Returns all rows from the left table and matched rows from the right table. If there is no match, NULL values are returned for columns from the right table.  
  _Example: Listing all users, with profile details if available._

- **RIGHT JOIN (RIGHT OUTER JOIN):**  
  Returns all rows from the right table and matched rows from the left table. If there is no match, NULL values are returned for columns from the left table.  
  _Example: Listing all roles, with users if assigned._

- **FULL OUTER JOIN (emulated):**  
  Returns all rows from both tables, with NULLs in places where a row from one table does not have a matching row in the other table.  
  _Example: Combining users and profiles, showing all entries from both sides._

- **CROSS JOIN:**  
  Returns the Cartesian product of the two tables. Every row from the first table is joined with all rows of the second table.  
  _Example: All possible combinations of users and roles._

- **SELF JOIN:**  
  A table is joined with itself.  
  _Example: Reporting user referrals (who referred whom)._

---

## `/api/reports` Endpoints

| Endpoint                              | Purpose / Description                                                                 |
|----------------------------------------|---------------------------------------------------------------------------------------|
| `/api/reports/users-with-roles`        | List all users with their roles. (Uses INNER JOIN)                                    |
| `/api/reports/users-with-profiles`     | List all users with their profile info (if any). (Uses LEFT JOIN)                     |
| `/api/reports/roles-right-join`        | List all roles, showing users assigned to them (if any). (Uses RIGHT JOIN)            |
| `/api/reports/profiles-full-outer`     | List users and profiles, including those without matches on either side. (FULL OUTER) |
| `/api/reports/user-role-combos`        | All possible user-role combinations. (Uses CROSS JOIN)                                |
| `/api/reports/referrals`               | Show user referrals: who referred whom. (Uses SELF JOIN/INNER JOIN)                   |
| `/api/reports/latest-login`            | Show the latest login for every user, including those who never logged in. (LEFT JOIN + subquery) |

All endpoints require authentication (Bearer token in `Authorization` header).

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
3. Set up your `.env` for MySQL and JWT configs.
4. Run the project:
   ```bash
   npm start
   ```

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for improvements or bug fixes.

## License

This project is licensed under the MIT License.

---

**Author:** [ethanangeles-gab](https://github.com/ethanangeles-gab)
