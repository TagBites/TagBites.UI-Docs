# Date time picker

The date time picker allows users to select a date, date time or month.

## Example

```csharp
[UILayout]
public DateTime DateTime { get; set; } = DateTime.Now;
```

## Value type

Automatically recognized in a form and the use of the `UIDateTime` attribute is NOT required.

Acceptable types: `DateTime` and `DateTime?`.

## Related attribute

`UIDateTime` - is related attribute.

Properties:
- `UIDateTimeType` - specifies the type of a date time.


## Date time type

|` UIDateTimeType`    | Description | 
| ------------- |:------------- 
| `DateTime` | Specifies a standard date time format. |
| `Date` | Specifies a date format with time value set to 12:00:00 midnight. |
| `Month` | Specifies a month format. |

**Note:** The default is `UIDateTimeType.DateTime`.

```csharp
[UIDateTime(UIDateTimeType.DateTime)]
public DateTime DateTime { get; set; } = DateTime.Now;

[UIDateTime(UIDateTimeType.Date)]
public DateTime Date { get; set; } = DateTime.Now;

[UIDateTime(UIDateTimeType.Month)]
public DateTime Month { get; set; } = DateTime.Now;
```