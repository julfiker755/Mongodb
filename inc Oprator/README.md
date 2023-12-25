>[$inc](https://www.mongodb.com/docs/current/reference/operator/update/inc/)

> [json data link pratic](https://raw.githubusercontent.com/julfiker755/json/main/practice-data.json)



```js
// $inc Oprator
// increment 
db.pratic.updateOne(
    {_id:new ObjectId("658914c63e9d899f3a38d1e7")},
     { $inc: {age:1} }
    )
//decrement
db.pratic.updateOne(
    {_id:new ObjectId("658914c63e9d899f3a38d1e7")},
     { $inc: {age:-1} }
    )   

```

```js

{
	"_id" : ObjectId("658914c63e9d899f3a38d1e7"),
	"name" : {
		"firstName" : "Wit",
		"lastName" : ""
	},
	"ipAddress" : "191.86.74.88",
	"city" : "graminphone",
	"emails" : "weffnert2r@networkadvertising.org"
}
// this josn data email key chnage for easy example
db.pratic.updateMany({},{ $rename: { 'email': 'emails'} })
```


