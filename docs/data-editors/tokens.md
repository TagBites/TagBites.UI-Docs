# Tokens

The tokens control allows a user to select the tokens.

## Example
```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Tokens)]
public string Field { get; set; } = "#csharp, #programing, #vs, as";
public object FieldDataSource { get; } = new List<KeyValuePair<string, string>>()
{
    new("#csharp", "csharp"),
    new("#programing", "Programing"),
    new("#vs", "Visual Studio"),
    new("#vs-pro", "Visual Studio Pro"),
    new("#vs2022", "Visual Studio 2022")
};
```

## Value type

No automatically recognized types, **attribute `UIDictionary` is required**.

Acceptable types: Any type, if the parse fails, the default value is set.

## Related attribute

`UIDictionary` - is related attribute with a `ViewType` property set to `UIDictionaryViewType.Tokens` value.

**Note**: `SelectMode` property is not respected, a user can chooses as many token as he wants.