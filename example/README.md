# Graffiti examples

### Run

```bash
# MongoDB has to be running
# Install dependencies
cd .. && npm install && cd example && npm install
# Run all servers
npm start
# Express server listening on port 3001
# Hapi server listening on port 3002
# Koa server listening on port 3003
```
### Config
`.env`
```shell
# Default : "mongodb://localhost/graphql"
MONGO_URI="mongodb://localhost:32768/graphql"
```

### Query
```shell
{
  pets(name: "katopz") {
    id
    name
  }
}
```

### Mutation
```shell
mutation{
  addPet(input:{name:"katopz", type: "B", age: 11}) {
    viewer {
      pets(name:"katopz") {
        edges {
          node {
            id
            name
          }
        }
      }
    }
  }
}
```
