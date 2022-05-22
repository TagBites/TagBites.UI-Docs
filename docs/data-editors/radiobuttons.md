# Radio buttons

The radio button control allows a user to make a choice among a number of options. The control may have several selection modes.

## Example
```csharp
[UIDictionary(nameof(FieldDataSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Buttons)]
public string Field { get; set; }
public object FieldDataSource { get; } = new List<KeyValuePair<string, string>>()
{
    new("#csharp", "C#"),
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

`UIDictionary` - is related attribute with a `ViewType` property set to `UIDictionaryViewType.Buttons` value.

## Selection mode

### One or none option selection

To allow the user to select at most one option, set the `SelectMode` property to `UISelectMode.OneOrNone`.

```csharp
[UIDictionary(nameof(TagSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Buttons, SelectMode = UISelectMode.OneOrNone)]
public string OneTagOrNone { get; set; }
public object TagSource { get; } = new List<KeyValuePair<string, string>>()
{
    new("#csharp", "C#"),
    new("#programing", "Programing"),
    new("#vs", "Visual Studio"),
    new("#vs-pro", "Visual Studio Pro"),
    new("#vs2022", "Visual Studio 2022")
};
```

### One option selection

To allow the user to select only one option, set the `SelectMode` property to `UISelectMode.OneOrNone`.

```csharp
[UIDictionary(nameof(TagSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Buttons, SelectMode = UISelectMode.One)]
public string OneTag { get; set; } = "#csharp";
public object TagSource { get; } = new List<KeyValuePair<string, string>>()
{
    new("#csharp", "C#"),
    new("#programing", "Programing"),
    new("#vs", "Visual Studio"),
    new("#vs-pro", "Visual Studio Pro"),
    new("#vs2022", "Visual Studio 2022")
};
```

### Many tags selection

To allow the user to select any number of options, especially none or all, set the `SelectMode` property to` UISelectMode.OneOrNone`.

```csharp
[UIDictionary(nameof(TagSource), ValueMember = "Key", DisplayMember = "Value", ViewType = UIDictionaryViewType.Buttons)]
public IList<string> ManyTags { get; set; } = new[] { "#programing", "#vs-pro" };
public object TagSource { get; } = new List<KeyValuePair<string, string>>()
{
    new("#csharp", "C#"),
    new("#programing", "Programing"),
    new("#vs", "Visual Studio"),
    new("#vs-pro", "Visual Studio Pro"),
    new("#vs2022", "Visual Studio 2022")
};
```