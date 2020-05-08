# Numeric

A numeric field is implemented for `public` property of `byte`, `short`, `int`, `decimal`, `double` and `float` type and nullable variants with `UILayoutAttribute` attribute.

```csharp
[UILayout]
public byte Byte { get; set; }
[UILayout]
public byte? NullableByte { get; set; }

[UILayout]
public short Short { get; set; }
[UILayout]
public short? NullableShort { get; set; }

[UILayout]
public int Integer { get; set; }
[UILayout]
public int? NullableInteger { get; set; }

[UILayout]
public decimal Decimal { get; set; }
[UILayout]
public decimal? NullableDecimal { get; set; }

[UILayout]
public double Double { get; set; }
[UILayout]
public double? NullableDouble { get; set; }

[UILayout]
public double Float { get; set; }
[UILayout]
public double? NullableFloat { get; set; }
```

To customize numeric field with settings like e.g. minimum or maximum value the property requires `UINumericAttribute` attribute.

**Note:** The `UILayoutAttribute` attribute is not required if property has the `UINumericAttribute` attribute, unless it defines location of a field (e.g. row and column).

## Minimum and maximum values
`UINumericAttribute` allows to defines a minimum and maximum values. Both of these can be set as a constant values (`Minimum` nad `Maximum`) or using properties (`MinimumProperty` nad `MaximumProperty`), which enable for dynamic range change.

### Constant minimum and maximum values example
```csharp
[UINumeric(Minimum = 0, Maximum = 100)]
public decimal Field { get; set; }
```

### Dynamic minimum and maximum values example
```csharp
[UINumeric(MinimumProperty = nameof(Minimum), MaximumProperty = nameof(Maximum))]
public decimal Field { get; set; }
public decimal Minimum => 0;
public decimal Maximum => 100;
```

## Decimal places
`UINumericAttribute` allows to set a decimal places of value both through the `DecimalPlaces` property as a constant value and `DecimalPlacesProperty` property as a bound value.

### Constant decimal place value example
```csharp
[UINumeric(DecimalPlaces = 2)]
public decimal Field { get; set; }
```

### Dynamic decimal place value example
```csharp
[UINumeric(DecimalPlacesProperty = nameof(DecimalPlace))]
public decimal Field { get; set; }
public decimal DecimalPlace => 2;
```

## View type
Numeric value can be presented both as standard numeric edit field and as a track bar. To use a special view type set the `ViewType` property of `UINumericAttribute`to value `UINumericViewType.TrackBar`.

### TrackBar view example
```csharp
[UINumeric(ViewType = UINumericViewType.TrackBar, Minimum = 0, Maximum = 100)]
public decimal Field { get; set; }
```

## Unit
Numeric value can be displayed with unit. It can be set by either as constant value (`Unit`) or bind with property (`UnitProperty`) or using a 
custom class, which implements `IDisplayProvider` interface.

### Constant unit value example
```csharp
[UINumeric(Unit = "USD")]
public decimal Field { get; set; }
```

### Dynamic unit value example
```csharp
[UINumeric(UnitProperty = nameof(Unit))]
public decimal Field { get; set; }
public string Unit { get; set; }
```

### Unit display provider example
```csharp
[UINumeric(UnitDisplayProviderType = typeof(DisplayProvider))]
public decimal Field { get; set; }


private class DisplayProvider : IDisplayProvider
{
    public string GetName(object obj)
    {
        return obj is int ? string.Format("U{0}", obj) : null;
    }
    public string GetShortName(object obj) => null;
    public string GetDescription(object obj) => null;
}
```