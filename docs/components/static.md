# Static

###  Example
```csharp
[UIStatic]
public string StaticField { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UIStatic` is required**.

## Related attribute

`UIStatic` - is related attribute.

Properties:
- `TextProperty`
- `TextProviderType`
- `Link`
- `LinkProperty`
- `LinkCommandName`
- `LinkProviderType`

## Text

Text parameter can be set with:

* dynamic value using binding with `TextProperty` property

```csharp
[UIStatic(TextProperty = nameof(Text))]
public string Field { get; set; }
public string Text { get; set; }
```

* provider, which implements `IDisplayNameProvider` interface, using `TextProviderType` property.

```csharp
[UIStatic(TextProviderType = typeof(DisplayProvider))]
public string Field { get; set; }

private class DisplayProvider : IDisplayProvider 
{ /* Implementations */ }
```

## Link

Link parameter can be set with:

* constant values using `Link` property

```csharp
[UIStatic(Link = "www.tagbites.com")]
public string Field { get; set; }
```

* dynamic value using binding with `LinkProperty` property

```csharp
[UIStatic(LinkProperty = nameof(Link))]
public string Field { get; set; }
public string Link { get; set; }
```

* command which should be executed on click

```csharp
[UIStatic(LinkCommandName = nameof(LinkCommand))]
public string Field { get; set; }

[UICommand]
public void LinkCommand() { /* action */ }
```

* provider, which implements `ILinkProvider` interface, using `LinkProviderType` property.

```csharp
[UIStatic(LinkProviderType = typeof(LinkProvider))]
public string Field { get; set; }

private class LinkProvider : ILinkProvider 
{ /* Implementations */ }
```