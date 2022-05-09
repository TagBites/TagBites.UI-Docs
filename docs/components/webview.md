# Web view

**Behavior control attribute:**  `UIWebSourceAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `string`

###  Example
```csharp
[UIWebSource]
public string Field { get; set; }
```

## Parameters setting

| Parameter | `UINumericAttribute` property | 
| -----------|:------------- 
| Source type | `SourceType` |
| Script | `ScriptObjectProperty` |
| Url | `BaseUrl` or `BaseUrlProperty` |
| Allow navigation | `AllowNavigation` |

## Source type

|` UIWebSourceType` | Description | 
| ------------- |:------------- 
| `Auto` | Specifies that the web source is auto type. |
| `Url` | Specifies that the web source is url. |
| `Content` | Specifies that the web source is html content. |

**Note:** The default is `UIWebSourceType.Auto`.

```csharp
[UIWebSource(UIWebSourceType.Content)]
public string WebSource { get; set; }
```

## Script

```csharp
[UIWebSource(ScriptObjectProperty = nameof(ScriptObject))]
public string WebSource { get; set; }
public string ScriptObject { get; set; }
```

## Url

Url parameter can be set as:
* constant value using `BaseUrl` property

```csharp
[UIWebSource(BaseUrl = "https://www.tagbites.com")]
public string WebSource { get; set; }
```

* dynamic value using binding with `BaseUrlProperty` property.

```csharp
[UIWebSource(BaseUrlProperty = nameof(Url))]
public string WebSource { get; set; }
public string Url {get; set;}
```

```csharp
[UIWebSource(ScriptObjectProperty = nameof(ScriptObject))]
public string WebSource { get; set; }
public string ScriptObject { get; set; }
```

## Allow navigation

```csharp
[UIWebSource(AllowNavigation = true)]
public string WebSource { get; set; }
```


| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |