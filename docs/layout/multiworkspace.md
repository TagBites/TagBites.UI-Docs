# Multi workspace

### Example
```csharp
[UIMultiWorkspace]
public object Workspaces { get; set; }
```

## Value type

No automatically recognized types, **attribute `UIMultiWorkspace` is required**.

Acceptable types:
- `object`
- `IEnumerable` implementations

## Related attribute

`UIMultiWorkspace` - is related attribute.

Properties:
- `ActiveWorkspaceProperty`
- `IdMember`

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