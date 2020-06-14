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
| Allow null | `AllowNull` |
| Tokens| `Tokens` |

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

## Allow null
A control allows to clear a selected value using `AllowNull` property.

```csharp
[UIDictionary(nameof(FieldDataSource), AllowNull = true)]
public int? Field { get; set; }
public object FieldDataSource { get; }
```

## Tokens
A control can be used in token mode if property `Tokens` is set to **true**.

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", Tokens = true)]
public string Field { get; set; }
public object FieldDataSource { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |