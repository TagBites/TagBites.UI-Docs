# Sections

**Behavior control attribute:**  `UISectionsAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

### Example
```csharp
[UISections]
public object Sections { get; }
```

## Parameters setting
| Parameter | `UISectionsAttribute` property | 
| -----------|:------------- 
| Id member| `IdMember` |
| View member | `ViewMember` |
| Display member | `DisplayMember` |

## Id member

```csharp
[UISections(IdMember = "Id")]
public object Sections { get; }
```

## View 

```csharp
[UISections("ViewMember")]
public object Sections { get; }
```

## Display member

```csharp
[UISections("ViewMember", "DisplayMember")]
public object Sections { get; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |