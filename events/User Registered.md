# User Registered

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Registered",
    "user": {
        "country": "<country>",
        "loginStatus": "<loginStatus>",
        "loyalty": {
            "isLoyaltyRegistration": "<isLoyaltyRegistration>"
        },
        "profileAttributesList": "<profileAttributesList>",
        "userType": "<userType>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|country|string|The country associated with this user's profile.|USA, Canada|||||||
|isLoyaltyRegistration|integer|User regsitered for a new Loyalty account.||||||||
|loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|profileAttributesList|string|A twice delimited string of key \/ value pairs.  Use \~ between key and value.  Use \| between pairs|homeStore\~234\|loyaltyTier\~gold\|memberSince\~2002|||||||
|userType|string|Describes the type of the user.  Often used to differentiate customers from employees or associates. |employee, guest, agent, customer|||||||
