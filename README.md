# OceanNovels

## Migrations

**User** The user table has `username` and `email` of type `string` and a `karma` of type `integer`. 

**Post** The post table has a `title` of type string, `content` of type `text`, and a reference to a `user`

**Community** The community table has a `name` of type string

**UserCommunity** The user_communities join table has foreign key references to a `user` and a `community`. 


## Models

**Accociations**
1. A `user` can have many `user_communities` and many `communities` through `user_communities`
2. A `community` can have many `user_communities` and many `users` through `user_communities`
3. A `user` can have many posts and a `post` belongs to exactly one `user`.
4. A `user_communities` belongs to a `user` and a `community`. 


**Additional Methods**

**User**

Instance method `get_username` returns the user's `username`
Instance method `get_karma` returns the user's `karma` rating

**Community**

## Validations

**User** 
1. A username must be at least 6 characters in length
2. A username must be unique

**Community**
1. A community name must be unique