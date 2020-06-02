# Track bar

**Supported platforms**: Web (Blazor), Android (Xamarin.Forms), iOS(Xamarin.Forms), Windows (WinForms)

**Behavior control attribute:**  `UINumericAttribute`

**Types automatically recognized:** `byte`, `short`, `int`, `decimal`, `double` `float` and nullable variants (`byte?`, `short?`, `int?`, `decimal?`, `double?`, `float?`)

**Acceptable types**: Any type, if the parse fails, the default value is set.

### Example
```csharp
[UINumeric(ViewType = UINumericViewType.TrackBar, Minimum = 0, Maximum = 100)]
public decimal Field { get; set; }
```

**Note:** TrackBar is a numeric with a `ViewType` property set to `UINumericViewType.TrackBar` value.