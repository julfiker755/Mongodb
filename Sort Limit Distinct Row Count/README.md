>  Sort Limit Distinct Row Count

```js
use('Pratic')
// Ascending
db.data.find().sort({
    price:1
})
```

```js
use('Pratic')
// Descending
db.data.find().sort({
    price:-1
})
```
```js
use('Pratic')
// total count data
db.data.find().count('total')
  const result=await  database.estimatedDocumentCount()
```
