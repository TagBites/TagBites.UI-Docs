# List

**Behavior control attribute:**  `UIListAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

###  Example
```csharp
[UIList]
public object Field { get; set; }
```

## Parameters setting

| Parameter | `UIListAttribute` property | 
| -----------|:------------- 
| View type | `ViewType` |
| ReadOnly | `ReadOnly` |
| Editable | `Editable` |
| Show menu | `ShowMenu` |
| Show find | `ShowFind` |
| Show details | `ShowDetails` |
| Show columns | `ShowColumns` |
| Select mode | `SelectMode` |
| Details view member | `DetailsViewMember` |
| Find filter text | `FindFilterTextProperty` |
| Focused row | `FocusedRowProperty` |
| Selected rows | `SelectedRowsProperty` |
| Add command | `AddCommand` |
| Add child command | `AddChildCommand` |
| Delete command | `DeleteCommand` |
| Enter command | `EnterCommand` |

## View type

|` UIListViewType` | Description | 
| ------------- |:------------- 
| `List` | Specifies that a list is presented as standard list with columns. |
| `ListWithDetails` | Specifies that a list is presented as master-detail list.|
| `ListView` | Specifies that a list is presented as list with rows with grid organized content. |

**Note:** The default is `UIListViewType.List`.

```csharp
[UIList(UIListViewType.ListView)]
public object Field { get; set; }
```

## ReadOnly

```csharp
[UIList(Readonly = true)]
public object Field { get; set; }
```

## Editable

```csharp
[UIList(Editable = false)]
public object Field { get; set; }
```

**Note:** The default parameter value is `true`.

## Show menu

```csharp
[UIList(ShowMenu = true)]
public object Field { get; set; }
```

**Note:** The default parameter value is from `UIFrameworkConfig.ListAttributeShowMenuDefault` setting.

## Show find

```csharp
[UIList(ShowFind = true)]
public object Field { get; set; }
```

## Show details

```csharp
[UIList(ShowDetails = true)]
public object Field { get; set; }
```

## Show columns

```csharp
[UIList(ShowColumns = true)]
public object Field { get; set; }
```

**Note:** The default parameter value is `true`.

## Select mode

|` UIListSelectMode` | Description | 
| ------------- |:------------- 
| `OneRecord` | Specifies that only one record can be selected. |
| `ManyRecords` | Specifies that many records can be selected.  |
| `OneCell` | Specifies that a only one cell can be selected. |
| `ManyCells` | Specifies that many cell can be selected.  |
| `CheckBoxes` | Specifies that a list is presented with column with check boxes.  |
| `None` | Specifies that selection is not supported.  |

**Note:** The default is `UIListSelectMode.OneRecord`.

```csharp
[UIList(SelectMode = UIListSelectMode.OneRecord)]
public object Field { get; set; }
```

## Details view member

```csharp
[UIList(DetailsViewMember = "DetailsView")]
public object Field { get; set; }
```

## Find filter text

```csharp
[UIList(FindFilterTextProperty = nameof(FindFilterText))]
public object Field { get; set; }
public string FindFilterText { get; set; }
```

## Focused row

```csharp
[UIList(FocusedRowProperty = nameof(FocusedRow))]
public object Field { get; set; }
public object FocusedRow { get; set; }
```

## Selected rows

```csharp
[UIList(SelectedRowsProperty = nameof(SelectedRows))]
public object Field { get; set; }
public IList SelectedRows { get; set; }
```

## Add command

```csharp
[UIList(AddCommand = nameof(Add))]
public object Field { get; set; }

[UICommand]
public void Add() => { /*action*/ }
```

## Add child command

```csharp
[UIList(AddChildCommand = nameof(AddChild))]
public object Field { get; set; }

[UICommand]
public void AddChild() => { /*action*/ }
```

## Delete command

```csharp
[UIList(DeleteCommand = nameof(Delete))]
public object Field { get; set; }

[UICommand]
public void Delete() => { /*action*/ }
```

## Enter command

```csharp
[UIList(EnterCommand = nameof(Enter))]
public object Field { get; set; }

[UICommand]
public void Enter() => { /*action*/ }
```


| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |