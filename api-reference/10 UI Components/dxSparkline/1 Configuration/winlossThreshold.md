---
id: dxSparkline.Options.winlossThreshold
type: Number
default: 0
---
---
##### shortDescription
Specifies a value that serves as a threshold for the sparkline of the winloss type.

---
In the winloss sparkline, values are represented by bars that either grow up or go down from an invisible line. This line is determined by a threshold value. If a data source value is greater than this threshold value, the bar grows up. Otherwise, it goes down.

You can paint the 'win' and 'loss' bars differently. For this purpose, specify the required colors using the [winColor](/api-reference/10%20UI%20Components/dxSparkline/1%20Configuration/winColor.md '/Documentation/ApiReference/UI_Components/dxSparkline/Configuration/#winColor') and [lossColor](/api-reference/10%20UI%20Components/dxSparkline/1%20Configuration/lossColor.md '/Documentation/ApiReference/UI_Components/dxSparkline/Configuration/#lossColor') properties respectively.