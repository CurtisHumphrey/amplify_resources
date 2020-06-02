# amplify_resources


## Working with DynamoDB

* Understanding conditions in the GraphQL calls: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Expressions.ConditionExpressions.html#Expressions.ConditionExpressions.PreventingOverwrites
* Tying changes to lambda: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.Lambda.Tutorial.html

## DynamoDB issues

```
errorType: 'DynamoDB:ValidationException'
```
This is caused by have a string field with an empty value `''`.  Replacing it with `null` seems to work if it is nullable.
