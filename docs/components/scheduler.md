# Scheduler

**Behavior control attribute:**  `UISchedulerAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

### Example

```csharp
[UIScheduler]
public IList<Item> Items { get; set; }
```

## Parameters setting

| Parameter | `UISchedulerAttribute` property | 
| -----------|:------------- 
| Extensions | `IntervalProperty` |
| x | `GroupingProperty` |
| x | `ItemIdMember` |
| x | `ItemResourceIdMember` |
| x | `ItemStartMember` |
| x | `ItemEndMember` |
| x | `ItemSubjectMember` |
| x | `ItemDescriptionMember` |
| x | `ItemColorMember` |
| x | `ItemPercentCompleteMember` |
| x | `ResourceIdMember` |
| x | `ResourceCaptionMember` |

| x | `EnterCommand` |
| x | `UpdateCommand` |
| x | `CreateCommand` |


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
| Android (Xamarin.Forms) |  |
| iOS (Xamarin.Forms) |  |
| Windows (WinForms) | &check; |