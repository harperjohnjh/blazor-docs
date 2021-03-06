# Accessibility

## Keyboard Interaction

The following shortcut keys are used to access the Chip control without any interruption.

| Keyboard shortcuts | Actions |
|------------|-------------------|
| <kbd>Enter</kbd> | Selects the targeted chip from the Chip/ChipItems. |
| <kbd>Delete</kbd> | Deletes the targeted chip from the Chip/ChipItems. |

```csharp
@using Syncfusion.Blazor.Buttons
<SfChip ID="chip-avatar" EnableDelete="true" CssClass="e-chip-avatar" Selection="SelectionType.Single">
    <ChipItems>
        <ChipItem Text="Andrew" LeadingIconCss='andrew'></ChipItem>
        <ChipItem Text="Janet" LeadingIconCss='janet'></ChipItem>
        <ChipItem Text="Laura" LeadingIconCss='laura'></ChipItem>
        <ChipItem Text="Margaret" LeadingIconCss='margaret'></ChipItem>
    </ChipItems>
</SfChip>

<style>
    #chip-avatar .andrew {
        background-image: url('./andrew.png')
    }

    #chip-avatar .margaret {
        background-image: url('./margaret.png')
    }

    #chip-avatar .laura {
        background-image: url('./laura.png')
    }

    #chip-avatar .janet {
        background-image: url('./janet.png')
    }
</style>

```

Output be like the below.

![Chip with avatarIcon and selection](./images/accessibility.gif)