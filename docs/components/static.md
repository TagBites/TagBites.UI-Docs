# Static

**Behavior control attribute:**  `UIStaticAttribute`

**Types automatically recognized:** None

**Acceptable types**: `string`

###  Example
```csharp
[UIStatic]
public string StaticField { get; set; }
```

## Parameters setting

| Parameter | `UITextAttribute` property | 
| -----------|:------------- 
| Text | `TextProperty` or `TextProviderType`  |
| Link | `Link` or `LinkProperty` or `LinkCommandName` or`LinkProviderType` |

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

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |