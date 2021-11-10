# API SPEC

## Route: `/api/question/similar`
**Get similar questions based on given question**
**Method**: GET   

**Query Params**:
* id: String   
* title: String
* description: String

**Authentication**:    
  * In header
	* key: “Authorization”
	* value: “Token {your api key}”

**Return**:    
  * list of object with id, title, description:    
```
[ 
    {
	id: String,
	title: String,
	description: String,
    }
]
```

## Example:
	
```
curl 'localhost:8000/api/question/similar/?id=13377&title=whatiscassava&description=whatiscassava' \
-H 'Authorization: Token b67c1fbcec60cc0610e5d949c5b0775065942214'
```

**Result**:

```
[
    {
        "id": "1",
        "title": "title_test",
        "description": "description_test"
    },
    {
        "id": "2",
        "title": "title_test",
        "description": "description_test"
    },
    {
        "id": "3",
        "title": "title_test",
        "description": "description_test"
    },
    {
        "id": "4",
        "title": "title_test",
        "description": "description_test"
    }
]
```
