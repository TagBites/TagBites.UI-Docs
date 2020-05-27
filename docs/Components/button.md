# Button

**Types automatically recognized:** None

**Behavior control attribute:**  `UIButtonAttribute`

###  Example
```csharp
[UIButton]
public string ButtonField { get; set; }
```

**Note:** A button can be connected with command or link.

## Command button
The value of property with `UIButtonAttribute` attribute is set to a name of method with `UICommandAttribute` attribute.

**Note:** Button can be connected with synchronous and asynchronous action.

### Button with a command example
```csharp
[UIButton]
public string CommandName { get; set; } = nameof(CommandAction);

[UICommand]
public void CommandAction() { /*action*/ }
```

### Button with a asynchronous command example
```csharp
[UIButton]
public string CommandName { get; set; } = nameof(CommandAction);

[UICommand]
public async Task CommandAction() { /*action*/ }
```

### Switching the commands connected with the buttons example
The command connected with the button can be replaced by other.

```csharp
[UIButton]
public string CommandName { get; set; } = nameof(CommandAction1);

[UICommand]
public void CommandAction1() 
{ 
    CommandName = nameof(CommandAction2); 
}

[UICommand]
public void CommandAction2() { /*action*/ }
```

## Link
The value of property with `UIButtonAttribute` attribute is set to a link.

```csharp
[UIButton]
public object Link => "https://tagbites.com";
```

## Button with icon

```csharp
[UIButton]
[UIIcon(MaterialIcons.Call)]
public string CommandName { get; set; }
```
