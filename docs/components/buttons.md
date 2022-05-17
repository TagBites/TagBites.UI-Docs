# Buttons


###  Example
```csharp
[UIButtons]
public IList<string> Commands { get; set; } = new[] { nameof(Alarm), nameof(AccountBalance), nameof(MultilineChart) };


[UICommand(UICommandSection.Hidden), UIIcon(MaterialIcons.AccessAlarm)]
public IUICommandResult Alarm() {/*action*/}

[UICommand(UICommandSection.Hidden), UIIcon(MaterialIcons.AccountBalance)]
public IUICommandResult AccountBalance() {/*action*/}

[UICommand(UICommandSection.Hidden), UIIcon(MaterialIcons.MultilineChart)]
public IUICommandResult MultilineChart() {/*action*/}
```

## Value Type

No automatically recognized types, **attribute `UIButtons` is required**.

Acceptable types:

## Related attribute

`Buttons` - is related attribute.

Properties:
- `ViewType`
- `LinkMember`
- `IconMember`
- `CaptionMember`
- `ColorMember`
- `Columns`
- `ButtonWidth`
- `ButtonHeight`
- `Alignment`
- `IconsOnTop`
- `NoMargins`

## View type

|` ViewType`    | Description | 
| ------------- |:------------- 
| `NormalButtons` | Specifies that a control is a track bar. |
| `Toolbox` | Specifies that a control presents small buttons containing only icons |
| `Grid` | Specifies that a control is a track bar. |
| `IconsGrid` | Specifies that a control is a track bar. |

**Note:** The default is `UIButtonsViewType.NormalButtons`.

```csharp
[UIButtons(ViewType = UINumericViewType.TrackBar, Minimum = 0, Maximum = 100)]
public decimal Field { get; set; }
```
