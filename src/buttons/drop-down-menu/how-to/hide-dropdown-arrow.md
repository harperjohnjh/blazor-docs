---
title: "Hide dropdown arrow"
component: "Dropdown Menu"
description: "Dropdown Menu how to section, hide drop down arrow, group popup items using list view component, dialog open on popup item click."
---

# Hide dropdown arrow

You can hide the dropdown arrow from the Dropdown Menu by adding class `e-caret-hide`
to Dropdown Menu element using [`CssClass`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.SplitButtons.SfDropDownButton~CssClass.html)
property.

```csharp
@using Syncfusion.Blazor.SplitButtons

<SfDropDownButton CssClass="e-caret-hide" Content="Message">
    <DropDownButtonItems>
        <DropDownButtonItem Text="Edit"></DropDownButtonItem>
        <DropDownButtonItem Text="Delete"></DropDownButtonItem>
        <DropDownButtonItem Text="Mark as Read"></DropDownButtonItem>
        <DropDownButtonItem Text="Like Message"></DropDownButtonItem>
    </DropDownButtonItems>
</SfDropDownButton>

```

Output be like

![Button Sample](./../images/ddb-hide.png)