---
layout: post
title: Layout | SfDataForm | Xamarin.Forms | Syncfusion
description: Different layouts and its customization in Xamarin.Forms SfDataForm.
platform: xamarin
control: SfDataForm
documentation: UG
---

# Layout in Xamarin.Forms SfDataForm

## Overview

The data form supports linear and grid layouts. The DataFormLayoutManager creates the [DataFormItemView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItemView.html), [DataFormGroupItemView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItemView.html), and manages layout of label, editor, and validation label.

## Linear layout support

By default, the data form arranges the fields one-by-one. It is applicable for both label positions: left and top.

When the label position is Left, the linear layout is shown as follows:

![Arranging data form field in linear layout when label position as left in Xamarin.Forms DataForm](SfDataForm_images/Linear_LabelLeft.jpg)

When the label position is Top, the linear layout is shown as follows:

![Arranging data form field in linear layout when label position as top in Xamarin.Forms DataForm](SfDataForm_images/Linear_LabelTop.jpg)

## Grid layout support

By default, the data form arranges one data field per row. It is possible to have more than one date fields per row by setting the [ColumnCount](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ColumnCount.html) property which provides grid like layout for the data form.

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             xmlns:dataForm ="clr-namespace:Syncfusion.XForms.DataForm;assembly=Syncfusion.SfDataForm.XForms"
             x:Class="GettingStarted.MainPage">
    <ContentPage.Content>        
            <dataForm:SfDataForm x:Name="dataForm" ColumnCount="2"/>                    
    </ContentPage.Content>    
