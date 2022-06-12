# til

Random tip for myself

# JS
- `null` and `undefined` are similar but behave slightly differently
```
 10 + null; // null behaves like zero
 << 10
 10 + undefined; // undefined is not a number
 << NaN
 ```
 
In general, values tend to be set to `undefined` by JavaScript, whereas values are usually set to `null` by the developer

- Only 9 values are always `false`
```
* "" // double quoted empty string literal
* '' // single quoted empty string literal
70 JavaScript: Novice to Ninja, 2nd Edition
* `` // empty template literal
* 0
* -0 // considered different to 0 by JavaScript!
* NaN
* false
* null
* undefined

```
# CSS
- `calc` for CSS
```example: calc(100%-30px) => give you the width/height of the property as you may want```

# POSTGRES
- Fix the error psql: error: FATAL:  role "postgres" does not exist

 ` createuser -s postgres `
 - Show hba
 `psql postgres  -c 'show hba_file';`
 
 - Not start server
 $ rm -rf /usr/local/var/postgres

# Install the binary
$ brew install postgresql

# init it
$ initdb /usr/local/var/postgres

# Start the PostgreSQL server
$ postgres -D /usr/local/var/postgres

# Create your database
$ createdb mydb
### HEROKU
heroku buildpacks:add heroku/nodejs -i 1 -a YOUR-APP-NAME to fix chose wrong node engine
