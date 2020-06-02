# Web view

**Supported platforms**: Android (Xamarin.Forms), iOS(Xamarin.Forms), Windows (WinForms)

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
| Url | `BaseUrl` or `BaseUrlProperty` |
| Script | `ScriptObjectProperty` |
| Allow navigation | `AllowNavigation` |

// TODO

## Source type

|` UIWebSourceType`    | Description | 
| ------------- |:------------- 
| `Auto` |  |
| `Url` |  |
| `Content` |  |

**Note:** The default is `UIWebSourceType.Auto`.

## Url

## Script

## Allow navigation
