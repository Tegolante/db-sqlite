# db-sqlite

Welcome in the repository! This is a simple SQLite DB made for testing

### 1. Download SQLite DB Browser
Download SQL Browser from [here](https://sqlitebrowser.org/dl/)

<img width="1901" height="868" alt="image" src="https://github.com/user-attachments/assets/82008a2e-69bd-420a-a7e1-f753e3181c87" />



### 2. Open SQLite DB Browser, select Open Database and select Database.db from your folder
Open the file\

<img width="1918" height="986" alt="image" src="https://github.com/user-attachments/assets/2ff17d56-c907-4905-acc4-9e9aa604cc29" />


### 3. Have fun!

<img width="1919" height="980" alt="image" src="https://github.com/user-attachments/assets/a2f78387-4563-4015-b4ff-1996adabc857" />



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
