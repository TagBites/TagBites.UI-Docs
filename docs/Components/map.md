# Map

**Behavior control attribute:**  `UIMapAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`

### Example

```csharp
[UIMap]
public object Map { get; set; }
```

## Parameters setting

| Parameter | `UIDateTimeAttribute` property | 
| -----------|:------------- 
| Show user location | `ShowUserLocation` |

## Show user location 

```csharp
[UIMap(ShowUserLocation = true)]
public object Map { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |