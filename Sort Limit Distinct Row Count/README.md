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
