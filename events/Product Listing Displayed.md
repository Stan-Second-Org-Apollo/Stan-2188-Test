# Product Listing Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Listing Displayed",
    "listingDisplayed": {
        "displayCount": "<displayCount>",
        "filterList": "<filterList>",
        "filterListLength": "<filterListLength>",
        "listing": [
            {
                "isDisplayed": "<isDisplayed>",
                "price": {
                    "currency": "<currency>",
                    "pointRangeHigh": "<pointRangeHigh>"
                },
                "productInfo": {
                    "isFeatured": "<isFeatured>",
                    "productID": "<productID>"
                }
            }
        ],
        "listingContext": "<listingContext>",
        "listingDriver": "<listingDriver>",
        "listingPersonalized": "<listingPersonalized>",
        "listingType": "<listingType>",
        "relatedSearchTermDisplayed": "<relatedSearchTermDisplayed>",
        "resultsCount": "<resultsCount>",
        "resultsNull": "<resultsNull>",
        "sortDefault": "<sortDefault>",
        "sortOrder": "<sortOrder>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|currency|string|Currency of the prices given. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|displayCount|integer|The total number of items displayed out of all returned items. \(Integer\)|10, 20, 30, 40||||0|||
|filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||
|filterListLength|integer|The number of filterValue pairs in the filterList|0, 20, 12||||0|||
|isDisplayed|boolean|Helper node used by AA Product String Builder to set product scoped events|true|||||||
|isFeatured|integer|Count of times the product was a featured\/boosted product.||||||||
|listingContext|string|Describes the context of a listing display \(sort changed, filter added, filter removed\)|Filter Added, Filter Removed, Sort Change, Pagination|||||||
|listingDriver|string|Describes the action that caused the listing to be displayed|Onsite Search, Curated Assortment, Navigation|||||||
|listingPersonalized|integer|Count of times a user lands on a product listing that is personalized for them based on their history or cookies.||||||||
|listingType|string|The type of results being listed|text, product, location, event, room, product location|||||||
|pointRangeHigh|integer|Upper end of the point range shown.|5000, 2520, 3200|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|relatedSearchTermDisplayed|integer|Count of times a user viewed product listings or search results with "Related Search Terms" present.||||||||
|resultsCount|integer|The total number of items returned that matched the search criteria. \(Integer\)|1, 21, 111, 166||||0|||
|resultsNull|integer|Count of times that an on-site search was performed that resulted in 0 results.||||||||
|sortDefault|integer|The default sort value on listings|A to Z, Low to High, Newest to Oldest||||0|||
|sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||
