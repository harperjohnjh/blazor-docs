---
title: "Action Buttons"
component: "Card"
description: "This section explains how to customizes the card using action buttons and changes the vertical or horizontal alignment of the card element."
---

# Action Buttons

You can include Action buttons within the Card and customize them. Action button is a `div` element with `CardFooter` component followed by button tag or anchor tag within the card root element.

* For adding action buttons you can create a  `CardFooterContent` component within the card action element.

```csharp
@using Syncfusion.Blazor.Cards

<SfCard ID="HugeImage">
    <CardFooter>
        <CardFooterContent>
        </CardFooterContent>
    </CardFooter>
</SfCard>
```

## Vertical

By default, action buttons positioned in horizontal alignment , and also it can be aligned to show in vertical alignment by adding `Orientation` property.

```csharp
@using Syncfusion.Blazor.Cards
@using Syncfusion.Blazor.Buttons

<SfCard ID="HugeImage" Orientation="CardOrientation.Vertical">
    <CardImage Image="images/cards/steven.png"/>
    <CardHeader Title="Harrisburg Keith" SubTitle="@CardSubTitle"/>
    <CardContent Content="Hi, I'm creative graphic design for print, new media based in Edenbridge"/>
    <CardFooter>
        <CardFooterContent>
            <SfButton CssClass="e-btn e-outline e-primary">FOLLOW US</SfButton>
        </CardFooterContent>
    </CardFooter>
</SfCard>
```