</ContentPage>
{% endhighlight %}
{% highlight c# %}
dataForm.ColumnCount = 2;
{% endhighlight %}
{% endtabs %}

N> Setting the `ColumnCount` property to SfDataForm does not arrange the data field in a group according to the column count. To set the column count for data fields in the data form group, refer to [loading different layout for data form group](https://help.syncfusion.com/xamarin/sfdataform/layout?cs-save-lang=1&cs-lang=csharp#loading-different-layout-for-group)

When the label position is Left, the grid layout is shown as follows:

![Arranging data form field in grid layout when label position as left in Xamarin.Forms DataForm](SfDataForm_images/Layout_LabelLeft.png)

When the label position is Top, the grid layout is shown as follows:

![Arranging data form field in grid layout when label position as top in Xamarin.Forms DataForm](SfDataForm_images/Layout_LabelTop.png)

## Label visibility

You can hide the label by defining the [DisplayOptions](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute.html) attribute or by handling `AutoGeneratingDataFormItem` event. In this case, only the editor will be loaded.

### Using attributes

{% tabs %}
{% highlight c# %}
private double? percentage;

[DisplayOptions(ShowLabel = false)]
[Display(Prompt = "Enter percentage")]
public double? Percentage
{
    get
    {
        return percentage;
    }
    set
    {
        percentage = value;
        RaisePropertyChanged("Percentage");
    }
}
{% endhighlight %}
{% endtabs %}

### Using event

{% tabs %}
{% highlight c# %}
private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null && e.DataFormItem.Name == "Percentage")
    {
        e.DataFormItem.PlaceHolderText = "Enter percentage";
        e.DataFormItem.ShowLabel = false;
    }
}
{% endhighlight %}
{% endtabs %}

![Hiding label of data form field in Xamarin.Forms DataForm](SfDataForm_images/Layout_HideLabel.png)

## Label position

Labels can be positioned either top or left side of the editor. By using the [LabelPosition](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~LabelPosition.html) property, you can layout the label associated with editor.

By default, the label will be positioned at left side of the editor.

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             xmlns:dataForm ="clr-namespace:Syncfusion.XForms.DataForm;assembly=Syncfusion.SfDataForm.XForms"
             x:Class="GettingStarted.MainPage">
    <ContentPage.Content>        
            <dataForm:SfDataForm x:Name="dataForm" LabelPosition="Top"/>                    
    </ContentPage.Content>    
</ContentPage>
{% endhighlight %}
{% highlight c# %}
dataForm.LabelPosition = LabelPosition.Top;
{% endhighlight %}
{% endtabs %}

![Arranging data form field when label position as top in Xamarin.Forms DataForm](SfDataForm_images/Layout_LabelPosition.png)

## Loading images for label

You can load image instead of label by defining attribute or by handling the `AutoGeneratingDataFormItem` event.

### Using attributes

To show the image as label, use the [ImageName](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute~ImageName.html) property in [DisplayOptions](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute.html) attribute. Images will be taken from …\Resources\drawable folder in Xamarin.Forms.Android, …\Resources folder in Xamarin.Forms.iOS.

{% tabs %}
{% highlight c# %}
private string firstName;
[DisplayOptions(ImageName = "ContactInfo.png")]
public string FirstName
{
    get { return this.firstName; }
    set
    {
        this.firstName = value;
    }
}
{% endhighlight %}
{% endtabs %}

### Using event

By using the [ImageSource](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~ImageSource.html) property in the `DataFormItem`, you can load the image as label.

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;
private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {        
        if (e.DataFormItem.Name == "FirstName")
            e.DataFormItem.ImageSource = ImageSource.FromFile("ContactInfo.png");
    }
}
{% endhighlight %}
{% endtabs %}

![Setting image to data form field in Xamarin.Forms DataForm](SfDataForm_images/LabelCustomized.png)

## Changing order of the DataFormItem

You can change the order of the `DataFormItem` by using attributes or by handling `AutoGeneratingDataFormItem` event.

### Using attributes

You can set the order by using the `Order` property in display attribute.

{% tabs %}
{% highlight c# %}
public class ContactsInfo
{
    private string lastName;
    private string contactNo;       
    public ContactsInfo()
    {

    }

    [Display(Order = 2)]
    public string ContactNumber
    {
        get { return contactNo; }
        set
        {
            this.contactNo = value;
        }
    }

    private string firstName;
    [Display(Order = 0)]
    public string FirstName
    {
        get { return this.firstName; }
        set
        {
            this.firstName = value;
        }
    }

    [Display(Order = 1)]
    public string LastName
    {
        get { return this.lastName; }
        set
        {
            this.lastName = value;
        }
    }
}
{% endhighlight %}
{% endtabs %}

![Ordering label of data form fields in Xamarin.Forms DataForm](SfDataForm_images/LabelOrder.png)

### Using event

You can change the fields order by using the [Order](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~Order.html) property in the `DataFormItem`.

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "FirstName")
            e.DataFormItem.Order = 0;
    }
}
{% endhighlight %}
{% endtabs %}

## Grouping data fields

It is possible to group some fields and set group name in the data form. You can expand or collapse the group by tapping the group item.

Grouping can be achieved by defining attributes or by handling the `AutoGeneratingDataFormItem` event.

### Using attributes

{% tabs %}
{% highlight c# %}
public class ContactsInfo
{
    private string lastName;
    private string contactNo;
    private string email;   
    private DateTime? birthDate;

    public ContactsInfo()
    {

    }

    private string firstName;
    [Display(GroupName = "Name")]
    public string FirstName
    {
        get { return this.firstName; }
        set
        {
            this.firstName = value;
        }
    }
        
    private string middleName;
    [Display(GroupName = "Name")]
    public string MiddleName
    {
        get { return this.middleName; }
        set
        {
            this.middleName = value;
        }
    }
    [Display(GroupName = "Name")]
    public string LastName
    {
        get { return this.lastName; }
        set
        {
            this.lastName = value;
        }
    }
    [Display(GroupName ="Details", ShortName = "ContactNo.")]
    public string ContactNumber
    {
        get { return contactNo; }
        set
        {
            this.contactNo = value;
        }
    }

    [Display(GroupName = "Details")]
    public string Email
    {
        get { return email; }
        set
        {
            email = value;
        }
    }

    [Display(GroupName = "Details")]
    public DateTime? BirthDate
    {
        get { return birthDate; }
        set
        {
            birthDate = value;
        }
    }
}
{% endhighlight %}
{% endtabs %}

### Using event

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;
private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "FirstName" || e.DataFormItem.Name == "MiddleName" || e.DataFormItem.Name == "LastName")
            e.DataFormItem.GroupName = "Name";
        else
            e.DataFormItem.GroupName = "Details";
    }
}
{% endhighlight %}
{% endtabs %}

