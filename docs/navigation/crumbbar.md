# Crumb bar

### Example
```csharp
[UICrumbBar]
public object CrumbBar { get; set; }
```

## Value type

No automatically recognized types, **attribute `UICrumbBar` is required**.

Acceptable types:
- `object`
- `IEnumerable` implementations

## Related attribute

`UICrumbBar` - is related attribute.

Properties:
- `DisplayMember`
- `LinkMember`

## Display

```csharp
[UICrumbBar("DisplayName")]
public object CrumbBar { get; set; }
```

## Link

```csharp
[UICrumbBar("DisplayName", "Link")]
public object CrumbBar { get; set; }
```