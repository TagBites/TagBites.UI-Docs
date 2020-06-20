# Description

**Behavior control attribute:**  `UIDescriptionAttribute`

**Types automatically recognized:** None.

**Acceptable types**: `string`

### Example

```csharp
[UIDescription(CustomText = "Custom text")]
public string Field { get; set; }
```

## Parameters setting

| Parameter | `UIDescriptionAttribute` property | 
| -----------|:------------- 
| Text | `CustomText` or `DescriptionProperty` or `DescriptionProviderType` |
| Show | `Show` |

## Text

Text parameter can be set as:

* constant value using `CustomText` property
```csharp
[UIDescription(CustomText = "Custom tool tip")]
public string Field { get; set; }
```

* dynamic value using binding with `DescriptionProperty`

```csharp
[UIDescription(DescriptionProperty = nameof(FieldDescription))]
public string Field { get; set; }
public string FieldDescription { get; set; }
```

* provider, which implements `IDisplayNameProvider` interface, using `DescriptionProviderType` property.

```csharp
[UIDescription(DescriptionProviderType = typeof(DescriptionProvider))]
public string Field { get; set; }

private class DescriptionProvider : IDisplayNameProvider 
{ /* Implementations */ }
```

## Show

```csharp
[UIDescription(Show = false)]
public string Field { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | |
| iOS(Xamarin.Forms), Windows (WinForms) | |
| Windows (WinForms) | &check; |