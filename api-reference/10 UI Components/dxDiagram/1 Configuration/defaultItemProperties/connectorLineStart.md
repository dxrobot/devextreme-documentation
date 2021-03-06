---
id: dxDiagram.Options.defaultItemProperties.connectorLineStart
acceptValues: 'none' | 'arrow' | 'outlinedTriangle' | 'filledTriangle'
type: String
default: 'none'
---
---
##### shortDescription
Specifies the default tip of a connector's start point.

---
The **connectorLineStart** property specifies a tip that is displayed at a connector's start point if the [fromLineEndExpr](/api-reference/10%20UI%20Components/dxDiagram/1%20Configuration/edges/fromLineEndExpr.md '/Documentation/ApiReference/UI_Components/dxDiagram/Configuration/edges/#fromLineEndExpr') property does not provide another value.

#include common-ref-enum with {
    enum: "`DiagramConnectorLineEnd`",
    values: "`None`, `Arrow`, `OutlinedTriangle`, `FilledTriangle`"
}