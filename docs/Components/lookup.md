# Look up 

**Supported platforms**: Web (Blazor), Android (Xamarin.Forms), iOS(Xamarin.Forms), Windows (WinForms)

**Behavior control attribute:**  `UILookupAttribute`

**Types automatically recognized:** None

**Acceptable types**: Any type

###  Example
```csharp
[UILookup(typeof(SelectModel))]
public object Field { get; set; }
```

## Parameters setting

| Parameter | `UIDateTimeAttribute` property | 
| -----------|:------------- 
| Item lookup | `ItemLookupProperty` |
| Item lookup type | `ItemLookupType` |
| Value and display values  | `ValueMember` and `DisplayMember`|

// TODO