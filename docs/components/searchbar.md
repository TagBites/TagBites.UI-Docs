# Search bar

**Behavior control attribute:**  `UISearchAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `string`

###  Example
```csharp
[UISearch]
public object SearchField { get; set; }
```

## Parameters setting

| Parameter | `UISearchAttribute` property | 
| -----------|:------------- 
| Progress | `ProgressProperty` |

## Progress

```csharp
[UISearch(ProgressProperty = nameof(Progress))]
public object SearchField { get; set; }
public double Progress { get; set; }
```


| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |