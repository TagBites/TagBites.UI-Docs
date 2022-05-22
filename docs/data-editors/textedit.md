# Text edit

The text edit control control allows a user to edit text value.

##  Example
```csharp
[UILayout]
public string Text { get; set; }
```

## Value Type

Automatically recognized types: `string`

Automatically recognized in a form and the use of the `UIString` attribute is NOT required.

Acceptable types: `string`

Properties:
- `UIStringType`
- `CodeSyntax`
- `MaximumLength`
- `MinimumLineCount`
- `MaximumLineCount`
- `Alignment`

## String type

| UIStringType | Description | 
| ------------- |:------------- 
| `None` | Specifies that a text is not formatted in any specific way. |
| `Multiline` | Specifies that a text is presented in multi lines.  |
| `Code` | Specifies that a text is presented as code. The code syntax is determined from property `CodeSyntax`. |
| `Password` | Specifies that a text is presented as password. |
| `Email` | Specifies that a text is formatted as a email. |
| `Phone` | Specifies that a text is formatted as a phone number. |
| `Url` | Specifies that a text is formatted as a url. |

**Note:** The default is `UIStringType.None`.

```csharp
[UILayout]
[UIString(UIStringType.None)]
public string None { get; set; } = "None";

[UILayout]
[UIString(UIStringType.Multiline)]
public string Multiline { get; set; } = "Multiline\ntext";

[UILayout]
[UIString(UIStringType.Code, CodeSyntax = "C#")]
public string Code { get; set; } = "[UILayout]\npublic string Text { get; set; }";

[UILayout]
[UIString(UIStringType.Password)]
public string Password { get; set; } = "Test password";

[UILayout]
[UIString(UIStringType.Email)]
public string Email { get; set; } = "support@tagbites.com";

[UILayout]
[UIString(UIStringType.Phone)]
public string Phone { get; set; } = "(12)34567890";

[UILayout]
[UIString(UIStringType.Url)]
public string Url { get; set; } = "www.tagbites.com";
```

## Maximum length
```csharp
[UIString(MaximumLength = 10)]
public string TextMaximumLength { get; set; } = "Maximum 10";
```

## Minimum and maximum line count
```csharp
[UIString(MinimumLineCount = 2, MaximumLineCount = 10)]
public string TextWith2To10Lines { get; set; } = "Text\nWith\n2\nTo\n10\nLines";
```

## Horizontal alignment

| Alignment | Description | 
| ------------- |:------------- 
| `Start`     | Specifies that a text is aligned near the layout. In a left-to-right layout, the near position is left. In a right-to-left layout, the near position is right. |
| `Center`     | Specifies that a text is aligned in the center. |
| `End`     | Specifies that a text is aligned far from the origin position of the layout rectangle. In a left-to-right layout, the far position is right. In a right-to-left layout, the far position is left. |

**Note:** The default is `UIAlignment.Start`.

```csharp
[UILayout]
[UIString(Alignment = UIAlignment.Start)]
public string Start { get; set; } = "Start";

[UILayout]
[UIString(Alignment = UIAlignment.Center)]
public string Center { get; set; } = "Center";

[UILayout]
[UIString(Alignment = UIAlignment.End)]
public string End { get; set; } = "End";
```