> Comparison Query Operator

 [$in: In Operator](#1$in:-In-Operator)
$nin: Not In Operator
$eq:Equal to Operator
$ne: Not Squal Ta Operater
$gt: Greater Than Operator
$gte: Greater Than or Equal To Operator
$lt: Less Than Operator
$lte:Less Than or Equel To Operetor


## 1. $in: In Operator

```js
db.employee.find(
    {
        salary:{$in:[4000,500,600]}
    }
)
```
```js
// $nin: Not In Operator
db.employee.find(
    {
        salary:{$nin:[4000,500,600]}
    }
)
```

```js
// $eq:Equal to Operator
db.employee.find(
    {
        salary:{$eq:4000}
    }
)
```
```js
// $ne: Not Squal Ta Operater
db.employee.find(
    {
        salary:{$nc:4000}
    }
)
```
```js
// $gt: Greater Than Operator
db.employee.find(
    {
        salary:{$gt:400}
    }
)
```
```js
//  $gte: Greater Than or Equal To Operator
db.employee.find(
    {
        salary:{$gte:400}
    }
)
```
```js
//  $lt: Less Than Operator
db.employee.find(
    {
        salary:{$lt:400}
    }
)
```
```js
//  $lte:Less Than or Equel To Operetor
db.employee.find(
    {
        salary:{$lte:400}
    }
)
```
