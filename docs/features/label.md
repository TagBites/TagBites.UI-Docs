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
| Link | `Link` or `LinkProperty` or `LinkCommandName` or `LinkProviderType` |
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

## Link

Link parameter can be set with:

* constant value using `Link` property

```csharp
[UILabel(Link = "www.tagbites.com")]
public string Label { get; set; }
```

* dynamic value using binding with `LinkProperty` property

```csharp
[UILabel(LinkProperty = nameof(LabelLink))]
public string Label { get; set; }
public string LabelLink { get; set; }
```

* command which should be executed on click

```csharp
[UILabel(LinkCommandName = nameof(LinkCommand))]
public string Label { get; set; }

[UICommand]
public void LinkCommand() { /* action */ }
```

* provider, which implements `ILinkProvider` interface, using `LinkProviderType` property.

```csharp
[UILabel(LinkProviderType = typeof(LinkProvider))]
public string Label { get; set; }

private class LinkProvider : ILinkProvider 
{ /* Implementations */ }
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