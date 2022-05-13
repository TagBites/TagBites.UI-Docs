# Text

###  Example
```csharp
[UIText]
public string Text { get; set; }
```

## Value type

No automatically recognized types, **attribute `UIText` is required**.

Acceptable types: Any type, if the parse fails, the default value is set.

## Related attribute

`UIText` - is related attribute

Properties:
- `ViewType`
- `HorizontalAlignment`
- `VerticalAlignment`

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