# Icons

**Behavior control attribute:**  `UIIconFontResourceAttribute`

**Usage**: enum

### Example

```csharp
[UIIconFontResource("Custom Icons", "CustomIcons.otf")]
public enum CustomIconFont
{ }
```

## Parameters setting

| Parameter | `UIStateAttribute` property | 
| -----------|:------------- 
| Font | `FontName` nad `FontPath` |
| Web url | `WebUrl` |
| Html class | `HtmlClass` |

## Font

```csharp
[UIIconFontResource("Custom Icons", "CustomIcons.otf")]
public enum CustomIconFont
{ }
```

## Web url

```csharp
[UIIconFontResource("Custom Icons", "CustomIcons.otf", WebUrl = "https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css")]
public enum CustomIconFont
{ }
```

## Html class

```csharp
[UIIconFontResource("Custom Icons", "CustomIcons.otf", HtmlClass = "custom")]
public enum CustomIconFont
{ }
```