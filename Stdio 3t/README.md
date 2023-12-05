## Table of Contents
1. [Mongobd insert](#1-mongobd-insert)
2. [Select all data](#2-mongobd-find)
3. [Row Count](#3-mongobd-row-count)
4. [sorting](#4-mongobd-sorting)


# 1. Mongobd insert

```js
// Mongobd insert/insertone/insertMany

db.food.insertOne({
    name:"Julfiker",
    age:33,
});
db.foods.insertMany({[
    {name:'Julfiker',age:44}
    {name:'jim',age:47}
]})

```
# 2. Mongobd find

```js
// Mongobd find/aggregate

db.barand.find({})
db.barand.find({}).toArray()
db.barand.aggregate([])

```

# 3. Mongobd Row Count

```js
// Mongobd find/aggregate row count

db.barand.estimatedDocumentCount()
db.barand.find({}).count('total')
// mongobd  aggregate use
db.barand.aggregate([
{$count:'total'}
])

```
# 4. Mongobd Sorting

```js
//Mongobd sorting

```
