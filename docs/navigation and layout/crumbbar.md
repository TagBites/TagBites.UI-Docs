# Crumb bar

**Behavior control attribute:**  `UICrumbBarAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

### Example
```csharp
[UICrumbBar]
public object CrumbBar { get; set; }
```

## Parameters setting

| Parameter | `UIDateTimeAttribute` property | 
| -----------|:------------- 
| Display | `DisplayMember` |
| Link | `LinkMember` |

## Display

```csharp
[UICrumbBar("DisplayName")]
public object CrumbBar { get; set; }
```

## Link

```csharp
[UICrumbBar("DisplayName", "Link")]
public object CrumbBar { get; set; }
```