# Navbar

**Behavior control attribute:**  `UINavBarAttribute`

**Types automatically recognized:** None

**Acceptable types**: `object`, `IEnumerable` implementations

###  Example
```csharp
[UINavBar]
public object NavBars { get; set; }
```

## Parameters setting

| Parameter | `UINavBarAttribute` property | 
| -----------|:------------- 
| Item group | `ItemGroupMember` |
| Item icon | `ItemIconMember` |
| Item display | `ItemDisplayMember` |
| Item link | `ItemLinkMember` |
| Group source | `GroupSourceProperty` |
| Group id | `GroupIdMember` |
| Group icon | `GroupIconMember` |
| Group display | `GroupDisplayMember` |
| Active item | `ActiveItemProperty` |
| Is find field shown | `ShowFind` |
| Enter command | `EnterCommand` |

## Item group

```csharp
[UINavBar("GroupId")]
public object NavBars { get; set; }
```

## Item icon

```csharp
[UINavBar(ItemIconMember = "ItemIcon")]
public object NavBars { get; set; }
```

## Item display

```csharp
[UINavBar(ItemDisplayMember = "ItemDisplay")]
public object NavBars { get; set; }
```

## Item link 

```csharp
[UINavBar(ItemLinkMember = "ItemLink")]
public object NavBars { get; set; }
```

## Group source and Group id

```csharp
[UINavBar("ItemGroupId", nameof(Groups), "GroupId")]
public object NavBars { get; set; }
public object Groups { get; set; }
```

## Group icon

```csharp
[UINavBar(GroupIconMember = "GroupIcon")]
public object NavBars { get; set; }
```

## Group display

```csharp
[UINavBar(GroupDisplayMember = "GroupDisplay")]
public object NavBars { get; set; }
```

## Active item

```csharp
[UINavBar(ActiveItemProperty = nameof(ActiveItem))]
public object NavBars { get; set; }
public object ActiveItem { get; set; }
```

## Is find field shown

```csharp
[UINavBar(ShowFind = false)]
public object NavBars { get; set; }
```

**Note:** The default is `true`.

## Enter command

```csharp
[UINavBar(EnterCommand = nameof(Enter))]
public object Field { get; set; }

[UICommand]
public void Enter() => { /*action*/ }
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) ||
| iOS (Xamarin.Forms) ||
| Windows (WinForms) | &check; |