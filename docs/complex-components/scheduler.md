# Scheduler

### Example

```csharp
[UIScheduler]
public IList<Item> Items { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UIScheduler` is required**.

Acceptable types:
- `object`
- `IEnumerable` implementations

Properties:
- `IntervalProperty`
- `GroupingProperty`
- `ItemIdMember`
- `ItemResourceIdMember`
- `ItemStartMember`
- `ItemEndMember`
- `ItemSubjectMember`
- `ItemDescriptionMember`
- `ItemColorMember`
- `ItemPercentCompleteMember`
- `ResourceIdMember`
- `ResourceCaptionMember`
- `EnterCommand`
- `UpdateCommand`
- `CreateCommand`