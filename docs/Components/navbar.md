# Navbar

**Supported platforms**: Web (Blazor), Windows (WinForms)

**Behavior control attribute:**  `UINavBarAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

###  Example
```csharp
[UINavBar]
public object NavBars { get; set; }
```

## Parameters setting

| Parameter | `UINavBarAttribute` property | 
| -----------|:------------- 
| Item group | `ItemGroupMember` |
| Item icon | `ItemIconMember` |
| Item Display | `ItemDisplayMember` |
| Item link | `ItemLinkMember` |
| Group source | `GroupSourceProperty` |
| Group id | `GroupIdMember` |
| Group icon | `GroupIconMember` |
| Group display | `GroupDisplayMember` |
| Active item | `ActiveItemProperty` |

// TODO