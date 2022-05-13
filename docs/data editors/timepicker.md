# Time picker

A time picker lets users select a time.

### Example
```csharp
[UILayout]
public TimeSpan TimeSpan { get; set; }
```

## Value type

Automatically recognized in a form and the use of the `UITimeSpan` attribute is NOT required.

Acceptable types: `TimeSpan` and `TimeSpan?`.

## Related attribute

`UITimeSpan` - is related attribute.

Properties:
- `TimeSpanType` - specifies the type of a time.
- `Precision` - precision.

## Time span type

| `UITimeSpanType` | Description | 
| ------------- |:------------- 
| `PositiveOrNegative` | Specifies whether a time span is positive or negative. |
| `Positive` | Specifies positive `TimeSpan`. |
| `TimeOfDay` | Specifies time of day format. |

```csharp
[UITimeSpan(UITimeSpanType.PositiveOrNegative)]
public TimeSpan PositiveOrNegative { get; set; }

[UITimeSpan(UITimeSpanType.Positive)]
public TimeSpan Positive { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay)]
public TimeSpan TimeOfDay { get; set; }
```

## Precision

| `UITimeSpanPrecision` | Description | 
| ------------- |:------------- 
| `Milliseconds` | Specifies that value is in milliseconds precision. |
| `Seconds` | Specifies that value is in seconds precision. |
| `Minutes` | Specifies that value is in minutes precision. |
| `Hours` | Specifies that value is in hours precision. |

**Note:** The default is `UITimeSpanPrecision.Minutes`.

```csharp
[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Milliseconds)]
public TimeSpan TimeOfDay { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Seconds)]
public TimeSpan TimeOfDayWithSeconds { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Minutes)]
public TimeSpan TimeOfDayWithMinutes { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Hours)]
public TimeSpan TimeOfDayWithHours { get; set; }
```