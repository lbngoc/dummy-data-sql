Generate random test data for MySQL using routines

# Files

1. Download the sql code: `populate_dummy_data.sql`.
2. Download sql for generating random data for foreign-key dependent child tables: `populate_fk.sql`

## Install

```bash
mysql -uUSER -pPASSWORD DATABASE_NAME < populate_dummy_data.sql
mysql -uUSER -pPASSWORD DATABASE_NAME < populate_fk.sql
```

## Usage

- Run this SQL query

```sql
call populate('DATABASE-NAME','TABLE-NAME',NUMBER-OF-ROWS,DEBUG-MODE);
```
- `DEBUG-MODE` ('Y','N') will print an SQL that's executed and iterated.


## Example

To generate test data of `1000` rows for `sakila`.`film` table execute following sql command:

```sql
call populate('sakila','film',1000,'N');
```

## Author

- [Kedar Vaijanapurkar](http://kedar.nitty-witty.com/blog/generate-random-test-data-for-mysql-using-routines)
- Editted by [Ngoc-LB](http://ngoclb.com)
