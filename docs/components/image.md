# Image

**Behavior control attribute:**  `UIImageAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `UIUrlImage`, `UIResourceImage`, enum with `UIIconFontResource` attribute

### Example
```csharp
[UIImage]
public object Image { get; set; }
```

## Parameters setting

| Parameter | `UIDateTimeAttribute` property | 
| -----------|:------------- 
| Width and height | `Width` and `Height` |

## Width and height
```csharp
[UIImage(Height = 200, Width = 200)]
public object Image { get; set; }
```

## Using `UIUrlImage`, `UIResourceImage`, enum with `UIIconFontResource` types

```csharp
[UIImage]
public object UrlImage { get; } = new UIUrlImage("https://www.tagbites.com/images/favicon.png");
```

```csharp
[UIImage]
public object ResourceImage { get; } = new UIResourceImage(typeof(LoginExample), "TagBites.UI.Demo.Resources.Images.logo.png");
```

```csharp
[UIImage]
public object IconImage { get; } = MaterialIcons.Watch;
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |