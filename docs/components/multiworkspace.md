# Multi workspace

**Behavior control attribute:**  `UIMultiWorkspaceAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

###  Example
```csharp
[UIMultiWorkspace]
public object Workspaces { get; set; }
```

## Parameters setting

| Parameter | `UIMultiWorkspaceAttribute` property | 
| -----------|:------------- 
| Active workspace | `ActiveWorkspaceProperty` |
| Id member | `IdMember` |

## Active workspace

```csharp
[UIMultiWorkspace(nameof(ActiveWorkspace))]
public object Workspaces { get; set; }
public object ActiveWorkspace { get; set; }
```

## Id member

```csharp
[UIMultiWorkspace(IdMember = "IdMember")]
public object Workspaces { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) ||
| iOS(Xamarin.Forms), Windows (WinForms) ||
| Windows (WinForms) | &check; |