# Related Products Viewed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Related Products Viewed",
    "relatedProducts": {
        "item": [
            {
                "itemPosition": "<itemPosition>",
                "price": {
                    "priceType": "<priceType>"
                },
                "productInfo": {
                    "brand": "<brand>",
                    "name": "<name>",
                    "productID": "<productID>",
                    "sku": "<sku>"
                },
                "recommendationDisplayZone": "<recommendationDisplayZone>",
                "recommendationEngine": "<recommendationEngine>",
                "recommendationID": "<recommendationID>",
                "recommendationParentProductID": "<recommendationParentProductID>",
                "recommendationStrategy": "<recommendationStrategy>"
            }
        ]
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|itemPosition|integer|Integer position of a property within a sorted result. The first returned is position 1. For map results, this value can be the rank by distance from POI.|1, 2, 3, 4, 5||||0|||
|name|string|Name of the product or offering.  Should be unique and 1:1 with productID|Oceana, Corsica, Flame Tech, Air Jordan 88|||||||
|priceType|string|Describes the type of price offered using commonly used terms. |1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|recommendationDisplayZone|string|Describes the zone or content area wher ethe recommendation is shown.|Right Rail, Footer, Top Bar|||||||
|recommendationEngine|string|Engine associated with product cross-sell that were generated from a data science recommendation engine.||||||||
|recommendationID|string|ID associated with product cross-sell that were generated from a data science recommendation engine.||||||||
|recommendationParentProductID|string|Unique Identifier of the parent product or offering for which the recommendation is offerred.|155, 65588, 987764448, cart, none, behavior|||||||
|recommendationStrategy|string|Describes the strategy used to include a related product.|Previously Viewed, Others Also Viewed, Others Bought With, Similar Item|||||||
|sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
