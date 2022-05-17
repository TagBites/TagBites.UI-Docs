# Custom control

### Example
```csharp
[UIEditor(typeof(CustomControl))]
public object CustomControlField { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UIEditor` is required**.

Acceptable types: Any type, if the parse fails, the default value is set.

## Related attribute

`UIEditor` - is related attribute.

Properties:
- `EditorType`
- `EditorTypeName`
- `EditorValuePropertyName`
- `OneWayBinding`

## Editor type

Editor type parameter can be set as:
* `Type` of custom control using `EditorType` property

```csharp
[UIEditor(typeof(CustomControl))]
public object CustomControlField { get; set; }
```

* type name of custom control using `EditorTypeName` property

```csharp
[UIEditor(nameof(CustomControl))]
public object CustomControlField { get; set; }
```

## Editor value property 

```csharp
[UIEditor(typeof(CustomControl), nameof(CustomControl.Text))]
public object CustomControlField { get; set; }
```

## One way binding

```csharp
[UIEditor(typeof(CustomControl), OneWayBinding = true)]
public object CustomControlField { get; set; }
```