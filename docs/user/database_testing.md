# Database Testing Feature

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
</picture>

> [!TIP]
> - Use your browser's search (Ctrl+F or Cmd+F) to find specific features

## What is the Database Testing Feature?
The Database Testing Feature enables direct database interactions and validations, providing comprehensive support for both SQL and NoSQL databases through SQLAlchemy and other database drivers.

## Key Capabilities
- SQL and NoSQL database support
- Database connection management
- CRUD operations execution
- Data validation and assertions
- Query execution and result analysis
- JQ pattern support for data processing
- Secure credential management
- JSON output conversion

## Supported Databases

### SQL Databases
- SQLite
- MySQL/MariaDB
- PostgreSQL
- Microsoft SQL Server
- Oracle
- IBM DB2

### NoSQL Databases
- MongoDB
- Redis
- Cassandra
- Elasticsearch
- Graph Databases (Neo4j+)

## Database Drivers Installation

Install the required database drivers using Poetry:

| Database | Poetry Install Command |
|----------|----------------------|
| SQLAlchemy | `poetry add sqlalchemy` |
| MySQL (PyMySQL) | `poetry add pymysql` |
| MySQL (MySQL Connector) | `poetry add mysql-connector-python` |
| PostgreSQL (Psycopg2) | `poetry add psycopg2` |
| SQLite | `poetry add sqlite` |
| MSSQL (PyODBC) | `poetry add pyodbc` |
| Oracle (cx_Oracle) | `poetry add cx_oracle` |
| IBM Db2 | `poetry add ibm_db_sa` |

## Database Connection Methods

### Connection String Storage
- Store database connection strings in variables
- Implement secure credential management
- Use environment variables for sensitive information

### Database Output to JSON
Steps to convert database output to JSON:
1. Execute database query
2. Fetch results
3. Convert to Python dictionary
4. Serialize to JSON format

### Driver Support
- JDBC (Java Database Connectivity)
- ODBC (Open Database Connectivity)

## Query Language Support

- ANSI SQL v92 compliant
- Database-specific SQL dialects
- ORM query builders

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀 