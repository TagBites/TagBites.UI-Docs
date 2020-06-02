# Custom control

**Supported platforms**: Web (Blazor), Android (Xamarin.Forms), iOS(Xamarin.Forms), Windows (WinForms)

**Behavior control attribute:**  `UIEditorAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`

### Example
```csharp
[UIEditorAttribute(typeof(CustomControl))]
public object CustomControlField { get; set; }
```

// TODO