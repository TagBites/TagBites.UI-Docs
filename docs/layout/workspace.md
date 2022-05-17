# Workspace

###  Example
```csharp
[UIWorkspace]
public object Field { get; set; }
```
## Value Type

No automatically recognized types, **attribute `UIWorkspace` is required**.

## Related attribute

`UIWorkspace` - is related attribute.

Acceptable types:
- `object`
- `IEnumerable` implementations

Properties:
- `ViewType`
- `ActiveWindowProperty`
- `ActivePanelProperty`
- `IdMember`
- `ViewMember`
- `IsPanelMember`

## View type

|` UIWorkspaceViewType`    | Description | 
| ------------- |:------------- 
| `Tabbed` | Specifies that a workspace is tabbed view. |
| `Widget` | Specifies that a workspace is widget view. |

**Note:** The default is `UIWorkspaceViewType.Tabbed`.

## Active window

```csharp
[UIWorkspace(nameof(ActiveWindow))]
public object Windows { get; }
public object ActiveWindow { get; set; }
```

## Active panel

```csharp
[UIWorkspace(ActivePanelProperty = nameof(ActivePanelProperty))]
public object Windows { get; }
public object ActivePanelProperty { get; set; }
```

## Id member 

```csharp
[UIWorkspace(IdMember = "IdMember")]
public object Windows { get; }
```

## View member

```csharp
[UIWorkspace(ViewMember = "Content"))]
public object Windows { get; }
```

## Is panel

```csharp
[UIWorkspace(IsPanelMember = "IsPanelMember")]
public object Windows { get; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | |
| iOS (Xamarin.Forms) | |
| Windows (WinForms) | &check; |