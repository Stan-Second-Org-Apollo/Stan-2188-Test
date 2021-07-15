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
                "priceTier": "<priceTier>",
                "priceType": "<priceType>",
                "sellingPrice": "<sellingPrice>"
            },
            "productInfo": {
                "brand": "<brand>",
                "businessUnit": "<businessUnit>",
                "color": "<color>",
                "discountAmount": "<discountAmount>",
                "fulfillmentOptions": "<fulfillmentOptions>",
                "isFeatured": "<isFeatured>",
                "isOutOfStock": "<isOutOfStock>",
                "isSKuAvailable": "<isSKuAvailable>",
                "name": "<name>",
                "productID": "<productID>",
                "productLine": "<productLine>",
                "quantityAvailable": "<quantityAvailable>",
                "ratingAverage": "<ratingAverage>",
                "ratingCount": "<ratingCount>",
                "ratingCountAndAverageCombined": "<ratingCountAndAverageCombined>",
                "sku": "<sku>",
                "status": "<status>",
                "thirdyPartyVendorID": "<thirdyPartyVendorID>",
                "trademarkedTechnology": "<trademarkedTechnology>",
                "webExclusive": "<webExclusive>"
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
|brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|color|string|Describes the colorway of a product or product variant|Antique Oak, Granite, Black Marble, Knotty Pine|||||||
|discountAmount|string|The product discount amount shown to the visitor for each product.|$20, 10%, $5|||||||
|fulfillmentOptions|string|The product fulfillment options available for each product to view impact on conversion.|Shipped Only, In Store Only, Local Pickup Only, In Store or Ship, Digital \(Email or Text\)|||||||
|isBestSeller|integer|Count of times the product was a best seller product.||||||||
|isBopusOnly|integer|Count of times the user engaged with a product whose only available shipping method was Buy Online Pick Up In Store \(i.e., BOPUS\).||||||||
|isFeatured|integer|Count of times the product was a featured\/boosted product.||||||||
|isOutOfStock|boolean|Boolean flag indicating that an inventoried product is out of stock. |TRUE, FALSE|||||||
|isSKuAvailable|boolean|True\/False flag to indicate if product SKU is known at the time of the event|true, false|||||||
|isThirdPartyProduct|integer|Count of times a user viewed a product page for a third party \(e.g., marketplace vendor\) product.||||||||
|isTopRated|integer|Count of times the product was a top rated product.||||||||
|priceTier|string|Describes the general pricing tier of a product. \(Good, Better, Best\)|Good, Better, Best, Bronze, Silver, Gold|||||||
|priceType|string|Describes the type of price offered using commonly used terms. |1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|productLine|string|Describes the product Line of a product. |Laminate Wood, Vinyl, Hardwood, Stone, Ceramic|||||||
|quantityAvailable|string|The product quantity available.|1, 10, 100|||||||
|ratingAverage|string|String representation of the average customer rating.  Positive. Up to two decimal places. This is most often a number between 0 and 5. |1.1, 2, 5|^[0-9]*(\.[0-9]{1,2})?$||||||
|ratingCount|integer|Integer number of customer ratings. |1, 5, 11, 200||||0|||
|ratingCountAndAverageCombined|string|Combined Rating Count and Rating Average with colon as delimiter|23:4.5, 222:1.7, 1:5, 2:3.5|||||||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|status|string|Described the product's status|In Stock, Out of Stcok, Back-Ordered|||||||
|thirdyPartyVendorID|string|Captures the vendor id of the third party vendor associated with product conversion.||||||||
|trademarkedTechnology|string|Describes trademarks and\/or technical branding used to describe the product|Stainmaster, GoreTex, WeatherShield|||||||
|webExclusive|boolean|Captures whether or not the product is sold on website\/app only.||||||||
