Evaluation query operator

## Table of Contents
1. [$expr](#1-expression-query)
2. [$mod](#2-modulus-query)
3. [$regex](#3-regex-query)
4. $jsonSchema
4. $text
5. $where

# 1. Expression query
```js
[{
  "category": "food",
  "budget": 500,
  "spent": 600
},
{
  "category": "pizza",
  "budget": 200,
  "spent": 150
},
{
  "category": "mango",
  "budget": 300,
  "spent": 280
},
{
  "category": "apple",
  "budget": 150,
  "spent": 120
},
{
  "category": "sup",
  "budget": 250,
  "spent": 300
}]
```
```js
//example for code   =budget < spent
use('Pratic')
db.Monthbaget.find({
    $expr:{
        $lt:["$budget","$spent"]
    }
}).toArray()
```
```js
//example for code =budget > spent
use('Pratic')
db.Monthbaget.find({
    $expr:{
        $gt:["$budget","$spent"]
    }
}).toArray()

```
# 2. Modulus query
```js
//example for code  =vakses value 0 
use('Pratic')
db.Monthbaget.find({
    budget:{$mod:[500,0]}
}.toArray()

```
# 3. Regex query
```js
//example for code  = spesifik search,name,graminphone number,robi number
use('Pratic')
db.data.find({
   name:{$regex:'018'}
}).toArray()

```
