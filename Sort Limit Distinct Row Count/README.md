>  Sort Limit Distinct Row Count

```js
// Ascending
db.data.find().sort({
    price:1
})
```

```js
// Descending
db.data.find().sort({
    price:-1
})
```
```js
// total count data
db.data.find().count('total')
const result=await  database.estimatedDocumentCount()
```
```js
// all data fast 2 data limt
db.data.find().limit(2)
// all data last 2 data limt
db.data.find().sort({_id:-1}).limit(2)
```
```js
use('Pratic')
db.Monthbaget.distinct("_id")
```

