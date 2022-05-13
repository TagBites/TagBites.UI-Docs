# Combobox

Represents a selection control with a drop-down list that can be displayed or hidden.

###  Example

```csharp
[UIDictionary(nameof(FieldDataSource))]
public string Field { get; set; }
public object FieldDataSource { get; }
```

## Value type

No automatically recognized types, **attribute `UIDictionary` is required**.

Acceptable types: TODO

Properties:
- `DataSourceProperty` - allows to provide a collection, which is displayed in control and selected value is binding with property
- `ValueMember` - key identifier
- `DisplayMember` - display name identifier
- `DisplayProviderType` - custom display provider
- `ViewType`

## Data source

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