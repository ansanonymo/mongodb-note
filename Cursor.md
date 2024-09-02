# Cursor Methods

| Cursor name | Use for                          |
| ----------- | -------------------------------- |
| count()     | return total find                |
| limit()     | limit the array of "find" method |
| skip()      | skip some object from starting   |
| sort()      | sort the array of "find" method  |

<br />
<br />

```js
db.<collection-name>.find().count()

db.<collection-name>.find().limit(5)

db.<collection-name>.find().limit(5).skip(2)


db.<collection-name>.find().limit(5).sort(
    {
        price:1
        // 1 for ascending, -1 for descending
    }
)
```

<br />
<hr />
<br />

### [Go Back CRUD file >](./CRUD.md)

### [Go Back README file >](./README.md)
