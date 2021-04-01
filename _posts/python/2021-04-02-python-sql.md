---
layout: post
title: Python - How to return a JSON file?
categories: python json
author: Simon Lee
permalink: /:categories/:title
---

<strong>[Python JSON output][python-json]</strong>

## 1. What you need

- Import module
- Create a Function
- Create a Dictionary
- Convert Dictionary to JSON Object using `dumps()` method
- Return JSON Object

Syntax: `json.dumps(obj, *, skipkeys=False, ensure_ascii=True, check_circular=True, allow_nan=True, cls=None, indent=None, separators=None, default=None, sort_keys=False, **kw)`

json module is a built-in library `import json`.
Return beautified json format in terminal: `json.dumps(DaTa, indent=2, sort_keys=True)`

<br>
<br>
<br>

## 2. Example(1)

{% highlight python %}

# Import Module

import json

# Create geeks function

def geeks():

    # Define Variable
    language = "Python"
    company = "GeeksForGeeks"
    Itemid = 1
    price = 0.00

    # Create Dictionary
    value = {
        "language": language,
        "company": company,
        "Itemid": Itemid,
        "price": price
    }

    # Dictionary to JSON Object using dumps() method
    # Return JSON Object
    return json.dumps(value)

# Call Function and Print it.

print(geeks())
{% endhighlight %}

Expectec Output: `{“language”: “Python”, “company”: “GeeksForGeeks”, “Itemid”: 1, “price”: 0.0}`

<br>
<br>
<br>

## 3. Example(2)

{% highlight python %}

# Import Module

import json

# Create geeks function

def geeks():

    # Create Dictionary
    value = {
        "firstName": "Pawan",
        "lastName": "Gupta",
        "hobbies": ["playing", "problem solving", "coding"],
        "age": 20,
        "children": [
            {
                "firstName": "mohan",
                "lastName": "bansal",
                "age": 15
            },
            {
                "firstName": "prerna",
                "lastName": "Doe",
                "age": 18
            }
        ]
    }

    # Dictionary to JSON Object using dumps() method
    # Return JSON Object
    return json.dumps(value)

# Call Function and Print it.

print(geeks())
{% endhighlight %}

Expectec Output: `{“firstName”: “Pawan”, “lastName”: “Gupta”, “hobbies”: [“playing”, “problem solving”, “coding”], “age”: 20, “children”: [{“firstName”: “mohan”, “lastName”: “bansal”, “age”: 15}, {“firstName”: “prerna”, “lastName”: “Doe”, “age”: 18}]}`

[python-json]: https://www.geeksforgeeks.org/how-to-return-a-json-object-from-a-python-function/
