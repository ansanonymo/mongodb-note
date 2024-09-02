# Update Operation

- [Structure to Update](#structure-to-update)
- [Example of Update](#example-of-update)
- [Remove Field Name](#remove-field-name)
- [Rename Field Name](#rename-field-name)

### Structure to Update

```js
db.<collection-name>.updateOne(
    {"condition to find"},
    {
        // update price field
        $set: { 'price' : 45 }
    }
)
```

### Example of Update

```js
db.<collection-name>.updateOne(
    {
        // update one where price 200
        price : 200
    },
    {
        // set the status to true
        $set: { 'status' :true }
    }
)

db.<collection-name>.updateMany(
    {
        // update all where price 200
        price : 200
    },
    {
        // set true
        $set: { 'status' :true }
    }
)
```

### Remove Field Name

```js
db.<collection-name>.updateOne(
    { filter },
    {
        // 1 for remove the field name
        $unset: { fieldname: 1 }
    }
)
```

### Rename Field Name

```js
db.<collection-name>.updateOne(
    { filter },
    {
        $rename: {
            "oldFieldname": "newFieldName"
        }
    }
)
```

<br />
<hr />
<br />

### [Go Back CRUD file >](./CRUD.md)

### [Go Back README file >](./README.md)
