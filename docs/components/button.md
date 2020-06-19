# Button

**Behavior control attribute:**  `UIButtonAttribute`

**Types automatically recognized:** None

**Acceptable types**: `string`, `Action`, `Func<Task>`, `Task`, `Task<IUICommandResult>,` `object`

###  Example
```csharp
[UIButton]
public string ButtonField { get; set; }
```

## `String` type - command button
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

## `Action` type

```csharp
[UILayout]
public Action Action => () { /*action*/ }
```

## `Func<Task>` type

```csharp
[UILayout]
public Func<Task> Task => async () =>
{
    await Task.Delay(500);
}
```

## `Task` type

A method returning `Task` should has the `UICommandAttribute`.

```csharp
[UICommand]
public async Task Delay()
{
    await Task.Delay(100);
}
```
## `Task<IUICommandResult>` type

```csharp
[UICommand]
public async Task<IUICommandResult> Delay()
{
    return UICommandResult.Success("Example message.");
}
```

## `Object` type - link
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

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |
