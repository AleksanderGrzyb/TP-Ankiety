TP-Ankiety
==========

*From server to app*
```
{
  "questionnaires" : [
    {
      "id" : 0,
      "questions" : [
        {
          "id" : 0,
          "type" : 0,
          "body_text" : "Jesteś YOLO?"
        },
        {
          "id" : 1,
          "type" : 0,
          "body_text" : "Joł?"
        }
      ]
    }, 
    {
      "id" : 1,
      "questions" : [
        {
          "id" : 0,
          "type" : 0,
          "body_text" : "Browar?"
        }
      ]
    }]
}
```

*From app to server*

Wysyłam ankiety, na które użytkownik odpowiedział. W tym przypadku odpowiedział na ankietę z id = 0.
```
{
  "questionnaires" : [
    {
      "id" : 0,
      "questions" : [
        {
          "id" : 0,
          "type" : 0,
          "body_text" : "Jesteś YOLO?"
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
