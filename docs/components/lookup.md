# Look up 

**Behavior control attribute:**  `UILookupAttribute`

**Types automatically recognized:** None

**Acceptable types**: Any type

###  Example
```csharp
[UILookup]
public object Field { get; set; }
```

## Parameters setting

| Parameter | `UIDateTimeAttribute` property | 
| -----------|:------------- 
| Item look up type | `ItemLookupType` |
| Item look up property | `ItemLookupProperty` |
| Value  | `ValueMember`|
| Display | `DisplayMember` or `DisplayProviderType`|

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

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |