> Logical Operator->[Mongodb oprator](https://www.mongodb.com/docs/manual/reference/operator/)+[Array Query Operators](https://www.mongodb.com/docs/manual/reference/operator/query/all/)

> [json data link pratic](https://raw.githubusercontent.com/julfiker755/json/main/practice-data.json)

```sh
$all:Operator
$elemMatch :Operator
$size:Operator
```


```js
// syntax = { <field>: { $all: [ <value1> , <value2> ... ] } }
// $all Operator
db.pratic.find(
    {
       interests:{$all:[ "Gaming", "Writing", "Reading" ]
        
    } 
}) 
```
```js
// syntax ={ <field>: { $elemMatch: { <query1>, <query2>, ... } } }
// $elemMatch (query)
db.pratic.find({
   skills: { 
    $elemMatch:{
       name:"JAVASCRIPT",
       level:"Intermidiate"
    }} 
}).project({
    skills:1
})
```
```js
// syntax ={ field: { $size: 2 } }
//  size Oprator
db.pratic.find(
  { skills: { $size: 0 } })
  .project({
        skills:1
        })
```

