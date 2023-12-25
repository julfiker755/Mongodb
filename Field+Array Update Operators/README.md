>[Update Operators](https://www.mongodb.com/docs/manual/reference/operator/update/)+[Field Update Operators](https://www.mongodb.com/docs/manual/reference/operator/update-field/)
+[Array Update Operators](https://www.mongodb.com/docs/manual/reference/operator/update-array/)

> [json data link pratic](https://raw.githubusercontent.com/julfiker755/json/main/practice-data.json)




```js
// NB:  city takble replace hobe / nah takle add hobe
// Field Update Operators----------$set:Operator
db.pratic.updateOne(
    {_id:new ObjectId("658914c63e9d899f3a38d1e7")},
     {
     $set:{
        city:'nai'
     }
     }
    )
```

```js
// Array Update Operators----------addToSet:Operator
db.pratic.updateOne(
    {_id:new ObjectId("658914c63e9d899f3a38d1e7")},
     {$addToSet:{
         languages:{$each:["tamil","oudu"]}
     }}
    )
```
