# OOP PHP PDO CRUD API
 A simple crud api  endpoints in php using pdo 
 
 ## Project Structure
 
├─ api/

├─── config/

├────── database.php - file used for connecting to the database.

├─── objects/

├────── product.php - contains properties and methods for "product" database queries.

├────── category.php - contains properties and methods for "category" database queries.

├─── product/

├────── create.php - file that will accept posted product data to be saved to database.

├────── delete.php - file that will accept a product ID to delete a database record.

├────── read.php - file that will output JSON data based from "products" database records.

├────── read_one.php - file that will accept product ID to read a record from the database.

├────── update.php - file that will accept a product ID to update a database record.

├────── search.php - file that will accept keywords parameter to search "products" database.

├─── category/

├────── read.php - file that will output JSON data based from "categories" database records.

## Set up the database
Using PhpMyAdmin, create a new `php_api` database. Yes,`php_api` is the database name. After that, run the following SQL queries in the `requirement.txt` file  to create new tables with sample data.

## Output/test data
You need to use POSTMAN to test our API. Download your version of POSTMAN [here](https://www.getpostman.com/downloads/
).

Launch POSTMAN. Enter the following as the request URL.

- To read the data using the `GET`  request method
http://localhost/api/product/read.php

- To add data using the `POST`  request method
http://localhost/api/product/create.php

**Sample data :**
"""
{
    "name" : "Amazing Pillow 2.0",
    "price" : "199",
    "description" : "The best pillow for amazing programmers.",
    "category_id" : 2,
    "created" : "2018-06-01 00:35:07"
}
"""

- To read one particular record using the `GET`  request method
`http://localhost/api/product/read_one.php?id=1`


- To delete one particular record using the `POST`  request method
`http://localhost/api/product/delete.php?id=1`

- To update one particular record using the `POST`  request method
`http://localhost/api/product/update.php`


- To read one particular record in the category using the `POST`  request method
`http://localhost/api/category/read.php`
