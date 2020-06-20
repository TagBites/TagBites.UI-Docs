# Access

**Behavior control attribute:**  `UIIconAttribute`

**Usage**: all

### Example

```csharp
[UIIcon(MaterialIcons.Clear)]
public string Field { get; set; }
```

## Parameters setting

| Parameter | `UIAccessAttribute` property | 
| -----------|:------------- 
| Resource type | `ResourceType` |
| Resource name | `ResourceName` |
| Icon | `IconValue` or `IconProperty` |
| Color | `Color` |

## Resource type

```csharp
[UIIcon(typeof(CustomIcons))]
public string Field { get; set; }
```

## Resource name

```csharp
[UIIcon(typeof(CustomIcons), "Icon")]
public string Field { get; set; }
```

## Icon

Icon parameter can be set as:
* constant value using `IconValue` property

```csharp
[UIIcon(MaterialIcons.Clear)]
public string Field { get; set; }
```

* dynamic value using binding with `IconProperty` property

```csharp
[UIIcon(IconProperty = FieldIcon)]
public string Field { get; set; }
public object FieldIcon { get; set; }
```

## Color

```csharp
[UIIcon(MaterialIcons.Clear, UIColorNames.Danger)]
public string Field { get; set; }
```
