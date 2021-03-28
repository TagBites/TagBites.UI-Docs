# File

**Behavior control attribute:**  `UIFileAttribute`

**Types automatically recognized:** `UIFileSource`

**Acceptable types**: `UIFileSource`

### Example

```csharp
[UILayout]
public UIFileSource File { get; set; }
```

## Parameters setting

| Parameter | `UIFileAttribute` property | 
| -----------|:------------- 
| Extensions | `Extensions` |
| Maximum file length | `MaximumFileLength` |

## Extensions

```csharp
[UIFile(Extensions = ".jpg, .png")]
public UIFileSource ImageFile { get; set; }
```

## Maximum file length

```csharp
[UIFile(Extensions = ".jpg, .png", MaximumFileLength = 16 * 1024)]
public UIFileSource ImageFileUpTo16Kb { get; set; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS (Xamarin.Forms) | &check; |
| Windows (WinForms) | &check; |