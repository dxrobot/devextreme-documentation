---
id: dxLookup.Options.popupWidth
type: Number | String | function()
default: function() {return $(window).width() * 0.8 }, function() { return Math.min($(window).width(), $(window).height()) * 0.4; } (iPad)
dep: dxLookup.Options.dropDownOptions
---
---
##### shortDescription
Specifies the popup element's width. Applies only if [fullScreen](/api-reference/10%20UI%20Components/dxLookup/1%20Configuration/fullScreen.md '/Documentation/ApiReference/UI_Components/dxLookup/Configuration/#fullScreen') is **false**.

##### return: Number | String
The popup element's width.

---
