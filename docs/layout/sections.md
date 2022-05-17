# Sections

###  Example
```csharp
[UISections]
 public IList<object> Sections { get; }
```

## Value type

No automatically recognized types, **attribute `UISections` is required**.

## Related attribute

`UISections` - is related attribute.

Properties:
- `IdMember`
- `ViewMember`
- `DisplayMember`

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