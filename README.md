# SpookySwap History

Check it out live: [https://fura.org/staging/spookyswap](https://fura.org/staging/spookyswap)


### Fura - SpookySwap GraphQL Endpoint
https://api.fura.org/subgraphs/name/spookyswap

### Code Configuration
change [src/apollo/client.js](https://github.com/Uniswap/uniswap-info/blob/v2/src/apollo/client.js) as follows:

```
export const client = new ApolloClient({
  link: new HttpLink({
    uri: 'https://api.fura.org/subgraphs/name/spookyswap',
  }),
  cache: new InMemoryCache(),
  shouldBatch: true,
})

export const healthClient = new ApolloClient({
  link: new HttpLink({
    uri: 'https://api.fura.org/subgraphs/name/spookyswap',
  }),
  cache: new InMemoryCache(),
  shouldBatch: true,
})

export const blockClient = new ApolloClient({
  link: new HttpLink({
    uri: 'https://api.fura.org/subgraphs/name/spookyswap',
  }),
  cache: new InMemoryCache(),
})
```

### CORS Settings
https://api.fura.org/subgraphs/name/spookyswap 

now supports:
```
localhost:3000
localhost:9528
127.0.0.1:3000
127.0.0.1:9528
info.spookyswap.finance
```

### Full Schema
check [schema.graphql](https://github.com/fura-protocol/fura-api-spookyswap/blob/main/schema.graphql)


### Use Playground
https://github.com/graphql/graphql-playground  

https://github.com/graphql/graphiql

