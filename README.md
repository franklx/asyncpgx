# asyncpgx
Extensions for asyncpg.

Based on the [asyncpg](https://github.com/MagicStack/asyncpg) and highly inspired by the [sqlx](https://github.com/jmoiron/sqlx) 
and [sqlalchemy](https://github.com/sqlalchemy/sqlalchemy) packages

Currently WIP

## Philosophy
This is a thin wrapper on the asyncpg package. Our purpose is to provide convenient extensions to the original package.
We're trying to delegate as much work as we can to the asyncpg (basically our extension methods are high-level proxies to the underlying ones)
and make only converting job.
Original asyncpg API stays the same, you can see it in the [asyncpg documentation](https://magicstack.github.io/asyncpg/current/).

## Functionality
* methods with named parameters, i.e.
```sql
SELECT field FROM some_table WHERE id <= :id;
```
