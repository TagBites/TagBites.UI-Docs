# Workspace

**Supported platforms**: Windows (WinForms)

**Behavior control attribute:**  `UIWorkspaceAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

###  Example
```csharp
[UIWorkspace]
public object Field { get; set; }
```

## Parameters setting

| Parameter | `UIWorkspaceAttribute` property | 
| -----------|:------------- 
| View type | `ViewType` |
| Active window | `ActiveWindowProperty` |
| Active panel | `ActivePanelProperty` |
| Id member | `IdMember` |
| View member | `ViewMember` |
| Is panel | `IsPanelMember` |


## View type

|` UIWorkspaceViewType`    | Description | 
| ------------- |:------------- 
| `Tabbed` | Specifies that a workspace is tabbed view. |
| `Widget` | Specifies that a workspace is widget view.|

**Note:** The default is `UIDateTimeType.DateTime`.

## Active window
## Active panel
## Id member 
## View member
## Is panel