## What is Yaml
YAML (YAML Ain’t Markup Language) is a human-readable data serialization language.
It’s often used for configuration files and data exchange between languages with different data structures.

For example, suppose you are writing a Python app that needs an input such as a simple list of users.
Instead of hardcoding the data or using a database, you can write that list in a YAML file and load it into your Python application.

This way, YAML helps you pass structured data (like lists, dictionaries) to your Python app in a clean, readable format.

In the same case you can also use some alternative like json and txt. 

But Yaml has its own advantage that is readable format.

## Yaml syntax

### String, Number, Boolean

```bash
String: "yoga", "setiawan"
Number: 20
Boolean: true
```
### List

```bash
student:
  - Anwar
  - Jhon
  - Mario
  - Marcus
```

### Dictionary

```bash
Person:
   name: Yoga 
   age: 20
   country: Indonesia
```

### List of Dictionary
Yaml allow nesting list and dictionary to represent more complex data

```bash
tasks:
  task_1:
   - red
   - orange
   - purple
   task_2:
   - black
   - white
   - green
```