## Update DB with entity changes:

### Database updates with the Maven liquibase:diff goal 
If you have choosen to use MySQL, MariaDB or PostgreSQL in development, you can use the `./mvnw liquibase:diff` goal to automatically generate a changelog.

If you are running H2 with disk-based persistence, this workflow is not yet working perfectly, but you can start trying to use it (and send us feedback!).

Liquibase Hibernate is a Maven plugin that is configured in your pom.xml, and is independant from your Spring application.yml file, so if you have changed the default settings (for example, changed the database password), you need to modify both files.

Here is the development workflow:


- Modify your JPA entity (add a field, a relationship, etc.)
- Compile your application (this works on the compiled Java code, so don’t forget to compile!)
- Run `./mvnw liquibase:diff` (or `./mvnw compile liquibase:diff` to compile before)
- A new “change log” is created in your `src/main/resources/config/liquibase/changelog` directory
- Review this change log and add it to your `src/main/resources/config/liquibase/master.xml` file, so it is applied the next time you run your application
