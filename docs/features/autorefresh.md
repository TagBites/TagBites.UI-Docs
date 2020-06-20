# Auto refresh

**Behavior control attribute:**  `UIAutoRefreshAttribute`

**Usage**: class

### Example

```csharp
[UIAutoRefresh]
public class Example
{ }
```

## Parameters setting

| Parameter | `UIAutoRefreshAttribute` property | 
| -----------|:------------- 
| Interval | `Interval` |
| OnRefresh | `OnRefresh` |

## Interval

```csharp
[UIAutoRefresh(Interval = 60)]
public class Example
{ }
```

## OnRefresh
```csharp
[UIAutoRefresh(Interval = 200, OnRefresh = nameof(OnRefresh))]
public class Example
{ 
    public void OnRefresh()
    { }
}
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |