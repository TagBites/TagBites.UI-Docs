# Numeric

###  Example
```csharp
[UILayout]
public decimal Decimal { get; set; }
```

## Value type

Automatically recognized types: `byte`, `short`, `int`, `decimal`, `double` `float` and nullable variants (`byte?`, `short?`, `int?`, `decimal?`, `double?`, `float?`)

Acceptable types: Any type, if the parse fails, the default value is set.

## Related attribute

`UINumericAttribute` - is related attribute.

Properties:
- `Minimum` - constant value providing minimum value.
- `MinimumProperty`
- `Maximum` - constant value providing maximum value.
- `MaximumMinimumProperty`
- `DecimalPlaces`- constant value providing decimal places.
- `DecimalPlacesProperty`
- `Unit` - constant value providing unit name.
- `ViewType`

## Related properties

Automatically recognized suffixes are:
- `Minimum`, 
- `Maximum`, 
- `DecimalPlaces`,
- `Unit`

##  Minimum and maximum
Minimum and maximum parameters can be set as:
* constant values using `Minimum` and `Maximum` properties

```csharp
[UINumeric(Minimum = 0, Maximum = 100)]
public decimal Field { get; set; }
```

* dynamic values using binding with `MinimumProperty` and `MaximumProperty` properties:

```csharp
[UINumeric(MinimumProperty = nameof(FieldMinimum), MaximumProperty = nameof(FieldMaximum))]
public decimal Field { get; set; }
public decimal FieldMinimum => 0;
public decimal FieldMaximum => 100;
```

## Decimal places
Decimal places parameter can be set as:
* constant value using `DecimalPlaces` property

    ```csharp
    [UINumeric(DecimalPlaces = 2)]
    public decimal Field { get; set; }
    ```

* dynamic value using binding with `DecimalPlacesProperty` property.

    ```csharp
    [UINumeric(DecimalPlacesProperty = nameof(DecimalPlace))]
    public decimal Field { get; set; }
    public decimal DecimalPlace => 2;
    ```

## Unit

Unit parameter can be set as:
* constant value using `Unit` property

```csharp
[UINumeric(Unit = "USD")]
public decimal Field { get; set; }
```

* dynamic value using binding with `UnitProperty` property.

```csharp
[UINumeric(UnitProperty = nameof(Unit))]
public decimal Field { get; set; }
public string Unit { get; set; }
```

## View type

|` ViewType`    | Description | 
| ------------- |:------------- 
| `Default` | Specifies that a control is a standard numeric edit field. |
| `TrackBar` | Specifies that a control is a track bar. |

**Note:** The default is `ViewType.Default`.

```csharp
[UINumeric(ViewType = UINumericViewType.TrackBar, Minimum = 0, Maximum = 100)]
public decimal Field { get; set; }
```
