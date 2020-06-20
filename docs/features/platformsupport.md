# Platform support

**Behavior control attribute:** `UISupportedOnAttribute`

**Usage**: all

### Example

```csharp
[UISupported]
public string Field { get; set; }
```

## Parameters setting

| Parameter | `UISupportedOnAttribute` property | 
| -----------|:------------- 
| Platform kind | `PlatformKind` |
| Except | `Except` |
| System name | `SystemName` |

## Platform kind

|` UIPlatformKind`    | Description | 
| ------------- |:------------- 
| `Desktop` | Specifies that element is not supported on desktop. |
| `Mobile` | Specifies that element is not supported on mobile. |
| `Web` | Specifies that element is not supported on web. |

```csharp
[UISupported(UIPlatformKind.Mobile)]
public string Field { get; set; }
```

## Except

```csharp
[UISupported(UIPlatformKind.Mobile, Except = true)]
public string Field { get; set; }
```

## System name

```csharp
[UISupported(UIPlatformKind.Desktop, SystemName = "Windows")]
public string Field { get; set; }
```