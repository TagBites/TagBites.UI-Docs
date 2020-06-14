# Tabs

**Behavior control attribute:**  `UITabsAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

### Example
```csharp
[UITabs]
public object Tabs { get; }
```

## Parameters setting
| Parameter | `UITabsAttribute` property | 
| -----------|:------------- 
| Active view | `ActiveViewProperty` |

**Note:** `UITabsAttribute` inherits from `UISectionsAttribute`.

## Active view
```csharp
[UITabs(ActiveViewProperty = nameof(ActiveTab))]
public object Tabs { get; }
public object ActiveTab { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |