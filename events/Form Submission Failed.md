# Form Submission Failed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Submission Failed",
    "form": {
        "formError": "<formError>",
        "formField": [
            {
                "fieldID": "<fieldID>",
                "formFieldError": "<formFieldError>"
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
|formError|string|Error text or code describing a form error.  This is the form-level error.|Credit card declined, Required entries missing, EC3456, EC8976|||||||
|formFieldError|string|Error text or code describing a form field error.  |email address invalid, date required. EC987767, EC4567|||||||
|formID|string|Unique identifier of a form. |F-0113, 2543, CU001, PI-0988|||||||
|formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|formType|string|Form type used for grouping of similar forms in reports.  |Address, Contact, Comment, Review, Payment|||||||
