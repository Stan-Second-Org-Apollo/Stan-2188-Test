# Room Listing Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Room Listing Displayed",
    "listingDisplayed": {
        "filterList": "<filterList>",
        "listing": [
            {
                "isDisplayed": "<isDisplayed>"
            }
        ],
        "listingContext": "<listingContext>",
        "resultsCount": "<resultsCount>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||
|isDisplayed|boolean|Helper node used by AA Product String Builder to set product scoped events|true|||||||
|listingContext|string|Describes the context of a listing display \(sort changed, filter added, filter removed\)|Filter Added, Filter Removed, Sort Change, Pagination|||||||
|resultsCount|integer|The total number of items returned that matched the search criteria. \(Integer\)|1, 21, 111, 166||||0|||
