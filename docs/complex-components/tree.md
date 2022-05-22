# Tree

##  Example
```csharp
[UITree("ParentMember", "ChildNodesMember")]
public object Tree { get; set; }
```

## Value Type

No automatically recognized types, **attribute `UITree` is required**.

Acceptable types: 
- `object`, 
- `IEnumerable` implementations

## Related attribute

`UITree` - is related attribute.

Properties:
- `KeyMember`
- `ParentMember`
- `ChildNodesMember`
- `IsLeafMember`
- `ForceRecursiveView`
- `SkipRootDataSource`
- `ViewType`
- `ReadOnly`
- `ReadOnlyProperty`
- `Editable`
- `ShowMenu`
- `ShowFind`
- `ShowDetails`
- `ShowColumns`
- `SelectMode`
- `DetailsViewMember`
- `FindFilterTextProperty`
- `FocusedRowProperty`
- `SelectedRowsProperty`
- `AddCommand`
- `AddChildCommand`
- `DeleteCommand`
- `EnterCommand`

## Key

```csharp
[UITree("ParentMember", "ChildNodesMember", true)]
public object Tree { get; set; }
```

## Parent and Child nodes

```csharp
[UITree("ParentMember", "ChildNodesMember")]
public object Tree { get; set; }
```

## Is leaf

```csharp
[UITree("ParentMember", "ChildNodesMember", IsLeafMember = "IsLeafMember")]
public object Tree { get; set; }
```

## Recursive view

```csharp
[UITree("ParentMember", "ChildNodesMember", ForceRecursiveView = true)]
public object Tree { get; set; }
```

## Skip root data source

```csharp
[UITree("ParentMember", "ChildNodesMember", SkipRootDataSource = true)]
public object Tree { get; set; }
```

## View type

|` UIListViewType` | Description | 
| ------------- |:------------- 
| `List` | Specifies that a tree is presented as standard list with columns. |
| `ListWithDetails` | Specifies that a tree is presented as master-detail list.|
| `ListView` | Specifies that a tree is presented as list with rows with grid organized content. |

**Note:** The default is `UIListViewType.List`.

```csharp
[UITree(UIListViewType.ListView, "ParentMember", "ChildNodesMember")]
public object Tree { get; set; }
```

## ReadOnly

```csharp
[UITree("ParentMember", "ChildNodesMember", Readonly = true)]
public object Tree { get; set; }
```

## Editable

```csharp
[UITree("ParentMember", "ChildNodesMember", Editable = false)]
public object Tree { get; set; }
```

**Note:** The default parameter value is `true`.

## Show menu

```csharp
[UITree("ParentMember", "ChildNodesMember", ShowMenu = true)]
public object Tree { get; set; }
```

**Note:** The default parameter value is from `UIFrameworkConfig.ListAttributeShowMenuDefault` setting.

## Show find

```csharp
[UITree("ParentMember", "ChildNodesMember", ShowFind = true)]
public object Tree { get; set; }
```

## Show details

```csharp
[UITree("ParentMember", "ChildNodesMember", ShowDetails = true)]
public object Tree { get; set; }
```

## Show columns

```csharp
[UITree("ParentMember", "ChildNodesMember", ShowColumns = true)]
public object Tree { get; set; }
```

**Note:** The default parameter value is `true`.

## Select mode

|` UIListSelectMode` | Description | 
| ------------- |:------------- 
| `OneRecord` | Specifies that only one record can be selected. |
| `ManyRecords` | Specifies that many records can be selected.  |
| `OneCell` | Specifies that a only one cell can be selected. |
| `ManyCells` | Specifies that many cell can be selected.  |
| `CheckBoxes` | Specifies that a tree is presented with column with check boxes.  |
| `None` | Specifies that selection is not supported.  |

**Note:** The default is `UIListSelectMode.OneRecord`.

```csharp
[UITree("ParentMember", "ChildNodesMember", SelectMode = UIListSelectMode.OneRecord)]
public object Tree { get; set; }
```

## Details view member

```csharp
[UITree("ParentMember", "ChildNodesMember", DetailsViewMember = "DetailsView")]
public object Tree { get; set; }
```

## Find filter text

```csharp
[UITree("ParentMember", "ChildNodesMember", FindFilterTextProperty = nameof(FindFilterText))]
public object Tree { get; set; }
public string FindFilterText { get; set; }
```

## Focused row

```csharp
[UITree("ParentMember", "ChildNodesMember", FocusedRowProperty = nameof(FocusedRow))]
public object Tree { get; set; }
public object FocusedRow { get; set; }
```

## Selected rows

```csharp
[UITree("ParentMember", "ChildNodesMember", SelectedRowsProperty = nameof(SelectedRows))]
public object Tree { get; set; }
public IList SelectedRows { get; set; }
```

## Add command

```csharp
[UITree("ParentMember", "ChildNodesMember", AddCommand = nameof(Add))]
public object Tree { get; set; }

[UICommand]
public void Add() => { /*action*/ }
```

## Add child command

```csharp
[UITree("ParentMember", "ChildNodesMember", AddChildCommand = nameof(AddChild))]
public object Tree { get; set; }

[UICommand]
public void AddChild() => { /*action*/ }
```

## Delete command

```csharp
[UITree("ParentMember", "ChildNodesMember", DeleteCommand = nameof(Delete))]
public object Tree { get; set; }

[UICommand]
public void Delete() => { /*action*/ }
```

## Enter command

```csharp
[UITree("ParentMember", "ChildNodesMember", EnterCommand = nameof(Enter))]
public object Tree { get; set; }

[UICommand]
public void Enter() => { /*action*/ }
```