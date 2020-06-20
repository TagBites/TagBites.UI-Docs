# Start up member

**Behavior control attribute:**  `UIViewAttribute`

### Example

```csharp
[UIView(StartupActiveMember = nameof(Field)]
public class ViewExample
{
    [UILayout]
    public string Field { get; set; }
}
```