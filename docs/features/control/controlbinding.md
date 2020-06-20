# Control binding

**Behavior control attribute:**  `UIEditorBindingAttribute`

### Example

```csharp
[UIEditorBinding("BackColor"nameof(CustomColor))]
public string Field { get; set; }
public object CustomColor { get; }
```


## Parameters setting

| Parameter | `UIEditorBindingAttribute` property | 
| -----------|:------------- 
| Editor member | `EditorMember` |
| Model member | `ModelMember` |
| One way binding | `OneWayBinding` |