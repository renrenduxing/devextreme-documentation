If you do not explicitly specify certain columns' [width](/api-reference/_hidden/GridBaseColumn/width.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/columns/#width'), the TreeList distributes the available space equally among columns at startup. As a result, cell values may appear truncated. Use the [columnMinWidth](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/columnMinWidth.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#columnMinWidth') property to specify a minimum width for all columns and the [minWidth](/api-reference/_hidden/GridBaseColumn/minWidth.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/columns/#minWidth') for an individual column. Note that all these settings may cause horizontal scrolling if columns cannot fit into the UI component's width.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        $("#treeListContainer").dxTreeList({
            // ...
            columnMinWidth: 100,
            columns: [{
                dataField: "Title",
                width: 200
            }, {
                dataField: "Address",
                minWidth: 150
            }]
        });
    });

##### Angular
    
    <!--HTML-->
    <dx-tree-list ...
        [columnMinWidth]="100">
        <dxi-column dataField="Title" [width]="200"></dxi-column>
        <dxi-column dataField="Address" [minWidth]="150"></dxi-column>
    </dx-tree-list>

    <!--TypeScript-->
    import { DxTreeListModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxTreeList ...
            :column-min-width="100">
            <DxColumn data-field="Title" :width="200" />
            <DxColumn data-field="Address" :min-width="150" />
        </DxTreeList>
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import DxTreeList, {
        DxColumn
    } from 'devextreme-vue/tree-list';

    export default {
        components: {
            DxTreeList,
            DxColumn
        },
        // ...
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';

    import 'devextreme/dist/css/dx.light.css';

    import TreeList, {
        Column
    } from 'devextreme-react/tree-list';

    export default function App() {
	    return (
            <TreeList ...
                columnMinWidth={100}>
                <Column dataField="Title" width={200} />
                <Column dataField="Address" minWidth={150} />
            </TreeList> 
        );
    }
    
---

Set the [columnAutoWidth](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/columnAutoWidth.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#columnAutoWidth') property to **true** to make all columns adjust their widths to their content.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        $("#treeListContainer").dxTreeList({
            // ...
            columnAutoWidth: true
        });
    });

##### Angular
    
    <!--HTML-->
    <dx-tree-list ...
        [columnAutoWidth]="true">
    </dx-tree-list>

    <!--TypeScript-->
    import { DxTreeListModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxTreeList ...
            :column-auto-width="true">
        </DxTreeList>
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import DxTreeList from 'devextreme-vue/tree-list';

    export default {
        components: {
            DxTreeList
        },
        // ...
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';

    import 'devextreme/dist/css/dx.light.css';

    import TreeList from 'devextreme-react/tree-list';

    export default function App() {
	    return (
            <TreeList ...
                columnAutoWidth={true}>
            </TreeList>
        );
    }
    
---

The UI component allows a user to resize columns in two different modes: by changing the next column's width or the UI component's width. To enable this functionality and set the mode, specify the [allowColumnResizing](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/allowColumnResizing.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#allowColumnResizing') and [columnResizingMode](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/columnResizingMode.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#columnResizingMode') properties, respectively. Note that you can prevent a specific column from being resized by assigning **false** to its [allowResizing](/api-reference/_hidden/GridBaseColumn/allowResizing.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/columns/#allowResizing') property.

---
##### jQuery

    <!--JavaScript-->
    $(function() {
        $("#treeListContainer").dxTreeList({
            // ...
            allowColumnResizing: true,
            columnResizingMode: 'widget', // or 'nextColumn'
            columns: [{
                dataField: "Title",
                allowResizing: false
            }, // ...
            ]
        });
    });

##### Angular
    
    <!--HTML-->
    <dx-tree-list ...
        [allowColumnResizing]="true"
        columnResizingMode="widget"> <!-- or 'nextColumn' -->
        <dxi-column dataField="Title" [allowResizing]="false"></dxi-column>
    </dx-tree-list>

    <!--TypeScript-->
    import { DxTreeListModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxTreeList ...
            :allow-column-resizing="true"
            column-resizing-mode="widget"> <!-- or "nextColumn" -->
            <DxColumn data-field="Title" :allow-resizing="false" />
        </DxTreeList>
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import DxTreeList, {
        DxColumn
    } from 'devextreme-vue/tree-list';

    export default {
        components: {
            DxTreeList,
            DxColumn
        },
        // ...
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';

    import 'devextreme/dist/css/dx.light.css';

    import TreeList, {
        Column
    } from 'devextreme-react/tree-list';

    export default function App() {
	    return (
            <TreeList ...
                allowColumnResizing={true}
                columnResizingMode="widget"> <!-- or 'nextColumn' -->
                <Column dataField="Title" allowResizing={false} />
            </TreeList>
        );
    }
    
    
---

#include btn-open-demo with {
    href: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Tree_List/Resizing/AngularJS/Light/"
}

#####See Also#####
- [TreeList - Column Reordering](/concepts/05%20UI%20Components/TreeList/10%20Columns/25%20Column%20Reordering '/Documentation/Guide/UI_Components/TreeList/Columns/Column_Reordering/')
