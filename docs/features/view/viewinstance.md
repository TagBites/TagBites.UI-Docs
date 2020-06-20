# View instance

**Behavior control attribute:**  `UIViewAttribute`

### Example

```csharp
[UIView(ViewInstanceProperty = nameof(WindowInstance)]
public class ViewExample
{
    public object WindowInstance { get; set; }
}
```