![Assigning group to the data form fields through attribute in Xamarin.Forms DataForm](SfDataForm_images/DataFormGroup_Attributes.png)

![Assigning group to the data form fields through event in Xamarin.Forms DataForm](SfDataForm_images/DataFormGroup_Events.png)

### Changing order of the DataFormGroupItem

You can change the order of the `DataFormGroupItem` by using attributes. You can set the order of data form items in group by using the `Order` property along with `GroupName` property in display attribute.

{% tabs %}
{% highlight c# %}
public class ContactInfo
{
    private string lastName;
    private string contactNo;
    public ContactInfo()
    {

    }

    private string firstName;
    [Display(Order = 0, GroupName = "Name")]
    public string FirstName
    {
        get { return this.firstName; }
        set
        {
            this.firstName = value;
        }
    }

    [Display(Order = 2, GroupName = "Name")]
    public string LastName
    {
        get { return this.lastName; }
        set
        {
            this.lastName = value;
        }
    }

    private string middleName;
    [Display(Order =1, GroupName = "Name")]
    public string MiddleName
    {
        get { return this.middleName; }
        set
        {
            this.middleName = value;
        }
    }

    private string email;
    [Display(Order = 1, GroupName = "Details")]
    public string Email
    {
        get { return email; }
        set
        {
            this.email = value;
        }
    }

    [Display(Order = 0, GroupName = "Details")]
    public string ContactNumber
    {
        get { return contactNo; }
        set
        {
            this.contactNo = value;
        }
    }
}
{% endhighlight %}
{% endtabs %}

![Setting order to the grouped data form fields in Xamarin.Forms DataForm](SfDataForm_images/GroupItemOrder.png)

### Changing group name for group

You can change the `GroupName` for the group in the `AutoGeneratingDataFormItem` event.

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;
private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormGroupItem != null && e.DataFormGroupItem.GroupName == "Name")
        e.DataFormGroupItem.GroupName = "Name Group";
}
{% endhighlight %}
{% endtabs %}

### Loading different layout for group

You can load linear or grid layout for the particular group by handling the `AutoGeneratingDataFormItem` event.
By setting the `ColumnCount` property in the data form, non-grouped items only will be arranged in the grid layout. To load the grid layout, set the [ColumnCount](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ColumnCount.html) for the [DataFormGroupItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem.html).

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormGroupItem != null && e.DataFormGroupItem.GroupName == "Name")
        e.DataFormGroupItem.ColumnCount = 2;
}
{% endhighlight %}
{% endtabs %}

![Setting ColumnCount to the data form group fields in Xamarin.Forms DataForm](SfDataForm_images/DataFormGroupwithLayout.png)

#### Loading linear and grid layout for the group

{% tabs %}
{% highlight c# %}
public class ContactsInfo
{
    private string lastName;
    private string contactNo;
    private string email;   
    private DateTime? birthDate;

    public ContactsInfo()
    {

    }

    private string firstName;
    [Display(GroupName = "Name")]
    public string FirstName
    {
        get { return this.firstName; }
        set
        {
            this.firstName = value;
        }
    }
        
    [Display(GroupName = "Name")]
    public string LastName
    {
        get { return this.lastName; }
        set
        {
            this.lastName = value;
        }
    }
    [Display(GroupName ="Details", ShortName = "ContactNo.")]
    public string ContactNumber
    {
        get { return contactNo; }
        set
        {
            this.contactNo = value;
        }
    }

    [Display(GroupName = "Details")]
    public string Email
    {
        get { return email; }
        set
        {
            email = value;
        }
    }

    [Display(GroupName = "Details")]
    public DateTime? BirthDate
    {
        get { return birthDate; }
        set
        {
            birthDate = value;
        }
    }
}
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormGroupItem != null && e.DataFormGroupItem.GroupName == "Name")
        e.DataFormGroupItem.ColumnCount = 2;
}
{% endhighlight %}
{% endtabs %}

