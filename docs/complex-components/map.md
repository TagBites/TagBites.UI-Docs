# Map

## Example

```csharp
[UIMap]
public object Map { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UIMap` is required**.

Acceptable types: object

## Related attribute

`UIMap` - is related attribute.

Properties:
- `ShowUserLocation`

## Show user location 

```csharp
[UIMap(ShowUserLocation = true)]
public object Map { get; set; }
```