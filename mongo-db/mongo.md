# Mongo DB

## Commands

### Please note that semicolon is optional while issuing commands.

### `View all databases`

```
show dbs
```
### `Create a new database`

```
use <newdatabasename>
```

### `Show current db name`

```
db
```
### `Delete Database`

```v
db.dropDatabase()
```

### `Show Collections`

```
show collections
```

### `Create a New Collection`

```vim
db.createCollection('CollectionName')
```

### `Delete an Existing Collection`

```vim
db.collectionName.drop()
```

## MongoDB Commands for Rows

### Insert One Row
```json
db.collectionName.insert({
    'name' : "Rashid",
    'age': 22,
    'language' : "Urdu",
})
```

### Insert Multiple Rows
```json
db.collectionName.insert([{
    'name' : "Rashid",
    'age': 22,
    'language' : "Urdu",
},
{
    'name' : "Wajid",
    'age': 12,
    'language' : "English",
},
])
```