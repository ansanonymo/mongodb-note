# Read Operation

- [Reading document](#reading-document)
- [Comparison operators](#comparison-operators)
- [Logical operators](#logical-operators)

### Reading Document

```js
// if find more than one, reatun a array of object
db.<collection-name>.find({key: value})

// return obj, if not find then return null
db.<collection-name>.findOne({key: value})
```

## Comparison Operators

| Operator | Operator Symbo | Operator | Operator Symbo |
| -------- | -------------- | -------- | -------------- |
| $eq      | ==             | $ne      | !=             |
| $gt      | >              | $gte     | >=             |
| $lt      | <              | $lte     | <=             |
| $in      | in             | $nin     | not in         |

<br />

**use structure :**

```js
db.<collection-name>.find(
    {
        filedName: { $operator: value }
    }
)
```

**Example :**

```js
db.<collection-name>.find(
    {
        price: { $eq: 600 }
    }
)

db.<collection-name>.find(
    {
        price: { $in: [200,300,560,600] }
    }
)
```

## Logical Operators

| Operator | Symbol to Compare in Programming Lanuage |
| -------- | ---------------------------------------- |
| $and     | &&                                       |
| $or      | \|\|                                     |
| $not     | !                                        |
| $nor     | ^                                        |

<br /><br />

**Structure :**

```js
{
    $and: [{ condition-1 }, { condition-2 },….]
}

{
    field: {$not : { operator : value }}
}
```

**Example :**

```js
db.<collection-name>.find(
    {
        $and: [
            { price: {$gt: 100} },
            { name: 'something' }
        ]
    }
).

db.<collection-name>.find(
    {
        $nor: [
            { 'price' : 200 },
            { 'name' : 'something' }
        ]
    }
)

db.<collection-name>.find(
    {
        $nor: [
            { 'price' : { $gt: 300 } },
            {'name' : 'something' }
        ]
    }
)
```

<hr />
<br />
<hr />

### [Go Back CRUD file >](./CRUD.md)

### [Go Back README file >](./README.md)
