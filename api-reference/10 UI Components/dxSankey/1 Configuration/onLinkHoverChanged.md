---
id: dxSankey.Options.onLinkHoverChanged
type: function(e)
default: null
EventForAction: dxSankey.linkHoverChanged
notUsedInTheme: 
---
---
##### shortDescription
A function that is executed after the pointer enters or leaves a sankey link.

##### param(e): Object
Information about the event.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): dxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.model): Object
The model data. Available only if you use Knockout.

##### field(e.target): dxSankeyLink
The [Link](/api-reference/10%20UI%20Components/dxSankey/7%20Link '/Documentation/ApiReference/UI_Components/dxSankey/Link/') object.

---
#####See Also#####
- **link**.[hoverStyle](/api-reference/10%20UI%20Components/dxSankey/1%20Configuration/link/hoverStyle '/Documentation/ApiReference/UI_Components/dxSankey/Configuration/link/hoverStyle/')