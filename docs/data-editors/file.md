# File

The file control allows a user to upload a file and open to read.

## Example

```csharp
[UILayout]
public UIFileSource Field { get; set; } =  UIFileSource.CreateFromBytes("virtual-file.txt", () => Encoding.UTF8.GetBytes("Virtual file content."));
```

## Value Type

Automatically recognized in a form and the use of the `UIFileSource` attribute is NOT required. 

Acceptable types:
- `string` - path to a file
- `UIFileSource` - provides such information as file name and source

## Related attribute

`UIFile` - is related attribute.

Properties:
- Extensions - specifies acceptable file extensions, after a comma, for example ".jpg, .png".
- MaximumFileLength - maximum file length in bytes.

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