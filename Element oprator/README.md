```sh
$exists: Matches documents that have the specified filed
$type: Selects documents if a field is of the specified type
```

```js
use( 'Shop')
db.brands. find({
country: {$exists:true}
})
```
> ## Git Branch Commands
| Command | Description |
| ----------- | ------------ |
| git branch | List branches (the asterisk denotes the current branch) |
| git branch [branch name] | Create a new branch |
| git branch -d [branch name]| Delete a branch |
| git branch [branch name] | Create a new branch |
| git checkout -b [branch name] | Create a new branch and switch to it |
| git checkout - | Switch to the branch last checked out |
| git checkout [branch name] | Switch to a branch |


```js
use( 'Shop')
db.brands. find({
salary: {$type:2}
})
```
