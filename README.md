TP-Ankiety
==========

*From server to app*
```json
{
    "errors": "None", 
    "questionnaires": [
        {
            "author": "Nowakowski", 
            "id": 4, 
            "points": 12, 
            "questions": [
                {
                    "answers": [
                        "Answer 1", 
                        "Answer 2", 
                        "Answer 3"
                    ], 
                    "id": 7, 
                    "question_text": "Single Choice Question #1", 
                    "type": "singlechoice"
                }, 
                {
                    "id": 3, 
                    "question_text": "How do you rate our service?", 
                    "type": "stars"
                }
            ], 
            "timeToComplete": 25, 
            "title": ""
        }
    ]
}
```

*From app to server*

Wysyłam ankiety, na które użytkownik odpowiedział. W tym przypadku odpowiedział na ankietę z id = 0.

```json
{
  "questionnaires" : [
    {
      "id" : 4,
      "questions" : [
        {
          "id" : 7,
          "type" : "singlechoice",
          "answer" : 1
        },
        {
          "id" : 3,
          "type" : "stars",
          "answer" : 5
        }
      ]
    } 
   ]
}
```
