# Tabs

### Example
```csharp
[UITabs]
public object Tabs { get; }
```
## Value Type

No automatically recognized types, **attribute `UITabs` is required**.

Acceptable types:
- `object`, 
- `IEnumerable` implementations

## Related attribute

`UITabs` - is related attribute.

Properties:
- `ActiveViewProperty`

**Note:** `UITabsAttribute` inherits from `UISectionsAttribute`.

## Active view
```csharp
[UITabs(ActiveViewProperty = nameof(ActiveTab))]
public object Tabs { get; }
public object ActiveTab { get; set; }
```