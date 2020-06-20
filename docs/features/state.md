# State

**Behavior control attribute:**  `UIStateAttribute`

**Usage**: class

### Example

```csharp
[UIState(nameof(StateContainer))]
public class Example
{
    public IDictionary<string, object> StateContainer { get; set; }
}
```

## Parameters setting

| Parameter | `UIStateAttribute` property | 
| -----------|:------------- 
| State container | `StateContainerProperty` |
| Propagate state container | `PropagateStateContainer` |

## State container

```csharp
[UIState(nameof(StateContainer))]
public class Example
{
    public IDictionary<string, object> StateContainer { get; set; }
}
```

## Propagate state container

```csharp
[UIState(nameof(StateContainer), true)]
public class Example
{
    public IDictionary<string, object> StateContainer { get; set; }
}
```
