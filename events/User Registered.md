# User Registered

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Registered",
    "user": {
        "loginStatus": "<loginStatus>",
        "loyalty": {
            "isLoyaltyRegistration": "<isLoyaltyRegistration>"
        },
        "registrationStatus": "<registrationStatus>",
        "registrationType": "<registrationType>",
        "userType": "<userType>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|isLoyaltyRegistration|integer|User regsitered for a new Loyalty account.||||||||
|loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|registrationStatus|string|Describes the registration state of the user \(independent of sign-in state\)|registered|||||||
|registrationType|string|Describes the thing that was registered for |account, loyalty program, event, sweepstakes, warranty|||||||
|userType|string|Describes the type of the user.  Often used to differentiate customers from employees or associates. |employee, guest, agent, customer|||||||
