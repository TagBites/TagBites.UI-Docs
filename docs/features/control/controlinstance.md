# View instance

**Behavior control attribute:**  `UIControlInstanceAttribute`

### Example

```csharp
[UIControlInstance(nameof(CustomControlInstance))]
public string Field { get; set; }
public object CustomControlInstance { get; }
```

## Parameters setting

| Parameter | `UIControlInstanceAttribute` property | 
| -----------|:------------- 
| Instance | `InstanceProperty` |