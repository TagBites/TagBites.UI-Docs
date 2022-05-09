# Text

**Behavior control attribute:**  `UITextAttribute`

**Types automatically recognized:** None

**Acceptable types**: `string`

###  Example
```csharp
[UIText]
public string Text { get; set; }
```

## Parameters setting

| Parameter | `UITextAttribute` property | 
| -----------|:------------- 
| View type | `ViewType` |
| Horizontal alignment | `HorizontalAlignment` |
| Vertical alignment | `VerticalAlignment` |

## View type

|` ViewType`    | Description | 
| ------------- |:------------- 
| `Default` | Specifies that a control is a standard text edit field. |
| `Badge` | Specifies that a control is a badge. |

**Note:** The default is `UITextViewType.Default`.

```csharp
[UIText(ViewType = UITextViewType.Badge)]
public string Field { get; set; }
```

## Horizontal alignment

|` TextAlignment` | Description | 
| ------------- |:------------- 
| `Start` | Specifies that a text is places at start of a available area. |
| `Center` | Specifies that a text is places in a center of a available area. |
| `End` | Specifies that a text is places at end of a available area. |

```csharp
[UIText(HorizontalAlignment = TextAlignment.Start)]
public string Text { get; set; }
```

## Vertical alignment

```csharp
[UIText(VerticalAlignment = TextAlignment.Center)]
public string Text { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms)| &check; |
| Windows (WinForms) | &check; |