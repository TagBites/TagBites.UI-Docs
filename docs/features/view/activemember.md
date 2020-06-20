# Active member

**Behavior control attribute:**  `UIViewAttribute`

### Example

```csharp
[UIView(ActiveMemberProperty = nameof(ActiveMember)]
public class ViewExample
{
    [UILayout]
    public string ActiveMember { get; set; }
}
```