# Access

**Behavior control attribute:**  `UIAccessAttribute`

**Usage**: property or class

### Example

```csharp
[UIAccess]
public string Field { get; set; }
```

## Parameters setting

| Parameter | `UIAccessAttribute` property | 
| -----------|:------------- 
| Used related properties | `UseRelatedProperties` |
| Read access | `ReadValue` or `ReadProperty` |
| Write access | `WriteValue` or `WriteProperty` |

## Used related properties

```csharp
[UIAccess(UseRelatedProperties = false)]
public string Field { get; set; }
```

**Note:** The default parameter value is `true`.

## Read access

Read access parameter can be set as:
* constant value using `ReadValue` property

```csharp
[UIAccess(ReadValue = false)]
public string Field { get; set; }
```

* dynamic value using binding with `ReadProperty` property

```csharp
[UIAccess(ReadProperty = nameof(FieldReadAccess))]
public decimal Field { get; set; }
public bool FieldReadAccess { get; set; }
```

## Write access

Write access parameter can be set as:
* constant value using `WriteValue` property

```csharp
[UIAccess(WriteValue = false)]
public string Field { get; set; }
```

* dynamic value using binding with `WriteProperty` property

```csharp
[UIAccess(WriteProperty = nameof(FieldWriteAccess))]
public decimal Field { get; set; }
public bool FieldWriteAccess { get; set; }
```