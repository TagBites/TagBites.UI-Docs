# Control binding

**Behavior control attribute:**  `UIEditorCommandBindingAttribute`

### Example

```csharp
[UIEditorBinding("Loaded", nameof(CustomCommand))]
public string Field { get; set; }

[UICommand]
public void CustomCommand() { }
```

## Parameters setting

| Parameter | `UIEditorCommandBindingAttribute` property | 
| -----------|:------------- 
| Event name | `ControlEventName` |
| Command name | `CommandName` |