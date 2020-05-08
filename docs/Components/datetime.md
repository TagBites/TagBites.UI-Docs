# DateTime

A date time field is implemented for `public` property of `TimeSpan` type and nullable variant with `UILayoutAttribute` attribute.

```csharp
[UILayout]
public DateTime DateTime { get; set; }

[UILayout]
public DateTime? NullableDate { get; set; }
```

To customize text field with settings like e.g. minimum or maximum value the property requires `UIDateTimeAttribute` attribute.

**Note:** The `UILayoutAttribute` attribute is not required if property has the `UIDateTimeAttribute` attribute, unless it defines location of a field (e.g. row and column).

## Date time type
`UIDateTimeAttribute` requires setting the date time type with `UIDateTimeType`.

| UIDateTimeType    | Description | 
| ------------- |:------------- 
| `DateTime` | Specifies a standard date time format. |
| `Date` | Specifies a date format with time value set to 12:00:00 midnight. |
| `Month` | Specifies a month format. |

### Example
```csharp
[UIDateTime(UIDateTimeType.DateTime)]
public DateTime Date { get; set; }

[UIDateTime(UIDateTimeType.Date)]
public DateTime Date { get; set; }

[UIDateTime(UIDateTimeType.Month)]
public DateTime Month { get; set; }
```