DevExtreme provides the <a href="https://github.com/DevExpress/DevExtreme.AspNet.Data/blob/master/README.md" target="_blank">DevExtreme.AspNet.Data</a> extension to access an ASP.NET Web API service. This extension consists of two parts: the server-side part implements data processing on the server according to the protocol the TreeList uses; the client-side part creates and configures a [CustomStore](/api-reference/30%20Data%20Layer/CustomStore '/Documentation/ApiReference/Data_Layer/CustomStore/') to access the server from the client. The following code shows how to use the extension's client-side <a href="https://github.com/DevExpress/DevExtreme.AspNet.Data/blob/master/docs/client-side-with-jquery.md#api-reference" target="_blank">createStore</a> method.

You should configure [remoteOperations](/api-reference/10%20UI%20Components/dxTreeList/1%20Configuration/remoteOperations '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/remoteOperations/') to notify the TreeList that the server handles data.

---
#####jQuery

    <!--JavaScript-->
    $(function() {
        var serviceUrl = "http://url/to/my/service";
        $("#treeListContainer").dxTreeList({
            dataSource: DevExpress.data.AspNet.createStore({
                key: "ID",
                loadUrl: serviceUrl + "/GetAction",
                insertUrl: serviceUrl + "/InsertAction",
                updateUrl: serviceUrl + "/UpdateAction",
                deleteUrl: serviceUrl + "/DeleteAction"
            }),
            remoteOperations: { 
                filtering: true,
                sorting: true,
                grouping: true
            },
            // ...
        })
    });

#####Angular

    <!--TypeScript-->
    import { DxTreeListModule } from "devextreme-angular";
    import CustomStore from "devextreme/data/custom_store";
    import { createStore } from "devextreme-aspnet-data-nojquery";
    // ...
    export class AppComponent {
        store: CustomStore;
        constructor() {
            let serviceUrl = "http://url/to/my/service";
            this.store = createStore({
                key: "ID",
                loadUrl: serviceUrl + "/GetAction",
                insertUrl: serviceUrl + "/InsertAction",
                updateUrl: serviceUrl + "/UpdateAction",
                deleteUrl: serviceUrl + "/DeleteAction"
            })
        }
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })

    <!--HTML-->
    <dx-tree-list ...
        [dataSource]="store">
        <dxo-remote-operations 
            [filtering]="true"
            [sorting]="true"
            [grouping]="true">
        </dxo-remote-operations>
    </dx-tree-list>

---

#include common-demobutton with { 
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/TreeList/WebAPIService/" 
}
