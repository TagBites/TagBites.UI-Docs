# Component extension

**Behavior control attribute:**  `UIExtensionAttribute`

**Usage**: property

### Example

```csharp
[UIExtensionAttribute(typeof(CustomExtension))]
public string Field { get; set; }


public class CustomExtension : IUIViewExtension
{
    /* Implementations */
}
```

## Parameters setting

| Parameter | `UIAccessAttribute` property | 
| -----------|:------------- 
| View extension | `ViewExtensionType` |