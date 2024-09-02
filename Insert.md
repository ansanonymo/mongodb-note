# Insert

### Insert One

```js
db.<collection-name>.insertOne(
    {
        key1: value1,
        key2: value2,
    }
);
```

### Insert Many

```js
db.<collection-name>.insertMany([
    {
        …object
    },
    {
        …object
    }
]);
```

### Ordered and Unordered Inserts:

> 🔴 By Default, behaviors is ordered. True. insert till errors.

```js
db.<collection-name>.insertMany(
    [obj1,obj2,….],
    {ordered: false}
)
```

<br />
<hr />
<br />

### [Go Back CRUD file >](./CRUD.md)

### [Go Back README file >](./README.md)
