# Cart Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Cart Viewed",
    "cart": {
        "item": [
            {
                "price": {
                    "isHidden": "<isHidden>"
                },
                "productInfo": {
                    "isBackOrdered": "<isBackOrdered>",
                    "isOutOfStock": "<isOutOfStock>",
                    "productID": "<productID>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|isBackOrdered|boolean|Boolean flag indicating that an inventoried product is on backorder|TRUE, FALSE|||||||
|isHidden|integer|Count of times the price of a product was hidden in the cart due to MAP \(Minimum Advertised Pricing\) requirements.
  Set in the product string for only those products where it is applicable, with a value of 1||||||||
|isOutOfStock|integer|Count of times a product was out of stock at the time of cart view.||||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
