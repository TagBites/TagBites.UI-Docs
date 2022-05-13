# Look up 

###  Example
```csharp
[UILookup]
public object Field { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UILookup` is required**.

Acceptable types: Any type

## Related attribute

`UILookup` - is related attribute.

Properties:
- `ItemLookupType`
- `ItemLookupProperty`
- `ValueMember`
- `DisplayMember`
- `DisplayProviderType`

## Item look up type

```csharp
[UILookup(typeof(ItemLookup))]
public object Field { get; set; }

private class ItemLookup : IItemLookup 
{ /* Implementations */ }
```

## Item look up property

```csharp
[UILookup(nameof(ItemLookupProvider))]
public object Field { get; set; }
public ItemLookup ItemLookupProvider { get; set; }

private class ItemLookup : IItemLookup 
{ /* Implementations */ }
```

## Value

```csharp
[UILookup(ValueMember = "Value")]
public object Field { get; set; }
```

## Display

Display parameter can be set as:
* dynamic value using binding with `DisplayMember` property.

```csharp
[UILookup(DisplayMember = "Display")]
public object Field { get; set; }
```

* provider, which implements `IDisplayNameProvider` interface, using `DisplayProviderType` property.

```csharp
[UILookup(DisplayProviderType = typeof(DisplayProvider))]
public string Field { get; set; }

private class DisplayProvider : IDisplayProvider 
{ /* Implementations */ }
```