# Custom control

**Behavior control attribute:**  `UIEditorAttribute`

**Types automatically recognized:** None

**Acceptable types**: Any type, if the parse fails, the default value is set.

### Example
```csharp
[UIEditor(typeof(CustomControl))]
public object CustomControlField { get; set; }
```

## Parameters setting

| Parameter | `UIEditorAttribute` property | 
| -----------|:------------- 
| Editor type | `EditorType` or `EditorTypeName`|
| Editor value property | `EditorValuePropertyName`|
| One way binding | `OneWayBinding`|

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

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |