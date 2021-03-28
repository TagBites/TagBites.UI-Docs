# Chart

**Behavior control attribute:**  `UIChartAttribute`

**Types automatically recognized:** none

**Acceptable types**: Collections of types `ValueTuple`, `Tuple` or `KeyValuePair` with two numeric values or three values where a first is string and two numerics or collections with custom types.

### Example

```csharp
[UIChart(UIChartViewType.Line)]
public List<(int, int)> Points { get; }
```

## Parameters setting

| Parameter | `UIListAttribute` property | 
| -----------|:------------- 
| View type | `ViewType` |
| Is rotated | `Rotated` |
| Arguments and values | `ArgumentMember` or `ValueMember` |
| Series | `SeriesMember` |

## View type

| Chart group | `UIChartViewType` | 
| ------------- |:------------- 
| Line | `Line`, `Spline`, `StepLine`, `StackedLine`, ` FullStackedLine`, |
| Area | `Area`, `SplineArea`, `StepArea`, `StackedArea`, ` StackedSplineArea`, `StackedStepArea`, `FullStackedArea`, `FullStackedSplineArea`, `FullStackedStepArea`|
| Bar | `Bar`, `StackedBar`, `FullStackedBar` |
| Points | `Point` |
| Pie | `Pie`, `Doughnut`, `NestedDoughnut` |
| Other | `Funnel` |

## Is rotated
A control allows to define if chart is rotated using `Rotated` property.

```csharp
[UIChart(UIChartViewType.Line, Rotated = true)]
public List<(int, int)> Points { get; }
```

## Arguments and values 
A data source can provide collections containing complex types, in which case it is necessary to indicate properties that act as argument (`ArgumentMember`) and value (`ValueMember`).

**Note:** If a type of the elements in a collection is `ValueTuple`, `Tuple` or `KeyValuePair` with two numeric values, the first value points to a argument and the second one to a value.

```csharp
[UIChart(UIChartViewType.Line, nameof(CustomModel.Argument), nameof(CustomModel.Value))]
public List<CustomModel> Custom { get; }
```

## Series
A data source can provide collections containing complex types, in this case, series can be indicated through `Series` property.

**Note:** If a type of the elements in a collection is `ValueTuple`, `Tuple` or `KeyValuePair` with tree values and the first is string, it points to series name.

```csharp
[UIChart(UIChartViewType.Line, nameof(CustomModel.Series), nameof(CustomModel.Argument), nameof(CustomModel.Value))]
public List<CustomModel> CustomWithSeries { get; }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) |  |
| iOS (Xamarin.Forms) |  |
| Windows (WinForms) | &check; |