---
layout: post
title: Multi Selection in Syncfusion SfAutoComplete control for Xamarin.Forms
description: Learn how to restrict maximum suggestion to be displayed in SfAutoComplete
platform: xamarin
control: SfAutoComplete
documentation: ug
---
# Multiple Selection

Select multiple items from a suggestion list. There are two ways to perform multi selection in autocomplete.

* Token Representation

*  Delimiter

## Token Representation

Selected items will be displayed with a customizable token representation and the users can remove each tokenized item with the close button.

{% tabs %}

{% highlight xaml %}

<StackLayout VerticalOptions="Start" HorizontalOptions="Start" Padding="30">
	<autocomplete:SfAutoComplete HeightRequest="40" x:Name="autoComplete" MultiSelectMode="Token" TokensWrapMode="Wrap" IsSelectedItemsVisibleInDropDown="false" />                    
</StackLayout> 

{% endhighlight %}

{% highlight c# %}

List<String> countryNames = new List<String>();
countryNames.Add("Uganda");
countryNames.Add("Ukraine");
countryNames.Add("United Arab Emirates");
countryNames.Add("United Kingdom");
countryNames.Add("United States");
autoComplete.MaximumSuggestion=3;
autoComplete.MultiSelectMode=MultiSelectMode.Token;
autoComplete.TokensWrapMode=TokensWrapMode.Wrap;
autoComplete.IsSelectedItemsVisibleInDropDown=false;
autoComplete.DataSource = countryNames;

{% endhighlight %}

{% endtabs %}

### Wrap Mode of Token

The selected item can be displayed as token inside SfAutoComplete in two ways. They are

* `Wrap` - When `TokensWrapMode` is set to `Wrap` the selected items will be wrap to the next line of the SfAutoComplete.

* `None` - When `TokensWrapMode` is set to `None` the selected item will be wrap in horizontal orientation.

{% tabs %}

{% highlight xaml %}

<StackLayout VerticalOptions="Start" HorizontalOptions="Start" Padding="30">
    <autocomplete:SfAutoComplete HeightRequest="40" x:Name="autoComplete" DropDownItemHeight="50" DisplayMemberPath="Name" ImageMemberPath="Image" MultiSelectMode="Token" TokensWrapMode="Wrap" DataSource="{Binding EmployeeCollection}">
    </autocomplete:SfAutoComplete>
</StackLayout>

{% endhighlight %}

{% highlight c# %}

List<String> countryNames = new List<String>();
countryNames.Add("Uganda");
countryNames.Add("Ukraine");
countryNames.Add("United Arab Emirates");
countryNames.Add("United Kingdom");
countryNames.Add("United States");
autoComplete.TokensWrapMode=TokensWrapMode.Wrap;



        public class Employee
{
    private string image;
    public string Image
    {
        get { return image; }
        set { image = value; }
    }
    private string name;
    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}

public class EmployeeViewModel :INotifyPropertyChanged
{
    private ObservableCollection<Employee> employeeCollection;
    public ObservableCollection<Employee> EmployeeCollection
    {
        get { return employeeCollection; }
        set { employeeCollection = value; }
    }
    public EmployeeViewModel()
    {
        employeeCollection = new ObservableCollection<Employee>();
        employeeCollection.Add(new Employee() { Image = "a0.png", Name = "John" });
        employeeCollection.Add(new Employee() { Image = "a1.png", Name = "James" });
        employeeCollection.Add(new Employee() { Image = "a2.png", Name = "Jacob" });
        employeeCollection.Add(new Employee() { Image = "a3.png", Name = "Joy" });
        employeeCollection.Add(new Employee() { Image = "a4.png", Name = "Justin" });
        employeeCollection.Add(new Employee() { Image = "a5.png", Name = "Jerome" });
        employeeCollection.Add(new Employee() { Image = "b0.png", Name = "Jessica" });
        employeeCollection.Add(new Employee() { Image = "b1.png", Name = "Victoria" });
       
    }

    public int GetHeight(bool value)
        {
            if (value)
                return 80;
            return 80;
        }

        private int toHeight = 40;
        public int ToHeight
        {
            get { return toHeight; }
            set
            {
                toHeight = value;
                RaisePropertyChanged("ToHeight");
            }
        }
        private bool isToFocused = false;
        public bool IsToFocused
        {
            get { return isToFocused; }
            set
            {
                isToFocused = value;
                ToHeight = GetHeight(value);
                RaisePropertyChanged("IsToFocused");
            }
        }
        public event PropertyChangedEventHandler PropertyChanged;
        private void RaisePropertyChanged(String name)
        {
            if (PropertyChanged != null)
                this.PropertyChanged(this, new PropertyChangedEventArgs(name));
        }
    }
}

}
{% endhighlight %}

