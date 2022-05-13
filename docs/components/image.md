# Image

### Example
```csharp
[UIImage]
public object Image { get; set; }
```
## Value Type

No automatically recognized types, **attribute `UIImage` is required**.

Acceptable types: `object`, `UIUrlImage`, `UIResourceImage`, enum with `UIIconFontResource` attribute

## Related attribute

`UIImage` - is related attribute.


Properties:
- `Width`
- `Height`

## Width and height
```csharp
[UIImage(Height = 200, Width = 200)]
public object Image { get; set; }
```

## More examples

### Using `UIUrlImage`, `UIResourceImage`, enum with `UIIconFontResource` types

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