# Search bar

###  Example
```csharp
[UISearch]
public object SearchField { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UISearch` is required**.

Acceptable types: `object`, `string`

## Related attribute

`UISearch` - is related attribute.

Properties:
- `ProgressProperty`
- `TargetProperty`

## Progress

```csharp
[UISearch(ProgressProperty = nameof(Progress))]
public object SearchField { get; set; }
public double Progress { get; set; }
```

## Target control

```csharp
[UISearch(TargetProperty = nameof(Items))]
public object SearchField { get; set; }
public object Items { get; set; }
```