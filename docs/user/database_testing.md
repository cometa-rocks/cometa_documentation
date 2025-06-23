# SQLAlchemy Database Support and Connection Guide

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://raw.githubusercontent.com/cometa-rocks/cometa_documentation/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
</picture>

> [!TIP]
> - Use your browser's search (Ctrl+F or Cmd+F) to find specific features

## What is SQLAlchemy Database Support?
SQLAlchemy is a powerful Python library that provides an Object Relational Mapper (ORM) and low-level SQL execution support for various relational databases. It supports SQL-92 as well as newer SQL standards.

## Key Capabilities
- SQL-92 compliant database support
- Object Relational Mapping (ORM)
- Low-level SQL execution
- Multiple database driver support
- Connection string management
- Query building and execution
- Transaction management
- Schema management

## Supported Standards

### SQL Databases
| Database | SQL-92 Support | SQLAlchemy Driver |
|----------|---------------|-------------------|
| MySQL | Yes | `mysql+pymysql://` or `mysql+mysqlconnector://` |
| PostgreSQL | Yes | `postgresql+psycopg2://` |
| SQLite | Yes | `sqlite:///database.db` |
| Microsoft SQL Server | Yes | `mssql+pyodbc://` |
| Oracle | Yes | `oracle+cx_oracle://` |
| MariaDB | Yes | `mysql+pymysql://` |
| IBM Db2 | Yes | `ibm_db_sa://` |

## Testing Categories

### Core Installation
```sh
pip install sqlalchemy
```

### Database Drivers
```sh
pip install pymysql                # MySQL / MariaDB
pip install psycopg2                # PostgreSQL
pip install pyodbc                  # MSSQL (Microsoft SQL Server)
pip install cx_Oracle                # Oracle
pip install ibm_db_sa                # IBM Db2
```

## Implementation Methods

### MySQL / MariaDB
```python
from sqlalchemy import create_engine

# Using PyMySQL driver (Recommended)
engine = create_engine("mysql+pymysql://testuser:testpassword@localhost/testdb")

# OR using MySQL Connector
engine = create_engine("mysql+mysqlconnector://testuser:testpassword@localhost/testdb")

with engine.connect() as conn:
    result = conn.execute("SELECT * FROM users;")
    print(result.fetchall())
```
Works with MySQL and MariaDB (SQL-92 compliant).

### PostgreSQL
```python
engine = create_engine("postgresql+psycopg2://testuser:testpassword@localhost/testdb")
```
PostgreSQL supports SQL-92 and newer features like JSON storage, window functions.

### SQLite (Lightweight, No Server Needed)
```python
engine = create_engine("sqlite:///mydatabase.db")
```
Good for local testing, fully supports SQL-92 but lacks advanced features like `RIGHT JOIN`.

### Microsoft SQL Server (MSSQL)
```python
engine = create_engine("mssql+pyodbc://testuser:testpassword@localhost/testdb?driver=SQL+Server")
```
MSSQL supports SQL-92 and extensions like `TOP` (instead of `LIMIT`).

### Oracle Database
```python
engine = create_engine("oracle+cx_oracle://testuser:testpassword@localhost:1521/orcl")
```
Oracle follows SQL-92 but has proprietary syntax like `ROWNUM` instead of `LIMIT`.

### IBM Db2
```python
engine = create_engine("ibm_db_sa://testuser:testpassword@localhost/testdb")
```
IBM Db2 is SQL-92 compliant with additional OLAP features.

## Reporting and Analysis

### SQL-92 Compatibility
If you need SQL-92 compatibility, MySQL, PostgreSQL, SQLite, and SQL Server are good choices.
For enterprise solutions, PostgreSQL, MSSQL, and Oracle offer more features.
For lightweight development, use SQLite (no installation required).

## Integration Capabilities

### Final Thoughts
SQLAlchemy supports almost every relational database, whether SQL-92 compliant or newer.

Would you like help choosing a database or setting up ORM models in SQLAlchemy?

## Need Help?

### Where can I get help?
- Join our [Discord community](https://discord.gg/PUxt5bsRej)
- Contact us at [tec_dev@cometa.rocks](mailto:tec_dev@cometa.rocks)

Happy testing! 🚀