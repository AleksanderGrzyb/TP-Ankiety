TP-Ankiety
==========

Symbols:
* SC - Single Choice
* MC - Multiple Choice
* ST - Stars
* RK - Rank

Available answers store tuples of (answer_index, answer_text).

Answers are submitted as pairs (answer_index, answer_value). Sum of values must be 1. For SC and choice 2 (answers are zero-indexed!) it will be [(0, 0), (1, 0), (2, 1), (3, 0)]. It can also be [(2, 1)]. The same goes for other questions, ie. for MC with choices 1 and 2 return [(1, 0.5), (2, 0.5)]. For ST return 1 for the selected number of stars. RK - I think best would be if 1st had 2x more value than 2nd, 4x more than third and so on.

There are max of 4 available answers, but that's only front-end restriction.

Initial  poll. Query using GET the address polls/mobile/USER_CODE/register/
You will get JSON as follows:

```json
{
    "points": 4.0,
    "poll_id": 21,
    "questions": [
        {
            "available_answers": [
                [
                    0,
                    "Male"
                ],
                [
                    1,
                    "Female"
                ],
                [
                    2,
                    ""
                ],
                [
                    3,
                    ""
                ]
            ],
            "id": 3,
            "question_type": "SC",
            "title": "What is your gender?"
        },
        {
            "available_answers": [
                [
                    0,
                    "Yes"
                ],
                [
                    1,
                    "No"
                ],
                [
                    2,
                    ""
                ],
                [
                    3,
                    ""
                ]
            ],
            "id": 4,
            "question_type": "SC",
            "title": "Do you smoke?"
        },
        {
            "available_answers": [
                [
                    0,
                    "Yes"
                ],
                [
                    1,
                    "No"
                ],
                [
                    2,
                    ""
                ],
                [
                    3,
                    ""
                ]
            ],
            "id": 5,
            "question_type": "SC",
            "title": "Are you a student?"
        },
        {
            "available_answers": [
                [
                    0,
                    "Yes"
                ],
                [
                    1,
                    "No"
                ],
                [
                    2,
                    ""
                ],
                [
                    3,
                    ""
                ]
            ],
            "id": 6,
            "question_type": "SC",
            "title": "Are you currently employed?"
        }
    ],
    "time_to_complete": 1.0
}
```

Using POST submit in a format that follows:
```json
{
    "questions": [
        {
            "answers": [
                [1, 1]
            ], 
            "id": 3
        }, 
        {
            "answers": [
                [0, 1]
            ], 
            "id": 4
        }, 
        {
            "answers": [
                [1, 1]
            ], 
            "id": 5
        }, 
        {
            "answers": [
                [1, 1]
            ],
            "id": 6
        }
    ], 
    "poll_id": 21
}
```

Successful POST gets you JSON with number of user points (field 'points').

After registration query polls/mobile/USER_CODE/getpoll/
The only difference will be that each polls will be packed in 'polls' list, so you have to deep one level deeper. At the same level as 'polls' will be the number of points (field 'points').

As a response submit one poll at a time in the same way you did with the Initiall poll.

There are points that user has (top level entry when getting list of polls) and points for each poll (at the same level as completion time for this poll).
