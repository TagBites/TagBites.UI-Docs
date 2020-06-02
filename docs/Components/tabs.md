# CheckBox

**Supported platforms**: Web (Blazor), Android (Xamarin.Forms), iOS(Xamarin.Forms), Windows (WinForms)

**Behavior control attribute:**  `UITabsAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

### Example
```csharp
[UITabs]
public IList<object> Tabs { get; }
```

## Parameters setting
| Parameter | `UITabsAttribute` property | 
| -----------|:------------- 
| Active view | `ActiveViewProperty` |
| Id and view members  | `IdMember` and `ViewMember` |

// TODO