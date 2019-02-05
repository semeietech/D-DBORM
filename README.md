# D³DBORM

A evolution step over dynamodborm. The dynamodborm will import this project adding settings and dependencys.
```js
import D3ORMFactory from 'domaindborm'
import dynamodbcclient from 'aws-sdk' // a example call
import dynamodbdatamapper from '@aws/dynamodb-data-mapper'

const dynamodbormFactory = new D3ORMFactory( dynamodbclient, dynamodbdatamapper)

export const AggregationRoot = dynamodbormFactory.createAggregationRoot({
    organization: '@spark',
    prefix: 'domain',
})
export const BaseModel = dynamodbormFactory.createBaseModel()
export const appendCustomMethods = dynamodbormFactory.createAppendCustomMethods()
```

## Features

Plug and Play anothers db's besides dynamodb to have a fullfeature orm.

- Migration
   - schema migration
   - migration de dados
   - rollback
   - deploy
   - target migration

- Version Attribute lock
- query language
