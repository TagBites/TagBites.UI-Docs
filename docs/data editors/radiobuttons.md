# Radio buttons

### Example
```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Buttons)]
public string Field { get; set; }
public object FieldDataSource { get; }
```

## Value type

No automatically recognized types, **attribute `UIDictionary` is required**.

Acceptable types: Any type, if the parse fails, the default value is set.

## Related attribute

`UIDictionary` - is related attribute with a `ViewType` property set to `UIDictionaryViewType.Buttons` value.