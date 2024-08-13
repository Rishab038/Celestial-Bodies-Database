
# Universe Database Project

## Instructions

To begin, log in to PostgreSQL using the following command:

```bash
psql --username=freecodecamp --dbname=postgres
```

Once logged in, create your database and work through the tests below to complete the project. Remember to enjoy the process and get creative with your database design!

**Be sure to connect to your database after creating it** 😄

Consider using the following ideas for column and table names: `description`, `has_life`, `is_spherical`, `age_in_millions_of_years`, `planet_types`, `galaxy_types`, `distance_from_earth`.

### Notes:
If you exit your virtual machine, your database might not be saved. You can back it up by running the following command:

```bash
pg_dump -cC --inserts -U freecodecamp universe > universe.sql
```

This will save the necessary commands to rebuild your database in a file named `universe.sql`. The file will be saved in the directory where you ran the command. If you save it inside the `project` folder, it will be preserved in the VM. You can restore your database by running:

```bash
psql -U postgres < universe.sql
```

Run this in a terminal where the `.sql` file is located.

If you're saving your progress on [freeCodeCamp.org](https://www.freecodecamp.org/), after passing all tests, save a dump of your database as described above. Upload the `universe.sql` file to a public repository and submit the URL on [freeCodeCamp.org](https://www.freecodecamp.org/).

### CodeRoad Requirements:
1. **Create a database** named `universe`.
2. **Connect to your database** with `\c universe`. Then, create the following tables: `galaxy`, `star`, `planet`, and `moon`.
3. Each table should have a **primary key**.
4. Each **primary key** should automatically increment.
5. Each table should have a **name** column.
6. Use the **INT** data type for at least two columns that aren't primary or foreign keys.
7. Use the **NUMERIC** data type at least once.
8. Use the **TEXT** data type at least once.
9. Use the **BOOLEAN** data type on at least two columns.
10. Each `star` should have a **foreign key** referencing a row in the `galaxy` table.
11. Each `planet` should have a **foreign key** referencing a row in the `star` table.
12. Each `moon` should have a **foreign key** referencing a row in the `planet` table.
13. Your database should include at least **five tables**.
14. Each table should have at least **three rows**.
15. The `galaxy` and `star` tables should each have at least **six rows**.
16. The `planet` table should have at least **12 rows**.
17. The `moon` table should have at least **20 rows**.
18. Each table should have at least **three columns**.
19. The `galaxy`, `star`, `planet`, and `moon` tables should each have at least **five columns**.
20. At least two columns per table should be **non-NULL**.
21. At least one column per table should be **UNIQUE**.
22. All columns named `name` should be of type **VARCHAR**.
23. Each **primary key** column should be named in the format `table_name_id` (e.g., the `moon` table should have a primary key named `moon_id`).
24. Each **foreign key** column should have the same name as the column it references.
