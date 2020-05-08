# Combobox

A combobox is implemented using the `UIDictionaryAttribute` attribute, which is added to property, which should contain selected value. It requires to specify the property that will be the data source.

```csharp
[UIDictionary(nameof(FieldDataSource))]
public string Field { get; set; }
public object FieldDataSource { get; }

[UIDictionary(nameof(FieldDataSource))]
public string Field2 { get; set; }
public IList<Item> Field2DataSource { get; }
```

## ValueMember and DisplayMember

A data source can provide collections containing complex types, in which case it is necessary to indicate properties that act as key identifiers (`ValueMember`) and display names (`DisplayMember`).

### Example

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value")]
public int? Field { get; set; }
public object FieldDataSource { get; }
```

## Allow null
`UIDictionaryAttribute` attribute allows to clear a selected value using `AllowNull` property.

### Example
```csharp
[UIDictionary(nameof(FieldDataSource), AllowNull = true)]
public int? Field { get; set; }
public object FieldDataSource { get; }
```

## Custom IDisplayProvider
Providing a user-defined class, which implements `IDisplayProvider` interface enables to customized displaying names.

### Example
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

## Tokens
`UIDictionaryAttribute` attribute can defined control to be use in tokens mode. 

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", Tokens = true)]
public string Field { get; set; }
public object FieldDataSource { get; set; }
```