# Date time picker

A date time picker lets users select a date, date time or month.

### Example

```csharp
[UILayout]
public DateTime DateTime { get; set; }
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
public DateTime DateTime { get; set; }

[UIDateTime(UIDateTimeType.Date)]
public DateTime Date { get; set; }

[UIDateTime(UIDateTimeType.Month)]
public DateTime Month { get; set; }
```