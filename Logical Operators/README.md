> Logical Operator->[Mongodb oprator](https://www.mongodb.com/docs/manual/reference/operator/)+[Logical Operator](https://www.mongodb.com/docs/manual/reference/operator/query-logical/)

> [json data link pratic](https://raw.githubusercontent.com/julfiker755/json/main/practice-data.json)

```sh
$and:Operator
$or:Operator

```

```js
// $and Operator
db.pratic.find({
    $and:[
      {gender :"Female"},
      {age :{$lt:30}},
      {"skills.name":"JAVASCRIPT"}
   ]
}).project({
    gender:1,
    age:1,
    "skills.name":1
})
```
```js
// $or Operator
db.pratic.find({
    $or:[
      {gender :"Female"},
      {age :{$lt:30}},
      {"skills.name":"JAVASCRIPT"}
   ]
}).project({
    gender:1,
    age:1,
    "skills.name":1
})

// example code
// 
db.pratic.find({"skills.name":{$in:["JAVASCRIPT","PYTHON"]}})

```