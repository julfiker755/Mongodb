## Table of Contents
1. [Mongobd insert](#1-mongobd-insert)
2. [Select all data](#2-mongobd-find)
3. [Row Count](#3-mongobd-row-count)
4. [sorting](#4-mongobd-sorting)
5. [limit](#5-Mongobd-limit)
6. [Select by match condition and or](#6-match-condition)
7. [Select like](#7-Select-like)
8. [select by match in](#8-Select-by-match-in)
9. [Projection](#9-Projection)


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
db.products.find((]).sort({salary:-1}) // Descending
db.products.find((}).sort({salary:1}) // Asending

//mongobd  aggregate use
db.products.aggregate ([{$sort:{salary:1}}]) //Asending
db.products.aggregate([{$sort:{salary:-1}}]) // Descending

```
# 5. Mongobd limit

```js
// Mongobd limit
db.Monthbaget.find({}).limit(2)
//Mongobd aggregate  use
db.Monthbaget.aggregate([
{$limit:3}
])

```

# 6. Match condition

```js
// Select by match condition and or

db.employee.find({
    $and: [
        {salary: {$gt:40000}},
        {city: 'Dhaka'},
        ]
})


// Mongobd aggregate use
db.employee.aggregate(
[
{$match: {salary:{$gt:40000}}}, 
{$match:{city: "Dhaka"}}
]
)

// nested use --
db.employee.aggregate([
{$match: {$and: [
        {salary: {$gt:40000}},
        {city: 'Dhaka'},
 ]}}
])

db.employee.aggregate([
{$match: {$or: [
        {salary: {$gt:40000}},
        {city: 'Dhaka'},
 ]}}
])

```

# 7. Select like

```js
// Select like
db.employee.find({designation:/Engineer/})


// Mongobd aggregate use
db.employee.aggregate([
{$match: {designation:/Engineer/}}
])
```
# 8. Select by match in

```js
// Select by match in
db.products.find({name: ($in: ['Rabbil', 'Rain']}})

//Mongobd aggregate use
db.products.aggregate ( [
{$match: {name: {$in:["Rabbil","Rain"]}}}

])
```
# 9. Projection

```js
//  Projection
const options = {
      sort: { "imdb.rating": -1 },
      projection: { _id: 0, title: 1, imdb: 1 },
    };

db.products.find({},options)
db.products.find({},{_id: 0, name: 1, designation: 1})

//Mongobd aggregate use
db.employee.aggregate([
{$project: {_id: 0, name: 1, designation: 1}}
])

```
