# Combobox

**Behavior control attribute:**  `UIDictionaryAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

###  Example
```csharp
[UIDictionary(nameof(FieldDataSource))]
public string Field { get; set; }
public object FieldDataSource { get; }
```

## Parameters setting

| Parameter | `UIStringAttribute` property | 
| -----------|:------------- 
| Data source | `DataSourceProperty` |
| Value and display values  | `ValueMember` and `DisplayMember`|
| Custom display provider | `DisplayProviderType` |
| View type | `ViewType` |

## Data source

Parameter allows to provide a collection, which is displayed in control and selected value is binding with property.

```csharp
[UIDictionary(nameof(FieldDataSource))]
public string Field { get; set; }
public object FieldDataSource { get; }
```

## Value and display properties

A data source can provide collections containing complex types, in which case it is necessary to indicate properties that act as key identifiers (`ValueMember`) and display names (`DisplayMember`).

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value")]
public int? Field { get; set; }
public object FieldDataSource { get; }
```

## Custom display provider
A control can use custom display provider by using a user-defined class, which implements `IDisplayProvider` interface.

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", DisplayProviderType = typeof(DisplayProvider))]
public int Field { get; set; }
public IList<KeyValuePair<int, int>> FieldDataSource

private class DisplayProvider : IDisplayProvider
{
    public string GetName(object obj) => // custom name
    public string GetShortName(object obj) => // custom short name
    public string GetDescription(object obj) => // custom description
}
```

## View type
|` ViewType`    | Description | 
| ------------- |:------------- 
| `Default` | Specifies that a control is a standard combo box. |
| `Tokens` | Specifies that a control is a tokens selector. |
| `Buttons` | Specifies that a control is a radio buttons. |

**Note:** The default is `UIDictionaryViewType.Default`.

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Tokens)]
public string Field { get; set; }
public object FieldDataSource { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |