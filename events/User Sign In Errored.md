# User Sign In Errored

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Sign In Errored",
    "user": {
        "loginStatus": "<loginStatus>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
