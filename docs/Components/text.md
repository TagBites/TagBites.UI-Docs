# Text

A text field is implemented for `public` property of `string` type with `UILayoutAttribute` attribute.

```csharp
[UILayout]
public string Text { get; set; }
```

To customize text field with settings like e.g. minimum or maximum value the property requires `UIStringAttribute` attribute.

**Note:** The `UILayoutAttribute` attribute is not required if property has the `UIStringAttribute` attribute, unless it defines location of a field (e.g. row and column).


## String type
`UIStringAttribute` allows to set a type of sting. The default is `UIStringType.None`.

| UIStringType | Description | 
| ------------- |:------------- 
| `None` | Specifies that a text is not formatted in any specific way. |
| `Multiline` | Specifies that a text is presented in multi lines.  |
| `Code` | Specifies that a text is presented as code. The code syntax is determined from property `CodeSyntax`. |
| `Password` | Specifies that a text is presented as password. |
| `Email` | Specifies that a text is formatted as a email. |
| `Telephone` | Specifies that a text is formatted as a telephone. |
| `Url` | Specifies that a text is formatted as a arl. |

### Example
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
`UIStringAttribute` allows to set a maximum length of text. The default is 32767.

### Example
```csharp
[UIString(MaximumLength = 10)]
public string Text { get; set; }
```

## Minimum and maximum line count
`UIStringAttribute` allows to set a minimum line count and maximum line count.

### Example
```csharp
[UIString(MinimumLineCount = 2, MaximumLineCount = 10)]
public string Text { get; set; }
```

## Horizontal alignment
`UIStringAttribute` allows to set a horizontal alignment of a text string relative to its layout rectangle.

| HorizontalAlignment | Description | 
| ------------- |:------------- 
| `Default`     | Specifies that a text is aligned in the default way. |
| `Near`     | Specifies that a text is aligned near the layout. In a left-to-right layout, the near position is left. In a right-to-left layout, the near position is right. |
| `Center`     | Specifies that a text is aligned in the center. |
| `Far`     | Specifies that a text is aligned far from the origin position of the layout rectangle. In a left-to-right layout, the far position is right. In a right-to-left layout, the far position is left. |

### Example

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