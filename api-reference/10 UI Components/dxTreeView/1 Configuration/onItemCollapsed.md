---
id: dxTreeView.Options.onItemCollapsed
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed when a tree view item is collapsed.

##### param(e): ui/tree_view:ItemCollapsedEvent
Information about the event.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.event): event
#include common-ref-eventparam

##### field(e.itemData): Object
The collapsed item's data.

##### field(e.itemElement): DxElement
#include common-ref-elementparam with { element: "item" }

##### field(e.itemIndex): Number
The item's index.

##### field(e.model): any
Model data. Available only if Knockout is used.

##### field(e.node): dxTreeViewNode
The item's node.

---
#####See Also#####
-[Expand and Collapse Nodes - Events](/concepts/05%20UI%20Components/TreeView/20%20Expand%20and%20Collapse%20Nodes/10%20Events.md '/Documentation/Guide/UI_Components/TreeView/Expand_and_Collapse_Nodes/#Events')