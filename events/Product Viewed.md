# Product Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Viewed",
    "product": [
        {
            "fulfillment": {
                "isBopusOnly": "<isBopusOnly>"
            },
            "isThirdPartyProduct": "<isThirdPartyProduct>",
            "price": {
                "sellingPrice": "<sellingPrice>"
            },
            "productInfo": {
                "isFeatured": "<isFeatured>",
                "isOutOfStock": "<isOutOfStock>",
                "isSKuAvailable": "<isSKuAvailable>",
                "productID": "<productID>",
                "thirdyPartyVendorID": "<thirdyPartyVendorID>"
            }
        }
    ],
    "productInfo": {
        "isBestSeller": "<isBestSeller>",
        "isTopRated": "<isTopRated>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|isBestSeller|integer|Count of times the product was a best seller product.||||||||
|isBopusOnly|integer|Count of times the user engaged with a product whose only available shipping method was Buy Online Pick Up In Store \(i.e., BOPUS\).||||||||
|isFeatured|integer|Count of times the product was a featured\/boosted product.||||||||
|isOutOfStock|boolean|Boolean flag indicating that an inventoried product is out of stock. |TRUE, FALSE|||||||
|isSKuAvailable|boolean|True\/False flag to indicate if product SKU is known at the time of the event|true, false|||||||
|isThirdPartyProduct|integer|Count of times a user viewed a product page for a third party \(e.g., marketplace vendor\) product.||||||||
|isTopRated|integer|Count of times the product was a top rated product.||||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|thirdyPartyVendorID|string|Captures the vendor id of the third party vendor associated with product conversion.||||||||
