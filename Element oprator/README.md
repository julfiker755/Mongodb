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
```js
use( 'Shop')
db.brands. find({
salary: {$type:2}
})
```
