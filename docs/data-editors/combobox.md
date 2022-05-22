# Combobox

Represents a selection control with a drop-down list that can be displayed or hidden.

##  Example

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value")]
public int? Field { get; set; }
public object FieldDataSource { get; }= new List<KeyValuePair<int?, string>>()
{
    new (null, "Empty"),
    new (0, "Item 1"),
    new (1, "Item 2"),
    new (2, "Item 3")
};
```

## Value type

No automatically recognized types, **attribute `UIDictionary` is required**.

Acceptable types: TODO

Properties:
- `DataSourceProperty` - allows to provide a collection, which is displayed in control and selected value is binding with property
- `ValueMember` - key identifier
- `DisplayMember` - display name identifier
- `DisplayProviderType` - custom display provider
- `ViewType` - 

## Data source

```csharp
[UIDictionary(nameof(FieldDataSource))]
public string Field { get; set; }
public object FieldDataSource { get; } = new[] { "Empty", "Item 1", "Item 2", "Item 3" };
```

## Value and display properties

A data source can provide collections containing complex types, in which case it is necessary to indicate properties that act as key identifiers (`ValueMember`) and display names (`DisplayMember`).

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value")]
public int? Field { get; set; }
public object FieldDataSource { get; }= new List<KeyValuePair<int?, string>>()
{
    new (null, "Empty"),
    new (0, "Item 1"),
    new (1, "Item 2"),
    new (2, "Item 3")
};
```

## Custom display provider
A control can use custom display provider by using a user-defined class, which implements `IDisplayProvider` interface.

```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", DisplayProviderType = typeof(DisplayProvider))]
public int Field { get; set; } = 2;
public object FieldDataSource { get; } = new[]
{
    new KeyValuePair<int, int>(1, 1),
    new KeyValuePair<int, int>(2, 2),
    new KeyValuePair<int, int>(3, 3),
    new KeyValuePair<int, int>(4, 4)
};


private class DisplayProvider : TagBites.UI.Components.IDisplayProvider
{
    public string GetName(object obj)
    {
        if (obj is not int value || value == 0)
            return "None";

        return $"{value} - {new string('A', value)}";
    }
    public string GetShortName(object obj) => null;
    public string GetDescription(object obj) => null;
}
```

## View type
|` ViewType`    | Description | 
| ------------- |:------------- 
| `Default` | Specifies that a control is a standard combo box. |
| `Tokens` | Specifies that a control is a tokens selector. |
| `Buttons` | Specifies that a control is a radio buttons. |

**Note:** The default is `UIDictionaryViewType.Default`.

Examples of using the view [Tokens](tokens.md) and [Buttons](buttons.md).