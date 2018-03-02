---
layout: post
title: Validation | SfDataForm | Xamarin.Forms | Syncfusion
description: How to validate the data in SfDataForm
platform: Xamarin.Forms
control: SfDataForm
documentation: UG
---

# Validation 

The data form validates the data and displays hints in the case of validation is not passed. In case of invalid data, the error message is shown at the bottom of the editor.

## Built in validations

The supported built in validations are as follows:

* INotifyDataErrorInfo
* Data annotation

### Using INotifyDataErrorInfo

You can validate the data by implementing the [INotifyDataErrorInfo](https://msdn.microsoft.com/en-us/library/system.componentmodel.inotifydataerrorinfo.aspx) interface in the data object class.

{% tabs %}
{% highlight c# %}
public class EmployeeInfo : INotifyDataErrorInfo, INotifyPropertyChanged
{
    private int _EmployeeID;
    private string _Name;
    private string _Title;

    public event PropertyChangedEventHandler PropertyChanged;
    public event EventHandler<DataErrorsChangedEventArgs> ErrorsChanged;

    public EmployeeInfo()
    {

    }

    public int EmployeeID
    {
        get { return this._EmployeeID; }
        set
        {
            this._EmployeeID = value;
            this.RaisePropertyChanged("EmployeeID");
        }
    }

    public string Name
    {
        get { return this._Name; }
        set
        {
            this._Name = value;
            this.RaisePropertyChanged("Name");
        }
    }


    public string Title
    {
        get { return this._Title; }
        set
        {
            this._Title = value;
            this.RaisePropertyChanged("Title");
        }
    }


    [Display(AutoGenerateField = false)]
    public bool HasErrors
    {
        get
        {
            return false;
        }
    }


    private void RaisePropertyChanged(string propertyName)
    {
        if (PropertyChanged != null)
            PropertyChanged(this, new PropertyChangedEventArgs(propertyName));
    }

    public IEnumerable GetErrors(string propertyName)
    {
        var list = new List<string>();
        if (!propertyName.Equals("Title"))
            return list;

        if (this.Title.Contains("Marketing"))
            list.Add("Marketing is not allowed");
        return list;
    }
}

{% endhighlight %}
{% endtabs %}

### Data annotations

You can validate the data using data annotation attributes.

The numeric type like Int, Double, Decimal properties can be validated using the [Range](https://msdn.microsoft.com/en-us/library/system.componentmodel.dataannotations.rangeattribute.aspx) attribute.

{% tabs %}
{% highlight c# %}
private int _EmployeeID;
[Range(1000, 1500, ErrorMessage = "EmployeeID should be between 1000 and 1500")]
public int EmployeeID
{
    get { return this._EmployeeID; }
    set
    {
        this._EmployeeID = value;
        this.RaisePropertyChanged("EmployeeID");
    }
}
{% endhighlight %}
{% endtabs %}

The String type property can be validated using [Required](https://msdn.microsoft.com/en-us/library/system.componentmodel.dataannotations.requiredattribute.aspx) and [StringLength](https://msdn.microsoft.com/en-us/library/system.componentmodel.dataannotations.stringlengthattribute.aspx) attributes.

{% tabs %}
{% highlight c# %}
private string _Name;

[Required(AllowEmptyStrings = false, ErrorMessage = "Name should not be empty")]
[StringLength(10, ErrorMessage = "Name should not exceed 10 characters")]
public string Name
{
    get { return this._Name; }
    set
    {
        this._Name = value;
        this.RaisePropertyChanged("Name");
    }
}

{% endhighlight %}
{% endtabs %}

#### Date range attribute

You can validate the date time value using date range attribute.

{% tabs %}
{% highlight c# %}
private DateTime joinDate;
[DateRange(MinYear = 2010, MaxYear = 2017, ErrorMessage = "Join date is invalid")]
public DateTime JoinDate
{
    get
    {
        return joinDate;
    }
    set
    {
        joinDate = value;
    }
}
{% endhighlight %}
{% endtabs %}

![](SfDataForm_images/Validation3.png)

## Validation mode

The [ValidationMode](https://help.syncfusion.com/cr/cref_files/xamarin/sfdataform/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ValidationMode.html) determines when the value should be validated.

The supported validation modes are as follows:

* LostFocus
* PropertyChanged
* Explicit

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             xmlns:dataForm ="clr-namespace:Syncfusion.XForms.DataForm;assembly=Syncfusion.SfDataForm.XForms"
             x:Class="GettingStarted.MainPage">
    <ContentPage.Content>     
            <dataForm:SfDataForm x:Name="dataForm" ValidationMode="LostFocus"/>            
        </Grid>
    </ContentPage.Content>
</ContentPage>
{% endhighlight %}
{% highlight c# %}
dataForm.ValidationMode = ValidationMode.LostFocus;
{% endhighlight %}
{% endtabs %}

### LostFocus

If the commit mode is LostFocus, the value will be validated when the editor lost its focus.

### PropertyChanged

The value will be validated immediately when it is changed.

### Explicit

The value should be validated manually by calling the [SfDataForm.Validate](https://help.syncfusion.com/cr/cref_files/xamarin/sfdataform/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~Validate().html) or [SfDataForm.Validate (propertyName)](https://help.syncfusion.com/cr/cref_files/xamarin/sfdataform/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~Validate(String).html) method.

The following code validates the value of all the properties in the data object:

{% tabs %}
{% highlight c# %}
dataForm.Validate();
{% endhighlight %}
{% endtabs %}

To validate the specific property value, pass the property name as argument.

{% tabs %}
{% highlight c# %}
dataForm.Validate("Name");
{% endhighlight %}
{% endtabs %}

You can determine whether the data form or property is valid or not by using the `Validate` method.

{% tabs %}
{% highlight c# %}
bool isValid = dataForm.Validate();
bool isPropertyValid = dataForm.Validate("Property");
{% endhighlight %}
{% endtabs %}

If the data form or property is valid, `true` will be returned. Or else `false` will be returned.

N> For validating value, the new value should be committed in data object. So, `ValidationMode` takes higher priority than `CommitMode`.

#### Custom validation through events

You can validate the data using the [Validating](https://help.syncfusion.com/cr/cref_files/xamarin/sfdataform/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~Validating_EV.html) event of the data form.

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             xmlns:dataForm ="clr-namespace:Syncfusion.XForms.DataForm;assembly=Syncfusion.SfDataForm.XForms"
             x:Class="GettingStarted.MainPage">
    <ContentPage.Content>     
            <dataForm:SfDataForm x:Name="dataForm" Validating="DataForm_Validating" />            
        </Grid>
    </ContentPage.Content>
</ContentPage>
{% endhighlight %}
{% highlight c# %}
dataForm.Validating += DataForm_Validating;
private void DataForm_Validating(object sender, ValidatingEventArgs e)
{
    if (e.PropertyName == "Name")
    {
        if (e.Value != null && e.Value.ToString().Length > 8)
        {
            e.IsValid = false;
            e.ErrorMessage = "Name should not exceed 8 characters";
        }
    }            
}
{% endhighlight %}
{% endtabs %}

You can get the notification after completing validation using the [Validated](https://help.syncfusion.com/cr/cref_files/xamarin-android/sfdataform/Syncfusion.SfDataForm.Android~Syncfusion.Android.DataForm.SfDataForm~Validated_EV.html) event of the data form.

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             xmlns:dataForm ="clr-namespace:Syncfusion.XForms.DataForm;assembly=Syncfusion.SfDataForm.XForms"
             x:Class="GettingStarted.MainPage">
    <ContentPage.Content>     
            <dataForm:SfDataForm x:Name="dataForm" Validated="DataForm_Validated" />            
        </Grid>
    </ContentPage.Content>
</ContentPage>
{% endhighlight %}
{% highlight c# %}
dataForm.Validated += DataForm_Validated;
private void DataForm_Validated(object sender, ValidatedEventArgs e)
{
    var isValid = e.IsValid;
    var propertyName = e.PropertyName;
}
{% endhighlight %}
{% endtabs %}

## Valid or positive message

If the value meets the desired criteria, you can show the [valid or positive message](https://help.syncfusion.com/cr/cref_files/xamarin/sfdataform/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute~ValidMessage.html). As error message, the valid message will also be displayed at the bottom of the editor.

{% tabs %}
{% highlight c# %}
private string _Name;
[DisplayOptions(ValidMessage = "Name length is enough")]
[StringLength(10, ErrorMessage = "Name should not exceed 10 characters")]
public string Name
{
    get { return this._Name; }
    set
    {
        this._Name = value;
        this.RaisePropertyChanged("Name");
    }
}
{% endhighlight %}
{% endtabs %}

![](SfDataForm_images/ValidMessage.png)

## How to validate the property value based on another value

To validate one property value based on another property value, use the [property changed event](https://msdn.microsoft.com/en-us/library/system.componentmodel.inotifypropertychanged.propertychanged.aspx) and [Validate](https://help.syncfusion.com/cr/cref_files/xamarin/sfdataform/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~Validate(String).html) methods.

Here, AccountNumber and AccountNumber1 fields are validated.

{% tabs %}
{% highlight c# %}
dataForm.DataObject = new RecipientInfo();
(dataForm.DataObject as INotifyPropertyChanged).PropertyChanged += DataFormGettingStarted_PropertyChanged;

private void DataFormGettingStarted_PropertyChanged(object sender, PropertyChangedEventArgs e)
{
    if (e.PropertyName.Equals("AccountNumber"))
    {
        var value = (string)sender.GetType().GetProperty("AccountNumber1").GetValue(sender);
        if (!string.IsNullOrEmpty(value))
            dataForm.Validate("AccountNumber1");
    }
    else if (e.PropertyName.Equals("AccountNumber1"))
    {
        var value = (string)sender.GetType().GetProperty("AccountNumber").GetValue(sender);
        if (!string.IsNullOrEmpty(value))
            dataForm.Validate("AccountNumber");
    }
}
{% endhighlight %}
{% endtabs %}