{% endtabs %}


![](images/MultiSelect/TokenRepresentation_Wrap.png)
 
### Token Customization

Customization can be done for Token. There are various ways to customize the tokens. They are as follows.

* `TextColor` - sets the color of the text inside the token.

* `FontSize` - sets the size of the Font inside the token.

* `FontFamily` - sets the Font family for the text inside the token.

* `BackgroundColor` - sets the background color of the token.

* `SelectedBackgroundColor` - sets the background color of the token when it is selected.

* `IsCloseButtonVisible` - Enables and disables the close button inside SfAutoComplete.

* `DeleteButtonColor` - sets the color of the close button inside SfAutoComplete.

* `CornerRadius` - sets the corner radius for the token.



{% tabs %}

{% highlight xaml %}

<StackLayout VerticalOptions="Start" HorizontalOptions="Start" Padding="30">
    <autocomplete:SfAutoComplete HeightRequest="40" x:Name="autoComplete" DropDownItemHeight="50" DisplayMemberPath="Name" ImageMemberPath="Image" MultiSelectMode="Token" TokensWrapMode="Wrap" DataSource="{Binding EmployeeCollection}">
    </autocomplete:SfAutoComplete>
</StackLayout>

{% endhighlight %}

{% highlight c# %}

namespace autocomplete
{
public partial class autocompletePage : ContentPage
{
    EmployeeViewModel view = new EmployeeViewModel();
    public autocompletePage()
    {
        InitializeComponent();

        TokenSettings token = new TokenSettings();
        token.FontSize = 16;
        token.BackgroundColor = Color.FromHex("#d3d3d3");
        token.TextColor = Color.Red;
        token.SelectedBackgroundColor = Color.FromHex("#ffffe0");
        token.DeleteButtonColor = Color.Brown;
         token.FontFamily= "Times New Roman";
        token.IsCloseButtonVisible = true;
        token.CornerRadius = 3;
        autoComplete.TokenSettings = token;
        this.BindingContext = view;
    }
}

        public class Employee
{
    private string image;
    public string Image
    {
        get { return image; }
        set { image = value; }
    }
    private string name;
    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}

public class EmployeeViewModel :INotifyPropertyChanged
{
    private ObservableCollection<Employee> employeeCollection;
    public ObservableCollection<Employee> EmployeeCollection
    {
        get { return employeeCollection; }
        set { employeeCollection = value; }
    }
    public EmployeeViewModel()
    {
        employeeCollection = new ObservableCollection<Employee>();
        employeeCollection.Add(new Employee() { Image = "a0.png", Name = "John" });
        employeeCollection.Add(new Employee() { Image = "a1.png", Name = "James" });
        employeeCollection.Add(new Employee() { Image = "a2.png", Name = "Jacob" });
        employeeCollection.Add(new Employee() { Image = "a3.png", Name = "Joy" });
        employeeCollection.Add(new Employee() { Image = "a4.png", Name = "Justin" });
        employeeCollection.Add(new Employee() { Image = "a5.png", Name = "Jerome" });
        employeeCollection.Add(new Employee() { Image = "b0.png", Name = "Jessica" });
        employeeCollection.Add(new Employee() { Image = "b1.png", Name = "Victoria" });
       
    }
}

}
{% endhighlight %}

{% endtabs %}


![](images/MultiSelect/TokenRepresentation.png)

## Delimiter

When selecting the multiple items, the selected items can be divided with a desired character given for a delimiter. We can set delimiter character with the `Delimiter` property.

{% tabs %}
{% highlight xaml %}

<StackLayout VerticalOptions="Start" HorizontalOptions="Start" Padding="30">
	<autocomplete:SfAutoComplete HeightRequest="40" x:Name="autoComplete" MultiSelectMode="Delimiter"  Delimiter="*" />                    
</StackLayout> 

{% endhighlight %}

{% highlight c# %}

List<String> countryNames = new List<String>();
countryNames.Add("Algeria");
countryNames.Add("Andorra");
countryNames.Add("Angola");
countryNames.Add("Antarctica");
countryNames.Add("Argentina");
countryNames.Add("Armenia");
countryNames.Add("Aruba");
autoComplete.MaximumSuggestion=3;
autoComplete.MultiSelectMode=MultiSelectMode.Delimiter;
autoComplete.Delimiter="*";
autoComplete.DataSource = countryNames;

{% endhighlight %}

{% endtabs %}

![](images/MultiSelect/Delimiter.png)

