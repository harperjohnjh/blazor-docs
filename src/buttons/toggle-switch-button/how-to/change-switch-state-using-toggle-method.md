---
title: "Toggle between the states"
component: "Toggle Switch Button"
description: "This section explains how to toggle between the states using toggle method in Blazor."
---

# Change Toggle Switch Button state using toggle method

This section explains about how to toggle between the Toggle Switch Button states using [`Toggle`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.Buttons.SfSwitch~Toggle.html) method.

```csharp

@using Syncfusion.Blazor.Buttons

<SfSwitch OffLabel="OFF" OnLabel="ON" Created="create" @ref="SwitchObj"></SfSwitch>

@code{
    SfSwitch SwitchObj;
    private void create(object obj)
    {
        SwitchObj.Toggle();
    }
}

```

Output be like

![Switch Sample](./../images/switch-toggle.png)

> Switch triggers [`OnChange`](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor~Syncfusion.Blazor.Buttons.SfSwitch~OnChange.html) event on every state stage to perform custom operations.