---
title: "Enable or disable context menu items"
component: "Context Menu"
description: "This section helps to learn how to Enable or disable context menu items"
---

# Enable or disable context menu items

You can enable and disable the menu items using the [`Disabled`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Navigations.MenuItem.html#Syncfusion_Blazor_Navigations_MenuItem_Disabled) property in [`MenuItem`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Navigations.MenuItem.html). To disable menuItems, set the [`Disabled`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Navigations.MenuItem.html#Syncfusion_Blazor_Navigations_MenuItem_Disabled) property in each item to `true` and vice-versa.

In the following example, the **Display Settings** in parent items is disabled during initial loading and **Medium icons** in sub menu items are enabled/disabled dynamically while opening the sub menu.

```csharp

@using Syncfusion.Blazor.Navigations

<div id="target">Right click/Touch hold to open the ContextMenu </div>
<SfContextMenu Target="#target" TValue="MenuItem">
    <MenuItems>
        <MenuItem Text="View">
            <MenuItems>
                <MenuItem Text="Large Icons"></MenuItem>
                <MenuItem Text="Medium Icons" Disabled="@disableState"></MenuItem>
                <MenuItem Text="Small Icons"></MenuItem>
            </MenuItems>
        </MenuItem>
        <MenuItem Text="Sort By"></MenuItem>
        <MenuItem Text="Refresh"></MenuItem>
        <MenuItem Separator="true"></MenuItem>
        <MenuItem Text="New"></MenuItem>
        <MenuItem Separator="true"></MenuItem>
        <MenuItem Text="Display Settings" Disabled="true"></MenuItem>
        <MenuItem Text="Personalize"></MenuItem>
    </MenuItems>
    <MenuEvents TValue="MenuItem" OnOpen="@BeforeOpenHandler"></MenuEvents>
</SfContextMenu>

@code {
    private bool disableState;

    private void BeforeOpenHandler(BeforeOpenCloseMenuEventArgs<MenuItem> e)
    {
        // While opening the first level context menu the parent item will not be available, so it would be null.
        if (e.ParentItem != null && e.ParentItem.Text == "View")
            disableState = !disableState; // Execute only for the View item sub menu.
    }
};

<style>
    #target {
        border: 1px dashed;
        height: 150px;
        padding: 10px;
        position: relative;
        text-align: justify;
        color: gray;
        user-select: none;
    }
</style>

```

Output be like

![Context Menu Sample](./../images/cm-disable.png)

> To disable sub menu items, use the [`OnOpen`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.Navigations.SfContextMenu~OnOpen.html) event.