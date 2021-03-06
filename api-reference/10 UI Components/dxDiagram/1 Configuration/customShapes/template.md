---
id: dxDiagram.Options.customShapes.template
type: template
---
---
##### shortDescription
Specifies a custom template for the shape.

##### param(container): dxSVGElement
#include common-ref-elementparam with { element: "shape" }

##### param(data): Object
Information about the shape.

##### field(data.item): dxDiagramShape
The shapes object.

---
The template content must be presented as SVG elements.

Use the [customShapeTemplate](/api-reference/10%20UI%20Components/dxDiagram/1%20Configuration/customShapeTemplate.md '/Documentation/ApiReference/UI_Components/dxDiagram/Configuration/#customShapeTemplate') property to define a common template for all shapes in the Diagram UI component.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Diagram/CustomShapesWithTemplates/jQuery/Light/"
}

#####See Also#####
- [Custom Templates](/concepts/05%20UI%20Components/zz%20Common/30%20Templates/10%20Custom%20Templates.md '/Documentation/Guide/UI_Components/Common/Templates/#Custom_Templates')