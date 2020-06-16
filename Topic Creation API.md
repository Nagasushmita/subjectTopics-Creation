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
                "topicNames": ["deletion"]
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
  "data": {
              "topic": {
                "topicId": "a53de7e450eb4111a2f0a34c848dcf20",
                "topicName": "python objects",
                "subjectId": 14,
                "description": null,
                "leaf": false
              },
              "subTopicsList": {
                "subTopics2List": [
                  {
                    "topicId": "8802a15a3a0d4b27a661c5dc53245d05",
                    "topicName": "insertion",
                    "parentTopicId": "6d2f8f1aa33d4b1a8076e7993a8f12fa",
                    "description": null,
                    "leaf": true
                  },
                  {
                    "topicId": "7459106061ac4a05a9e485fb2fd6b14d",
                    "topicName": "deletion",
                    "parentTopicId": "6d2f8f1aa33d4b1a8076e7993a8f12fa",
                    "description": null,
                    "leaf": true
                  },
                  {
                    "topicId": "cb6903a99bb348d08ace116cc3d879e8",
                    "topicName": "update",
                    "parentTopicId": "6d2f8f1aa33d4b1a8076e7993a8f12fa",
                    "description": null,
                    "leaf": true
                  },
                  {
                    "topicId": "156f5d31cf0f4c89a7a1f885d71bfc8d",
                    "topicName": "slicing",
                    "parentTopicId": "6d2f8f1aa33d4b1a8076e7993a8f12fa",
                    "description": null,
                    "leaf": true
                  },
                  {
                    "topicId": "58bbc86b4bd441e88efc4b641c7e8bdf",
                    "topicName": "deletion",
                    "parentTopicId": "1162f6441fc74e71b267c816258864fc",
                    "description": null,
                    "leaf": true
                  }
                ],
                "subTopics1List": [
                  {
                    "topicId": "6d2f8f1aa33d4b1a8076e7993a8f12fa",
                    "topicName": "lists",
                    "parentTopicId": "a53de7e450eb4111a2f0a34c848dcf20",
                    "description": null,
                    "leaf": false
                  },
                  {
                    "topicId": "1162f6441fc74e71b267c816258864fc",
                    "topicName": "dictionaries",
                    "parentTopicId": "a53de7e450eb4111a2f0a34c848dcf20",
                    "description": null,
                    "leaf": false
                  },
                  {
                    "topicId": "9f4757c865774fb49b5772ad4d9b9371",
                    "topicName": "tuples",
                    "parentTopicId": "a53de7e450eb4111a2f0a34c848dcf20",
                    "description": null,
                    "leaf": true
                  }
                ]
              }
            },
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