In the following image, for the `Name` group, the grid layout is loaded and for the `Details` group, linear layout is loaded:

![etting ColumnCount to the data form fields in Xamarin.Forms DataForm](SfDataForm_images/DataFormGroupwithLayout.png)

#### Setting different column count

You can also set different `ColumnCount` for each group.

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormGroupItem != null)
    {
        if (e.DataFormGroupItem.GroupName == "Name")
            e.DataFormGroupItem.ColumnCount = 2;
        else if (e.DataFormGroupItem.GroupName == "Details")
            e.DataFormGroupItem.ColumnCount = 3;
    }
}

{% endhighlight %}
{% endtabs %}

![Setting ColumnCount to different data form fields in Xamarin.Forms DataForm](SfDataForm_images/DataFormGroup_Layout.png)

### Loading group in collapsed state

By default, the group will be loaded in expanded state. You can collapse the group by setting the [IsExpanded](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem~IsExpanded.html) property to false in the [DataFormGroupItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem.html).

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormGroupItem != null && e.DataFormGroupItem.GroupName == "Name")
        e.DataFormGroupItem.IsExpanded = false;
}
{% endhighlight %}
{% endtabs %}

### Restricting the group expanding and collapsing

You can set restrict the group being expanded or collapsed by setting the [AllowExpandCollapse](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem~AllowExpandCollapse.html) to `false` in the [DataFormGroupItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem.html).

In this case, the group will be shown without expander.

![Expand and collapse the data form fields in Xamarin.Forms DataForm](SfDataForm_images/AllowExpandCollapse.png)

### Programmatically expand or collapse group

You can expand or collapse the group programmatically by using [ExpandGroup](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ExpandGroup.html) and [CollapseGroup](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~CollapseGroup.html) methods respectively.

