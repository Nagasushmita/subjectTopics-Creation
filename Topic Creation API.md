# subjectTopics-Creation API

**URL**

_https://cat.nineleaps.com/topic/api/v1/admin/addTopic_

**Method**

POST

**Headers**

_accessToken_

**RequestBody**

```json
{
	 "subjectId": 14,
         "topicName": "python objects",
         "isLeaf": false,
         "subTopicsList": [
            {
                "topicName": "lists",
                "isLeaf": false,
                "topicNames": ["insertion", "deletion", "update", "slicing"]
            },
            {
                "topicName": "dictionaries",
                "isLeaf": false,
                "topicNames": ["deletion", "built-in-functions"]
            },
            {
                "topicName": "tuples",
                "isLeaf": true,
                "topicNames": []
            }
        ]
}
```

**Success Response:**

```json
{
  "status": "success",
  "data": null,
  "message": "successfully created topics"
}
```

**Internal Server Error:**

```json
{
  "status": "error",
  "data": null,
  "message": "Database server down"
}
```





