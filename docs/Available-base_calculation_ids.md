# Available base_calculation_ids

These are the base_calculation_id values that can be used in the response `breakdown` object's `base_calculation_id` attribute:


ID | Name | Description | Expression
---------|----------|---------|---------
 1|BL|Charge that applies per Bill of Lading|`max($RATE, $MINIMUM)`
2|CONTAINER|Charge that applies per container|`max($RATE * $QUANTITY, $MINIMUM)`
3|WM|Weight Measure for LCL|`max($RATE * $WEIGHT_KGS / 1000, $RATE * $VOLUME_CBM, $MINIMUM)`
4|W|Charge per Ton|`max($RATE * ($WEIGHT_KGS / 1000), $MINIMUM)`
5|M|Charge per Cubic Meter|`max($RATE * $VOLUME_CBM, $MINIMUM)`
6|LUMPSUM|Flat charge|`$RATE`
7|KG|Charge per kilogram|`max($RATE * $WEIGHT_KGS, $MINIMUM)`

If you need more charge codes, please send your request to support@qwyk.io