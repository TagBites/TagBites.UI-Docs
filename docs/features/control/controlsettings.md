# Control settings

**Behavior control attribute:**  `UIEditorSettingAttribute`

### Example

```csharp
[UIEditorSetting("SettingsName", "SettingsValue")]
public string Field { get; set; }
```

## Parameters setting

| Parameter | `UIEditorSettingAttribute` property | 
| -----------|:------------- 
| Settings name | `Name` |
| Settings value | `Value` |