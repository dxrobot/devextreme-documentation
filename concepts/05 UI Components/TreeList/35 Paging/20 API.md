Call the [pageCount()](/api-reference/10%20UI%20Components/dxTreeList/3%20Methods/pageCount().md '/Documentation/ApiReference/UI_Components/dxTreeList/Methods/#pageCount') method to get the total page count.

---

#####jQuery

    <!--JavaScript-->
    var totalPageCount = $("#treeListContainer").dxTreeList("instance").pageCount();

#####Angular

    <!--TypeScript-->
    import { ..., ViewChild } from "@angular/core";
    import { DxTreeListModule, DxTreeListComponent } from "devextreme-angular";
    // ...
    export class AppComponent {
        @ViewChild(DxTreeListComponent, { static: false }) treeList: DxTreeListComponent;
        // Prior to Angular 8
        // @ViewChild(DxTreeListComponent) treeList: DxTreeListComponent;
        getTotalPageCount () {
            this.treeList.instance.pageCount();
        }
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })

---

The TreeList also provides the [pageIndex(newIndex)](/api-reference/10%20UI%20Components/GridBase/3%20Methods/pageIndex(newIndex).md '/Documentation/ApiReference/UI_Components/dxTreeList/Methods/#pageIndexnewIndex') and [pageSize(value)](/api-reference/10%20UI%20Components/GridBase/3%20Methods/pageSize(value).md '/Documentation/ApiReference/UI_Components/dxTreeList/Methods/#pageSizevalue') methods that switch the UI component to a specific page and change the page size. They can also be called without arguments, in which case, they return the current page's index and size.

---

#####jQuery

    <!--JavaScript-->
    $("#treeListContainer").dxTreeList("instance").pageSize(8);

<!---->

    <!--JavaScript-->
    var goToLastPage = function (treeListInstance) {
        treeListInstance.pageIndex(treeListInstance.pageCount() - 1);
    }

#####Angular

    <!--TypeScript-->
    import { ..., ViewChild } from "@angular/core";
    import { DxTreeListModule, DxTreeListComponent } from "devextreme-angular";
    // ...
    export class AppComponent {
        @ViewChild(DxTreeListComponent, { static: false }) treeList: DxTreeListComponent;
        // Prior to Angular 8
        // @ViewChild(DxTreeListComponent) treeList: DxTreeListComponent;
        changePageSize () {
            this.treeList.instance.pageSize(8);
        }
        goToLastPage () {
            this.treeList.instance.pageIndex(this.treeList.instance.pageCount() - 1);
        }
    }
    @NgModule({
        imports: [
            // ...
            DxTreeListModule
        ],
        // ...
    })

---

#####See Also#####
- [Scrolling](/concepts/05%20UI%20Components/TreeList/45%20Scrolling '/Documentation/Guide/UI_Components/TreeList/Scrolling/')
