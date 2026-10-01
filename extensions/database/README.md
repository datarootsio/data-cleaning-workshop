# Database extension

This extension imports database data using JDBC. SQL export code lives in
[`main/src/com/google/refine/exporters/sql`](../../main/src/com/google/refine/exporters/sql).

## Adding support for a database vendor

1. Register a service in [`DatabaseService.java`](src/com/google/refine/extension/database/DatabaseService.java).
2. Provide connection and service classes; use the existing
   [PostgreSQL](src/com/google/refine/extension/database/pgsql) or
   [MySQL](src/com/google/refine/extension/database/mysql) implementations as examples.
3. Set interface defaults in [`database-source-ui.js`](module/scripts/index/database-source-ui.js).
4. Add the driver's dependency to this extension's [`pom.xml`](pom.xml), following the other database drivers.
