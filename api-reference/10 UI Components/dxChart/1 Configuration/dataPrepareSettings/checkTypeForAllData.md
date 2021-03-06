---
id: dxChart.Options.dataPrepareSettings.checkTypeForAllData
type: Boolean
default: false
---
---
##### shortDescription
Validates the type of each value coming from the data source.

---
Use this property when values in your data source are of a different type, and you need all of them to be visualized on a single axis.

If this property is set to **true**, the type of each value is checked, and the [axis type](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/argumentAxis/type.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/#type') is chosen optimally to display all the values. Otherwise, only the type of the first value is checked, and the axis type is chosen according to the type of this value. In this case, the values that cannot be cast to a data type supported by the axis will be ignored.

[note]Because the type check affects UI component performance, keep this property set to **false** when you have a vast data source with values of the same type, and this type is known beforehand.

#####See Also#####
- **argumentAxis**.[argumentType](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/argumentAxis/argumentType.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/#argumentType') - casts arguments to a specified data type.
- **valueAxis**.[valueType](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/valueAxis/valueType.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/valueAxis/#valueType') - casts values to a specified data type.