{% tabs %}
{% highlight c# %}
dataForm.ExpandGroup("Group1");

dataForm.CollapseGroup("Group1");
{% endhighlight %}
{% endtabs %}

### Changing DataFormGroupItem visibility
You can change the [DataFormGroupItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem.html) visibility by using the [IsVisible](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItemBase~IsVisible.html) property in the `DataFormGroupItem`.

{% tabs %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;
private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
	if(e.DataFormGroupItem != null )
	{
        if (e.DataFormGroupItem.GroupName == "Details")
            e.DataFormGroupItem.IsVisible = false;
	}
}
{% endhighlight %}
{% endtabs %}

Here, the `Details` group will be hidden.

## Customizing DataFormLayoutManager

To customize the layout, override the [DataFormLayoutManager](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormLayoutManager.html) and assign to the [SfDataForm.LayoutManager](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~LayoutManager.html) property.

{% tabs %}
{% highlight c# %}
public class DataFormLayoutManagerExt : DataFormLayoutManager
{
    public DataFormLayoutManagerExt(SfDataForm dataForm) : base(dataForm)
    {

    }
}
dataForm.LayoutManager = new DataFormLayoutManagerExt(dataForm);
{% endhighlight %}
{% endtabs %}

### Changing editor padding

You can change the editor padding by overriding the `GetLeftPaddingForEditor` method.

{% tabs %}
{% highlight c# %}
public class ContactsInfo
{
    private string lastName;
    public ContactsInfo()
    {

    }

    private string firstName;
    [DisplayOptions(ImageSource = Resource.Drawable.Name)]
    public string FirstName
    {
        get { return this.firstName; }
        set
        {
            this.firstName = value;
        }
    }


    [Display(Prompt = "Enter last name")]
    [DisplayOptions(ShowLabel = false)]
    public string LastName
    {
        get { return this.lastName; }
        set
        {
            this.lastName = value;
        }
    }


}
{% endhighlight %}
{% highlight c# %}
dataForm.LayoutManager = new DataFormLayoutManagerExt(dataForm);

public class DataFormLayoutManagerExt : DataFormLayoutManager
{
    public DataFormLayoutManagerExt(SfDataForm dataForm) : base(dataForm)
    {

    }

    protected override int GetLeftPaddingForEditor(DataFormItem dataFormItem)
    {
        if (dataFormItem.Name == "LastName")
            return 35;
        return base.GetLeftPaddingForEditor(dataFormItem);
    }
}
{% endhighlight %}
{% endtabs %}

Here, the LastName padding is customized.

![Editor with left padding in Xamarin.Forms DataForm](SfDataForm_images/Layout_LeftPadding.png)

### Customizing label and editor

By using DataFormLayoutManager class , you can customize the generated label by overriding the `GenerateViewForLabel` method and also you can customize the editor by overriding the `OnEditorCreated` method.Here, BackgroundColor and TextColor of label and editor is customized.

{% tabs %}
{% highlight c# %}

public class ContactsInfo
{
    public ContactsInfo()
    {

    }

    private string firstName = "Iris";
    public string FirstName
    {
        get { return this.firstName; }
        set
        {
            this.firstName = value;
        }
    }

    private string lastName;
    public string LastName
    {
        get { return this.lastName; }
        set
        {
            this.lastName = value;
        }
    }
}
{% endhighlight %}
{% highlight c# %}

dataForm.LayoutManager = new DataFormLayoutManagerExt(dataForm);

public class DataFormLayoutManagerExt : DataFormLayoutManager
{
    public DataFormLayoutManagerExt(SfDataForm dataForm) : base(dataForm)
    {

    }

    protected override View GenerateViewForLabel(DataFormItem dataFormItem)
    {
        var label = base.GenerateViewForLabel(dataFormItem);
        if (label is Label)
        { 
            (label as Label).BackgroundColor = Color.FromHex("#ff9522");
            (label as Label).TextColor = Color.White;
        }
        return label;
    }
    
    protected override void OnEditorCreated(DataFormItem dataFormItem, View editor)
    { 
        if (editor is Entry)
            (editor as Entry).TextColor = Color.White;
        editor.BackgroundColor = Color.FromHex("#0073dc"); 
    }
}
{% endhighlight %}
{% endtabs %}

![Customization of label through LayoutManager in Xamarin.Forms DataForm](SfDataForm_images/Layout_LabelCustomization.jpg)

## Label width customization

You can set label and editor width proportionally by using [LabelWidth](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~LabelWidth.html) and [EditorWidth](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~EditorWidth.html) properties.

{% tabs %}
{% highlight xaml %}
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:GettingStarted"
             xmlns:dataForm ="clr-namespace:Syncfusion.XForms.DataForm;assembly=Syncfusion.SfDataForm.XForms"
             x:Class="GettingStarted.MainPage">
    <ContentPage.Content>        
            <dataForm:SfDataForm x:Name="dataForm" LabelWidth="1" EditorWidth="2"/>                    
    </ContentPage.Content>    
</ContentPage>
{% endhighlight %}
{% highlight c# %}
dataForm.LabelWidth = 1;
dataForm.EditorWidth = 2;
{% endhighlight %}
{% endtabs %}

Here, the available width is divided into proportionally for editor (2) and label (1).

![Customization of label width in Xamarin.Forms DataForm](SfDataForm_images/Layout_LabelWidth.png)

N> It is applicable only when `LabelPosition` is Left.

By default, the available width is divided equally for editor and label.

## Spanning rows and columns

You can increase row height and column width by defining the `DisplayOptions` attribute.

### Row span

You can increase the row height by using the [RowSpan](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute~RowSpan.html) property in the`DisplayOptions` attribute.

{% tabs %}
{% highlight c# %}
private string firstName;
[DisplayOptions(RowSpan = 2)]
public string FirstName
{
    get { return this.firstName; }
    set
    {
        this.firstName = value;
    }
}
{% endhighlight %}
{% endtabs %}

Here, `FirstName` field’s row height is increased.

![Setting row span to data form item in Xamarin.Forms DataForm](SfDataForm_images/Layout_RowSpan.png)

### Column span

When the grid layout is used, you can increase the column width by using the [ColumnSpan](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute~ColumnSpan.html) property in the `DisplayOptions `attribute.

{% tabs %}
{% highlight c# %}
dataForm.ColumnCount = 2;
{% endhighlight %}
{% highlight c# %}
private string firstName;
[DisplayOptions(ColumnSpan = 2)]
public string FirstName
{
    get { return this.firstName; }
    set
    {
        this.firstName = value;
    }
}
{% endhighlight %}
{% endtabs %}

![Setting column span to data form item in Xamarin.Forms DataForm](SfDataForm_images/Layout_ColumnSpan.png)

## Change DataFormItem visibility at runtime

You can change the field visibility by using the [IsVisible](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItemBase~IsVisible.html) property in the `DataFormItem`.

{% tabs %}
{% highlight c# %}
var dataFormItem = dataForm.ItemManager.DataFormItems["Name"];
if (dataFormItem.Name == "Name")
{
    dataFormItem.IsVisible = false;
}
{% endhighlight %}
{% endtabs %}
Here, the `Name` field will be hidden.

## Change DataFormGroupItem visibility at runtime

You can change the [DataFormGroupItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItem.html) visibility by using the [IsVisible](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItemBase~IsVisible.html) property in the `DataFormGroupItem`.

{% tabs %}
{% highlight c# %}
var dataFormGroupItem = dataForm.ItemManager.GetDataFormGroupItem("Name");
if (dataFormGroupItem.GroupName == "Name")
{
	dataFormGroupItem.IsVisible = false;
}
{% endhighlight %}
{% endtabs %}

Here, the `Name` group will be hidden.

![DataFormGroupItem visibility at runtime in Xamarin.Forms DataForm](SfDataForm_images/CollapseGroupItems.gif)

## Right to left(RTL)

SfDataForm supports to change the layout direction of the control in the right-to-left direction by setting the [FlowDirection](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.visualelement.flowdirection?view=xamarin-forms#Xamarin_Forms_VisualElement_FlowDirection) to `RightToLeft` or by changing the device language.

{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm FlowDirection="RightToLeft">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.FlowDirection = FlowDirection.RightToLeft;
{% endhighlight %}
{% endtabs %}

>**Note**
For implementing the `FlowDirection` in the control, Xamarin.Forms package version must be 3.0 and above. Please refer [RightToLeft](https://blog.xamarin.com/right-to-left-localization-xamarin-forms) to get more details about `RightToLeft` flow direction in Xamarin.Forms.

### Android
For Android, add `android:supportsRtl="true"` in your application tag of `AndroidManifest.xml` file, and make sure your `MinSDKVersion` is 17+. By changing the device language / enabling the device's `Force RTL layout` can achieve the `RightToLeft` layout direction in DataForm.

{% tabs %}
{% highlight xml %}
<manifest ... >
<uses-sdk android:minSdkVersion="17" ... />
<application ... android:supportsRtl="true">
</application>
</manifest>
{% endhighlight %}
{% endtabs %}

### iOS
For iOS, add the `RightToLeft` language in the `CFBundleLocalizations` section of your `Info.plist` file, and make sure you’re targeting iOS 9+.

{% tabs %}
{% highlight xml %}
<resources>
<key>CFBundleDevelopmentRegion</key>
<string>en</string>
<key>CFBundleLocalizations</key>
<array>
<string>en</string>
<string>ar</string>
</array>
</resources>
{% endhighlight %}
{% endtabs %}

![info plist](SfDataForm_images/DataForm_iosplist.png)

### UWP
For UWP, you need to set `FlowDirection` to `RightToLeft` in the `MainPage.cs` file of the `UWP` project.

{% tabs %}
{% highlight c# %}
public MainPage()
{
…
this.FlowDirection = FlowDirection.RightToLeft;
LoadApplication (new App ());
…
}
{% endhighlight %}
{% endtabs %}

![RTL in Xamarin.Forms DataForm](SfDataForm_images/DataForm_RTL.png)

## Programmatically scroll to specific editor

You can programmatically scroll to specific editor using the [ScrollTo](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ScrollTo.html) method by passing the `property name`. 

{% tabs %}
{% highlight c# %}
dataForm.ScrollTo("ContactNumber")
{% endhighlight %}
{% endtabs %}

![Scroll to specific editor in Xamarin.Forms DataForm](SfDataForm_images/xamarin-forms-scrolltosupport.gif)
