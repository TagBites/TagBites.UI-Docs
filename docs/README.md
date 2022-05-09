# TagBites.UI

Lightweight and efficient UI generation .NET library, which allows once prepared code to run on multiple platforms:
* `Web (Blazor - WebAssembly, Server Side)`
* `Android (Xamarin.Forms)`
* `iOS (Xamarin.Forms)`
* `Windows (WinForms)`.

NuGet Package: https://www.nuget.org/packages/TagBites.UI/

## The most important advantages of using the library:

* Independence from a specific UI framework.
* Knowledge of UI frameworks and front-end controls is unnecessary 
* Reduction application development time.  
* The developer receives a fully ready tool, he can focus only on the business logic of his application.
* No problems with data binding.
* Consistent appearance of the entire application.

### Example

Simple form with two text fields and list.

```csharp
[UILayout(0, 0)]
public string ClientName { get; set; }

[UILayout(0, 1)]
public string ClientAddress { get; set; }

[UILayout(1, 0, ColumnSpan = 2)]
public IList<Contact> PhoneContacts { get; set; }

public class Contact
{
    [UIListColumn(0, SizeMode = UIListColumnSizeMode.Absolute, Size = 30)]
    public bool ClientAnswer { get; set; }

    [UIListColumn(1)]
    public DateTime Date { get; set; }

    [UIListColumn(2, HorizontalAlignment = TextAlignment.End)]
    [UIString(UIStringType.Telephone)]
    public string PhoneNumber { get; set; }
}
```

### Example



```csharp
private object _identity;

[UILayout(0, 0, ColumnSize = 2)]
public bool IsCompany { get; set; }

[UILabel(false)]
[UILayout(0, 1, RowSpan = 2, ColumnSpan = 3)]
public object Identity
{
    get
    {
        if (_identity == null || IsCompany != (_identity is CompanyIdentityViewModel))
        {
            _identity = IsCompany
                ? new IdentityViewModel()
                : new CompanyIdentityViewModel()
        }

        return _identity;
    }
}

public class IdentityViewModel 
{
    [UILayout(Row = 1)]
    public string FirstName { get; set; }

    [UILayout(Row = 0)]
    public string Surname { get; set; }
}
public class CompanyIdentityViewModel 
{
    [UIString]
    public string Name { get; set; }
}
```