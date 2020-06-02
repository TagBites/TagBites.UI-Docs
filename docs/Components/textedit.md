# Text edit

**Supported platforms**: Web (Blazor), Android (Xamarin.Forms), iOS(Xamarin.Forms), Windows (WinForms)

**Behavior control attribute:**  `UIStringAttribute`

**Types automatically recognized:** `string`

**Acceptable types**: `string`

###  Example
```csharp
[UILayout]
public string Text { get; set; }
```

## Parameters setting

| Parameter | `UIStringAttribute` property | 
| -----------|:------------- 
| String type | `UIStringType` |
| Maximum length | `MaximumLength` |
| Minimum line count | `MinimumLineCount` |
| Maximum line count | `MaximumLineCount` |
| Horizontal alignment | `HorizontalAlignment` |


## String type

| UIStringType | Description | 
| ------------- |:------------- 
| `None` | Specifies that a text is not formatted in any specific way. |
| `Multiline` | Specifies that a text is presented in multi lines.  |
| `Code` | Specifies that a text is presented as code. The code syntax is determined from property `CodeSyntax`. |
| `Password` | Specifies that a text is presented as password. |
| `Email` | Specifies that a text is formatted as a email. |
| `Telephone` | Specifies that a text is formatted as a telephone. |
| `Url` | Specifies that a text is formatted as a url. |

**Note:** The default is `UIStringType.None`.

```csharp
[UIString(UIStringType.None)]
public string TextLine { get; set; }

[UIString(UIStringType.Multiline)]
public string TextMultiline { get; set; }

[UIString(UIStringType.Code, CodeSyntax = "C#")]
public string Code { get; set; }

[UIString(UIStringType.Password)]
public string Password { get; set; }

[UIString(UIStringType.Email)]
public string Email { get; set; }

[UIString(UIStringType.Telephone)]
public string Telephone { get; set; }

[UIString(UIStringType.Url)]
public string Url { get; set; }
```

## Maximum length
```csharp
[UIString(MaximumLength = 10)]
public string Text { get; set; }
```

## Minimum and maximum line count
```csharp
[UIString(MinimumLineCount = 2, MaximumLineCount = 10)]
public string Text { get; set; }
```

## Horizontal alignment

| HorizontalAlignment | Description | 
| ------------- |:------------- 
| `Default`     | Specifies that a text is aligned in the default way. |
| `Near`     | Specifies that a text is aligned near the layout. In a left-to-right layout, the near position is left. In a right-to-left layout, the near position is right. |
| `Center`     | Specifies that a text is aligned in the center. |
| `Far`     | Specifies that a text is aligned far from the origin position of the layout rectangle. In a left-to-right layout, the far position is right. In a right-to-left layout, the far position is left. |

**Note:** The default is `UIStringAttribute.Default`.

```csharp
[UIString(HorizontalAlignment = UIStringAlignment.Default)]
public string TextDefault { get; set; }

[UIString(HorizontalAlignment = UIStringAlignment.Near)]
public string TextNear { get; set; }

[UIString(HorizontalAlignment = UIStringAlignment.Center)]
public string TextCenter { get; set; }

[UIString(HorizontalAlignment = UIStringAlignment.Far)]
public string TextFar { get; set; }
```