# Events

**Behavior control attribute:**  `UIViewEventsAttribute`

**Usage**: class

### Example

```csharp
[UIViewEvents]
public class Example
{ }
```

## Parameters setting

| Parameter | `UIViewEventsAttribute` property | 
| -----------|:------------- 
| View creating | `OnViewCreating` |
| View created | `OnViewCreated` |
| View attached | `OnViewAttached` |
| View detached | `OnViewDetached` |
| View destroyed | `OnViewDestroyed` |

## View creating

```csharp
[UIViewEvents(OnViewCreating = nameof(OnViewCreating))]
public class Example
{ 
    public void OnViewCreating() { }
}
```

## View created

```csharp
[UIViewEvents(OnViewCreated = nameof(OnViewCreated))]
public class Example
{ 
    public void OnViewCreated() { }
}
```

## View attached

```csharp
[UIViewEvents(OnViewAttached = nameof(OnViewAttached))]
public class Example
{ 
    public void OnViewAttached() { }
}
```

## View detached

```csharp
[UIViewEvents(OnViewDetached = nameof(OnViewDetached))]
public class Example
{ 
    public void OnViewDetached() { }
}
```

## View destroyed

```csharp
[UIViewEvents(OnViewDestroyed = nameof(OnViewDestroyed))]
public class Example
{ 
    public void OnViewDestroyed() { }
}
```

| Platform | Support | 
| -----------|:-------------:| 
| Web (Blazor) | &check; |
| Android (Xamarin.Forms) | &check; |
| iOS(Xamarin.Forms), Windows (WinForms) | &check; |
| Windows (WinForms) | &check; |


# Window

**Behavior control attribute:**  `UIWindowEventsAttribute`

**Usage**: class

### Example

```csharp
[UIWindowEvents(OnShowing = nameof(OnShowing))]
public class EventsExample
{ 
    public void OnShowing() { }
}
```

## Parameters setting

| Parameter | `UIWindowEventsAttribute` property | 
| -----------|:------------- 
| On showing | `OnShowing` |
| On shown | `OnShown` |
| On apply | `OnApply` |
| On closing | `OnClosing` |
| On closed | `OnClosed` |

## On showing

```csharp
[UIWindowEvents(OnShowing = nameof(OnShowing))]
public class EventsExample
{ 
    public void OnShowing() { }
}
```

## On shown

```csharp
[UIWindowEvents(OnShown = nameof(OnShown))]
public class EventsExample
{ 
    public void OnShown() { }
}
```

## On apply

```csharp
[UIWindowEvents(OnApply = nameof(OnApply))]
public class EventsExample
{ 
    public void OnApply() { }
}
```

## On closing

```csharp
[UIWindowEvents(OnClosing = nameof(OnClosing))]
public class EventsExample
{ 
    public void OnClosing() { }
}
```

## On closed

```csharp
[UIWindowEvents(OnClosed = nameof(OnClosed))]
public class EventsExample
{ 
    public void OnClosed() { }
}
```