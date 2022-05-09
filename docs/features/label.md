# Label

**Behavior control attribute:**  `UILabelAttribute`

**Usage**: property

### Example

```csharp
[UILabel]
public string Text { get ;set }
```

## Parameters setting

| Parameter | `UILabelAttribute` property | 
| -----------|:------------- 
| Text | `Text` or `TextProperty` |
| Color | `Color` or `ColorProperty` |
| Show | `Show` |

## Text

Text parameter can be set with:

* constant value using `Text` property

```csharp
[UILabel(Text = "Custom text")]
public string Label { get; set; }
```

* dynamic value using binding with `TextProperty` property

```csharp
[UILabel(TextProperty = nameof(LabelText))]
public string Label { get; set; }
public string LabelText { get; set; }
```

## Color

Color parameter can be set with:

* constant value using `Color` property

```csharp
[UILabel(Color = UIColorNames.Blue)]
public string Label { get; set; }
```

* dynamic value using binding with `ColorProperty` property

```csharp
[UILabel(ColorProperty = nameof(LabelColor))]
public string Label { get; set; }
public string LabelColor { get; set; }
```

## Show

```csharp
[UILabel(Show = false)]
public string Label { get; set; }
```