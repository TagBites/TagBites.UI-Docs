# Date time range

The date time range allows users to select a start date time and end date time of the range.

## Example

```csharp
[UILayout]
public DateTimeRange Field { get; set; } = new(DateTime.Now.Date, DateTime.Now.Date + TimeSpan.FromDays(7));
```

## Value type

Automatically recognized in a form and the use of the `UIDateTimeRange` attribute is NOT required.

Acceptable types: `TagBites.UI.DateTimeRange`, `TagBites.UI.DateTimeRange?`, `object`.

## Related attribute

`UIDateTimeRange` - is related attribute.