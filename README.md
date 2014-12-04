TP-Ankiety
==========

*From server to app*
```json
{
    "errors": "None", 
    "questionnaires": [
        {
            "author": "Jan Kowalski", 
            "id": 5, 
            "points": 25, 
            "questions": [
                {
                    "answers": [
                        "Tak", 
                        "Nie"
                    ], 
                    "id": 12, 
                    "question_text": "Question 1"
                }, 
                {
                    "answers": [
                        "Odp. A", 
                        "Odp. B", 
                        "Odp. C"
                    ], 
                    "id": 13, 
                    "question_text": "Pytanie z 3 odpowiedziami"
                }
            ], 
            "timeToComplete": 10, 
            "title": "Poll 1"
        }, 
        {
            "author": "Mariusz ", 
            "id": 6, 
            "points": 12, 
            "questions": [
                {
                    "answers": [
                        "Tak", 
                        "Nie"
                    ], 
                    "id": 14, 
                    "question_text": "Czy palisz pieprosy?"
                }, 
                {
                    "answers": [
                        "MBW", 
                        "Audi", 
                        "Mercedes", 
                        "Inny"
                    ], 
                    "id": 15, 
                    "question_text": "Jaki chcesz miec samochod?"
                }
            ], 
            "timeToComplete": 5, 
            "title": "Poll 2"
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
      "id" : 0,
      "title" : "Transport Publiczny",
      "timeToComplete" : "10",
      "author" : "MPK",
      "points" : "9",
      "questions" : [
        {
          "id" : 0,
          "type" : 0,
          "body_text" : "Jesteś YOLO?",
          "answer" : 1
        },
        {
          "id" : 1,
          "type" : 0,
          "body_text" : "Joł?",
          "answer" : 0
        }
      ]
    } 
   ]
}
```
