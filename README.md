# db-sqlite

Welcome in the repository! This is a simple SQLite DB made for testing

### 1. Download SQLite DB Browser
Download SQL Browser from [here](https://sqlitebrowser.org/dl/)

<img width="1911" height="856" alt="image" src="https://github.com/user-attachments/assets/abfc9af5-b21b-40e0-b4bb-3afa19c9a6ea" />






### 2. Open SQLite DB Browser, select Open Database and select Database.db from your folder
Open the file\

<img width="1919" height="992" alt="image" src="https://github.com/user-attachments/assets/d9fdc681-d61f-41e1-bfac-68c2ef42d2bc" />

<img width="1919" height="988" alt="image" src="https://github.com/user-attachments/assets/9423f805-fb56-4727-a947-697080c47966" />








### 3. Have fun!

<img width="1919" height="984" alt="image" src="https://github.com/user-attachments/assets/51622f53-3225-4356-a1c7-ceacec95ba47" />




### 3.5 Some queries for you 

**--INSERT a record**\
`INSERT INTO table (prop1, prop2, prop3) VALUES (1, 'Insert your title', 'Insert your subtitle');`

**-- DELETE a record**\
`DELETE FROM tabella WHERE tabella.proprietà = 1`

**-- UPDATE the property of a record**\
`UPDATE posts
SET text = 'Come gestire il budget personale'
WHERE id = 5;`

**-- SELECT all data from a table**\
`SELECT * FROM authors`\
`SELECT * FROM categories`\
`SELECT * FROM posts`\
`SELECT * FROM roles`


**-- SELECT and JOIN**\
`SELECT * FROM posts
LEFT JOIN authors ON posts.author = authors.id`

**-- SELECT record with JOIN**\
`SELECT 
    posts.text AS title,
    posts.subtitle AS subtitle,
    authors.username AS author,
    categories.name AS categories
FROM posts
LEFT JOIN authors ON posts.author = authors.id
LEFT JOIN posts_categories ON posts.id = posts_categories.id_post
LEFT JOIN categories ON posts_categories.id_category = categories.id;`

**-- SELECT record with some specification and JOIN**\
`SELECT 
    posts.text AS title,
    posts.subtitle AS subtitle,
    authors.username AS author,
    categories.name AS categories
FROM posts
LEFT JOIN authors ON posts.author = authors.id
LEFT JOIN posts_categories ON posts.id = posts_categories.id_post
LEFT JOIN categories ON posts_categories.id_category = categories.id
WHERE posts.title = 'Number One post';`

**-- Some modifications that you can add at your queries**\
`LIMIT 5 //limit number of results`\
`WHERE table.property //select specific record`\
`AND condition OR condition  //condition`

**-- Relationship to remember**\
One to Many\
Many to One\
Many to Many
