```sh
$exists: Matches documents that have the specified filed
$type: Selects documents if a field is of the specified type
```

```js
use( 'Shop')
db.brands. find({
country: {$exists:true}
})
```
> ## Git Branch Commands
| Type | Number | Alias
| ----------- | ------------ | ------------ | 
| Double | 1 | "double" |
| String | 2 | "string" |
| Object | 3 | "object" |
| Binary data  | 5 | "binData" |
| ObjectId | 7 | "objectId" |
| Boolean | 8 | "bool" |
| Date | 9 | "date" |
| Null | 10 | "null" |
| Regular Expression | 11 | "regex" |
| 32-bit integer | 16 | "int" |
| Timestamp | 17 | "timestamp" |
| 64-bit integer | 18 | "long" |
| Decimal128 | 19 | "decimal" |



```js
use( 'Shop')
db.brands. find({
salary: {$type:2}
})
```
