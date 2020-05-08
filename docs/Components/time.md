# Time

A time field is implemented for `public` property of `TimeSpan` type and nullable variant with `UILayoutAttribute` attribute.

```csharp
[UILayout]
public TimeSpan TimeSpan { get; set; }

[UILayout]
public TimeSpan? NullableTimeSpan { get; set; }
```

To customize text field with settings like e.g. minimum or maximum value the property requires `UITimeSpanAttribute` attribute.

**Note:** The `UILayoutAttribute` attribute is not required if property has the `UITimeSpanAttribute` attribute, unless it defines location of a field (e.g. row and column).


## Time span type
`UITimeSpanAttribute` requires setting the time span type with `UITimeSpanType`.

| UITimeSpanType    | Description           | 
| ------------- |:------------- 
| `PositiveOrNegative` | Specifies whether a time span is positive or negative. |
| `Positive` | specifies  Positive `TimeSpan` |
| `TimeOfDay` | Specifies a timespan Time of day format  |

### Example
```csharp
[UITimeSpan(UITimeSpanType.PositiveOrNegative)]
public TimeSpan TimeOfDay { get; set; }

[UITimeSpan(UITimeSpanType.Positive)]
public TimeSpan TimeOfDayWithMinutes { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay)]
public TimeSpan TimeOfDayWithSeconds { get; set; }
```

## Precision
`UITimeSpanAttribute` allows to define precision of `TimeSpan`.
The default is `UITimeSpanPrecision.Minutes`.

| UITimeSpanPrecision | Description | 
| ------------- |:------------- 
| `Milliseconds` | Milliseconds precision |
| `Seconds` | Seconds precision |
| `Minutes` | Minutes precision |
| `Hours` | Hours precision|

### Example
```csharp
[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Milliseconds)]
public TimeSpan TimeOfDay { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Seconds)]
public TimeSpan TimeOfDayWithMinutes { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Minutes)]
public TimeSpan TimeOfDayWithSeconds { get; set; }

[UITimeSpan(UITimeSpanType.TimeOfDay, Precision = UITimeSpanPrecision.Hours)]
public TimeSpan TimeOfDayWithSeconds { get; set; }
```