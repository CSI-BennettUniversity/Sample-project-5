# forms-dynamically

## Introduction
In situations where you wish to generate fomrs dynamically form generaation is required. In such a use case it is very helpful to convert HTML forms into code compatible formats, in this case JSON. Hence, in short, this is a tiny and light weight npm package that allows you to convert an HTML Form to JSON and back.

# Documentation and Guide
## Installation
```bash
npm i forms-dynamically
```
OR
```HTML
<script src="https://unpkg.com/forms-dynamically@1.2.1/forms.min.js"></script>
```

## Usage


### **formToJson(id)**
*arguments required : Id of form element*

*returns: JSON object with structure*

Reads input elements of the form one by one and then stores them in a JSON format

e.g.

```HTML
<form id="testForm">

  <input type="text" id="name" name="name" placeholder="What is your name?">

  <input type="number" id="age" name="age" class="agefield">

</form>
```

Suppose there is a form like above in the HTML of any page.

When formToJson("testForm") is called it should return something like this

```json
{
"formId": "testForm",
"elements": [{
    "elementType": "input",
    "type": "text",
    "id": "name",
    "name": "name",
    "placeholder": "What is your name"
  },
  {
    "elementType": "input",
    "type": "number",
    "id": "age",
    "name": "age",
    "class": "agefield"

  }
]
}
```

Note : This is just a suggestive JSON. You can define your own structure.
The idea is to be able to store a structure of the form in JSON format.

### jsonToForm(jsonObject)
*arguments JSON object with structure mentioned above*

*returns: HTML for the form rendered with the given structure*

The **jsonToForm()** function will parse the JSON which we generated in the previous function and generate
a form HTML and populate the form HTML in the div given with targetDivId

# Future Scope 
The coming up features in this package is to be able to convert forms not only to JSON, but also to XML and back

# Language used
(Vannila) JavaScript

# Author 
[Muskan Vaswan](https://github.com/muskanvaswan)
