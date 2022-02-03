# json-server practice

## Resources
- Users
- Tweets
- Comments

## Relationships
A user has many comments and many tweets
A tweet belongs to a user and has many comments (tweet holds **userId** key)
A comment belongs to a user and also belongs to a tweet (comment holds **userId** and **tweetId** key)

## Query magic

### Get a tweet with its user info and comments
`http://localhost:3000/tweets/1?_embed=comments&_expand=user`

### Get a user with all their tweets and comments
`http://localhost:3000/users/3?_embed=tweets&_embed=comments`

### Get a comments with user info and tweet info
`http://localhost:3000/comments/1?_expand=tweet&_expand=user`

[Official json-server docs](https://github.com/typicode/json-server#relationships)
