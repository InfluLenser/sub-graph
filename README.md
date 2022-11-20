# Subgraph for TalentLayer

https://docs.indie.talentlayer.org/developers/graph-schema

https://docs.indie.talentlayer.org/developers/local-environment-setup

### GraphiQL request example

```graphql
{
  proposals {
    id
    createdAt
    updatedAt
    status
    uri
    rateToken {
      id
      name
      address
      decimals
    }
    rateAmount
    service {
      id
      buyer {
        handle
      }
    }
  }
  users(orderBy: id, orderDirection: desc) {
    id
    address
    uri
    handle
    withPoh
  }
  services {
    id
    createdAt
    updatedAt
    status
    proposals {
      id
      status
      rateAmount
      rateToken {
        id
        name
      }
      seller {
        handle
      }
    }
  }
  payments {
    id
    rateToken {
      decimals
      id
      name
      address
    }
  }
}
```
