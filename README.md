# Strapi application

#install

yarn install

#start

NODE_ENV=production yarn start


#API

endpoint: http://localhost:1337/graphql


## login
```
mutation {
  login(input: { identifier: "email", password: "password" }) {
    jwt
  }
}
```

and for other requests add http header
```
{
  "Authorization": "Bearer <jwt>"
}
```

example request:
```
{
  me {
    id,
    username,
    email
  }
}
```

