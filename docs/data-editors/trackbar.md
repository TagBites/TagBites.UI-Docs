# Track bar

The track bar control allows a user to select a numeric value by selecting a position on the bar.

## Example
```csharp
[UINumeric(ViewType = UINumericViewType.TrackBar, Minimum = 0, Maximum = 100)]
public decimal Field { get; set; } = 25;
```

## Value type

No automatically recognized types, **attribute `UINumeric` is required**.

Acceptable types: Any type, if the parse fails, the default value is set.

## Related attribute

`UINumeric` - is related attribute with a `ViewType` property set to `UINumericViewType.TrackBar` value.