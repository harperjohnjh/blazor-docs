---
title: "Dropdown Menu Popup Items"
component: "Dropdown Menu"
description: "Dropdown Menu allows the end user to customize the whole popup or action items in popup using templates, navigate to other pages on action item click."
---

# Popup items

## Icons

The popup action item have an icon or image to provide visual representation of the action. To place the icon on a popup item, set the [`IconCss`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.SplitButtons.SfDropDownButton~IconCss.html) property to `e-icons` with the required icon CSS. By default, the icon is
positioned to the left side of the popup action item.

In the following sample, the icons for edit, delete, mark as read  and like message menu items are
added using the `IconCss` property.

```csharp
@using Syncfusion.Blazor.SplitButtons

<SfDropDownButton IconCss="e-icons e-message" Content="Message">
    <DropDownButtonItems>
        <DropDownButtonItem Text="Cut"></DropDownButtonItem>
        <DropDownButtonItem Text="Copy"></DropDownButtonItem>
        <DropDownButtonItem Text="Paste"></DropDownButtonItem>
    </DropDownButtonItems>
</SfDropDownButton>

<style>
    .e-message::before {
        content: '\e30d';
    }

    .e-edit::before {
        content: '\e81e';
    }

    .e-delete::before {
        content: '\e84e';
    }

    .e-like::before {
        content: '\e682';
    }

</style>

```

Output be like

![Button Sample](./images/ddb-popup-icon.png)

## Separator

The Separators are the horizontal lines that are used to separate the popup items. You `cannot` select the separators.
You can enable separators to group the popup items using the [`Separator`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.SplitButtons.ItemModel~Separator.html) property.

In the following sample, cut, copy, and paste popup items are grouped using the separator property:

```csharp

@using Syncfusion.Blazor.SplitButtons

<SfDropDownButton Content="Clipboard">
    <DropDownButtonItems>
        <DropDownButtonItem Text="Cut"></DropDownButtonItem>
        <DropDownButtonItem Text="Copy"></DropDownButtonItem>
        <DropDownButtonItem Text="Paste"></DropDownButtonItem>
        <DropDownButtonItem Separator=true></DropDownButtonItem>
        <DropDownButtonItem Text="Font"></DropDownButtonItem>
        <DropDownButtonItem Text="Paragraph"></DropDownButtonItem>
    </DropDownButtonItems>
</SfDropDownButton>

```

Output be like

![Button Sample](./images/ddb-separator.png)

## Navigations

Actions in Dropdown Menu can be used to navigate to the other web page when action item is clicked. This can be achieved by providing link to the action item using [`url`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.SplitButtons.ItemModel~Url.html) property.

In the following sample, navigation URL for Flipkart, Amazon, and Snapdeal action items are added using the url property:

```csharp

@using Syncfusion.Blazor.SplitButtons

<SfDropDownButton IconCss="e-icons e-shopping" Content="Shop By">
    <DropDownButtonItems>
        <DropDownButtonItem Text="Flipkart" Url="https://www.google.co.in/search?q=flipkart"></DropDownButtonItem>
        <DropDownButtonItem Text="Amazon" Url="https://www.google.co.in/search?q=amazon"></DropDownButtonItem>
        <DropDownButtonItem Text="Snapdeal" Url="https://www.google.co.in/search?q=snapdeal"></DropDownButtonItem>
    </DropDownButtonItems>
</SfDropDownButton>

<style>

.e-shopping::before {
    content: '\e30c';
}

</style>

```

Output be like

![Button Sample](./images/ddb-navigation.png)

## Template

### Item Templating

Popup items can be customized using the [`OnItemRender`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.SplitButtons.DropDownButtonEvents~OnItemRender.html) event. The item render event triggers while rendering each popup action item. The event argument will be used to customize the items based on the requirement.

```csharp

@using Syncfusion.Blazor.SplitButtons

<SfDropDownButton Content="Edit">
    <DropDownButtonEvents OnItemRender="Render"></DropDownButtonEvents>
    <DropDownButtonItems>
        <DropDownButtonItem Text="Cut"></DropDownButtonItem>
        <DropDownButtonItem Text="Copy"></DropDownButtonItem>
        <DropDownButtonItem Text="Paste"></DropDownButtonItem>
    </DropDownButtonItems>
</SfDropDownButton>

@code {
    public void Render(MenuEventArgs args)
    {
        args.Element.AddClass(new string[] { "custom" });
    }
}

<style>
    .custom{
        float: left;
        font-size: 10px;
        padding-left: 50px;
        font-style: oblique;
    }
</style>

```

Output be like

![Button Sample](./images/ddb-template.png)