# Alignment

**Behavior control attribute:**  `UIViewAttribute`

### Example
```csharp
[UILayout]
public DateTime DateTime { get; set; }
```

## Parameters setting

| Parameter | `UIViewAttribute` property | 
| -----------|:------------- 
| Horizontal and Vertical alignment | `Horizontal` and `Vertical` |

## Horizontal and Vertical alignment 

|` UIAlignment`    | Description | 
| ------------- |:------------- 
| `Start` | Specifies a standard date time format. |
| `Center` | Specifies a date format with time value set to 12:00:00 midnight. |
| `End` | Specifies a month format. |

**Note:** The default is `UIDateTimeType.DateTime`.
`

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
