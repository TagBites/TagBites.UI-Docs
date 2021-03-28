# Date time

**Behavior control attribute:**  `UIDateTimeAttribute`

**Types automatically recognized:** `DateTime` and `DateTime?`

**Acceptable types**: `DateTime` and `DateTime?`

### Example
```csharp
[UILayout]
public DateTime DateTime { get; set; }
```

## Parameters setting

| Parameter | `UIDateTimeAttribute` property | 
| -----------|:------------- 
| Date time type | `UIDateTimeType` |

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

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |