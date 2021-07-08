# Form Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Started",
    "form": {
        "formField": [
            {
                "fieldID": "<fieldID>"
            }
        ],
        "formID": "<formID>",
        "formName": "<formName>",
        "formType": "<formType>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|fieldID|string|Unique identifier of a form field within a form. |first\_name, last\_name, addr\_line1, addr\_line2|||||||
|formID|string|Unique identifier of a form. |F-0113, 2543, CU001, PI-0988|||||||
|formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|formType|string|Form type used for grouping of similar forms in reports.  |Address, Contact, Comment, Review, Payment|||||||
