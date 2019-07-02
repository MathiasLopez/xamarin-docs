---
layout: post
title: Floating label Layout | DataForm | Xamarin.Forms | Syncfusion
description: Xamarin.Forms Dataform supports floating label layout with assistive labels, leading and trailing icons, password toggle icon to display or hide a password.
platform: xamarin
control: SfDataForm
documentation: UG
---

# Floating label layout

The Dataform supports floating label layout with support for assistive labels, leading and trailing icons, and a password toggle icon to show or hide a password. It provides three type of containers such as filled, outlined and none. Floating label layout can be enabled by setting `DataForm.LayoutOptions` to `TextInputLayout`.

![Arranging data form field in floating label layout in Xamarin.Forms DataForm](SfDataForm_images/FloatingLabel_Layout.png)

## Layout options
By default, the dataform arranges the editors and their labels corresponding to the fields in stack layout. However, to enable the floating label layout set [LayoutOptions](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~LayoutOptions.html) property of `DataForm` or [DataFormItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem.html) to `TextInputLayout`.

{% tabs %}
{% highlight xaml %}       
 <dataForm:SfDataForm x:Name="dataForm" LayoutOptions="TextInputLayout">
 <dataForm:SfDataForm/>
{% endhighlight %}
{% highlight c# %}
dataForm.LayoutOptions = LayoutOptions.TextInputLayout;
{% endhighlight %}
{% endtabs %}

### Changing layout options of the DataFormItem
You can change layout option by using the [LayoutOptions](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~LayoutOptions.html) property in the `DataFormItem` and it will be handled in the `AutoGeneratingDataFormItem` event.

{% tabs %}
{% highlight xaml %}      
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Address")
        {
            e.DataFormItem.LayoutOptions = LayoutOptions.TextInputLayout;
        }
        if (e.DataFormItem.Name == "DOB")
        {
            e.DataFormItem.LayoutOptions = LayoutOptions.TextInputLayout;
        }
    }
    if (e.DataFormItem != null && e.DataFormItem.Name == "Password")
    {
       e.DataFormItem.LayoutOptions = LayoutOptions.TextInputLayout;
    }
}

{% endhighlight %}
{% endtabs %}

![Arranging data form field in different layouts in Xamarin.Forms DataForm](SfDataForm_images/DataFormItem_LayoutOptions.png)

## Supported editors
Dataform supports the floating label layout for the following editors.
* Text editor
* Password editor
* MaskedEditText editor
* Numeric editor 
* MultilineText editor
* Date editor
* Time editor
* Picker editor

## Container types
Containers enhance the perspective of dataform editor views and provide some contrast between editor view and assistive labels. Their border and assistive label color will be changed based on the dataform field validation.

By default, the container type is `Outlined`. By using the [ContainerType](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ContainerType.html) property in `DataForm` or in `DataFormItem`, you can modify the container type to `Filled` or `None`.

### Filled
The background color of dataform editor view will be filled with container color and it can be enabled by setting the [ContainerType](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ContainerType.html)  property to `Filled` in `DataForm` or in `DataFormItem`.

![Arranging data form field in floating label layout with filled container type in Xamarin.Forms DataForm](SfDataForm_images/Filled_ContainerType.png)

### Outlined
To enable the outlined container type, you can set [ContainerType](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ContainerType.html) property to `Outlined` in `DataForm` or in `DataFormItem` which covers the editor view with rounded-corner.

![Arranging data form field in floating label layout with outlined container type in Xamarin.Forms DataForm](SfDataForm_images/FloatingLabel_Layout.png)

### None
When setting the [ContainerType](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.SfDataForm~ContainerType.html) property to ` None ` in `DataForm` or in `DataFormItem` container, it will have empty background and enough spacing.

![Arranging data form field in floating label layout with none container type in Xamarin.Forms DataForm](SfDataForm_images/NoneContainerType.png)

{% tabs %}
{% highlight xaml %}      
<dataForm:SfDataForm x:Name="dataForm" ContainerType="Outlined">
</dataForm:SfDataForm>                    
{% endhighlight %}
{% highlight c# %}
dataForm.LayoutOptions = ContainerType.Outlined;
{% endhighlight %}
{% endtabs %}

### Changing container type of the DataFormItem

You can change the container type of the [DataFormItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem.html) by using the [ContainerType](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~ContainerType.html) property in the [TextInputLayoutSettings](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings.html) of `DataFormItem` and it will be handled by the `AutoGeneratingDataFormItem` event.

{% tabs %}
{% highlight xaml %}  
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Name")
        {
            e.DataFormItem.ContainerType = ContainerType.Filled;
        }
        if (e.DataFormItem.Name == "Address")
        {
            e.DataFormItem.ContainerType = ContainerType.None;
        }
    }
    if (e.DataFormItem != null && e.DataFormItem.Name == "Password")
    {
        e.DataFormItem.ContainerType = ContainerType.Outlined;
    }
}

{% endhighlight %}
{% endtabs %}

![Arranging data form field in floating label layout with multiple containers in Xamarin.Forms DataForm](SfDataForm_images/DataFormItem_ContainerTypes.png)

## Leading view
Floating label layout supports leading view, which shows an icon view to the left of editor.

Unicode or font icons for the labels can be displayed as icons. By setting the [LeadingView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~LeadingView.html) property in `TextInputLayoutSettings` of `DataFormItem`, a label can be added as a leading icon for editor view. By setting the [LeadingViewPosition](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~LeadingViewPosition.html) property, it can be placed either inside or outside the container. It is positioned outside by default. 

N> Refer to the following links to learn more about font icons:
* [How to create font icons using our metro studio and export as ttf?](https://help.syncfusion.com/metro-studio/export-icon-font)
* [How to set font family for the custom fonts in labels?](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/fonts#using-a-custom-font)


{% tabs %}
{% highlight xaml %}  
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Name")
        {
            e.DataFormItem.TextInputLayoutSettings = new Syncfusion.SfDataForm.XForms.TextInputLayoutSettings()
            {
                LeadingView = new Label()
                {
                    VerticalTextAlignment = Device.RuntimePlatform == Device.iOS ? TextAlignment.Center : TextAlignment.Start,
                    FontSize = Device.RuntimePlatform == Device.iOS ? 18 : 24,
                    Text = "A",
                    FontFamily = Device.RuntimePlatform == Device.iOS ? "ContactsIcons" : Device.RuntimePlatform == Device.Android ? "ContactsIcons.ttf#ContactsIcons" : "Assets/Fonts/ContactsIcons.ttf#ContactsIcons"
                }
            };
        }
    }
}

{% endhighlight %}
{% endtabs %}

![Arranging data form field in floating label layout with leading view in Xamarin.Forms DataForm](SfDataForm_images/FloatingLabel_LeadingView.png)

## Trailing view
Floating label layout supports trailing view, which shows an icon view to the right of editor.

Unicode or font icons for the labels can be displayed as icons.By setting the [TrailingView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~TrailingView.html) property, a label can be added as a trailing icon for editor view. By setting the [TrailingViewPosition](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~TrailingViewPosition.html) property, it can be placed either inside or outside the container. It is positioned outside by default. 

N> Refer to the following links to learn more about font icons:
* [How to create font icons using our metro studio and export as ttf?](https://help.syncfusion.com/metro-studio/export-icon-font)
* [How to set font family for the custom fonts in labels?](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/fonts#using-a-custom-font)

{% tabs %}
{% highlight xaml %}  
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "PhoneNumber")
        {
            e.DataFormItem.TextInputLayoutSettings = new Syncfusion.SfDataForm.XForms.TextInputLayoutSettings()
            {
                TrailingView = new Label()
                {
                    VerticalTextAlignment = Device.RuntimePlatform == Device.iOS ? TextAlignment.Center : TextAlignment.Start,
                    FontSize = Device.RuntimePlatform == Device.iOS ? 18 : 24,
                    Text = "I",
                    FontFamily = Device.RuntimePlatform == Device.iOS ? "ContactsIcons" : Device.RuntimePlatform == Device.Android ? "ContactsIcons.ttf#ContactsIcons" : "Assets/Fonts/ContactsIcons.ttf#ContactsIcons"
                }
            };
        }
    }
}

![Arranging data form field in floating label layout with trailing view in Xamarin.Forms DataForm](SfDataForm_images/FloatingLabel_TrailingView.png)

## Enable password visibility toggle for password editor

Password toggle visibility in floating label layout is used to show or hide the visibility of characters in the dataform password editor. You can enable this toggle by setting the [EnablePasswordVisibilityToggle](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormTextItem_members.html) property to true in [DataFormTextItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormTextItem.html).

{% tabs %}
{% highlight xaml %}      
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}"/>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null && e.DataFormItem.Name == "Password")
    {
        (e.DataFormItem as DataFormTextItem).EnablePasswordVisibilityToggle = true;
    }
}
{% endhighlight %}
{% endtabs %}

![Arranging data form field in floating label layout with password toggle in Xamarin.Forms DataForm](SfDataForm_images/Password_Toggel.png)

## Assistive label

Assistive labels comprise of floating label or hint label, helper label, counter label and validation label.

### Reserve space for assistive labels

The reserved spaces for assistive labels can be removed by setting the [ReserveSpaceForAssistiveLabels](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~ReserveSpaceForAssistiveLabels.html) property to false or it can be set to false automatically if there is no prompt value or water mark provider for `DataformItem` and/or no counter label added.

{% tabs %}
{% highlight xaml %}  
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        e.DataFormItem.TextInputLayoutSettings = new Syncfusion.SfDataForm.XForms.TextInputLayoutSettings()
        {
            ReserveSpaceForAssistiveLabels= true
        };
    }
}

![Arranging data form field in floating label layout with reserved space between editors for assistive labels in Xamarin.Forms DataForm](SfDataForm_images/ReserveSpaceForAssitiveLabel.png)

### Hint label

The data field caption will be displayed as floating or hint label for the editor, and it will be enabled by using the `Name` or [LabelText](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~LabelText.html)  property.

### Helper label

The helper label is used to display the water mark for the editor to provide hint for users and it can be set using [Prompt ] https://help.syncfusion.com/xamarin/sfdataform/working-with-dataform#setting-watermark.

### Validation label

The validation label used to display the dataform validation messages such as valid or invalid data. Refer [validation](https://help.syncfusion.com/xamarin/sfdataform/validation) to learn more about dataform validation.

### Counter label

The counter label is can be used to notify the character count limitation in given validation. It can be enabled by setting the [ShowCharCount](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~ShowCharCount.html) property to `true`. Character limit can be set using the `StringLength` attribute.


{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null && e.DataFormItem.Name == "Password")
    {
        e.DataFormItem.ShowCharCount = true;
    }
}

private string _Password;

[Required(AllowEmptyStrings = false, ErrorMessage = "Password should not be empty")]
[StringLength(10, ErrorMessage = "Password should not exceed 10 characters")]
public string Password
{
    get { return this._Password; }
    set
    {
        this._Password = value;
        this.RaisePropertyChanged("Password");
    }
}
{% endhighlight %}
{% endtabs %}

![Arranging data form field in floating label layout with counter label in Xamarin.Forms DataForm](SfDataForm_images/CounterLabel.png)

## Appearance customization
The assistive labels and border color can be customized based on the editor view states and data validation.

### Changing outline corner radius
When setting the [OutlineCornerRadius](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.SfDataForm.XForms.TextInputLayoutSettings~OutlineCornerRadius.html) property to double value, the corner radius of the container will be changed.

{% tabs %}
{% highlight xaml %}  
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        e.DataFormItem.TextInputLayoutSettings = new Syncfusion.SfDataForm.XForms.TextInputLayoutSettings()
        {
            OutlineCornerRadius = 30
        };
    }
}

![Arranging data form field in floating label layout with outlined corner radius in Xamarin.Forms DataForm](SfDataForm_images/FloatingLabel_CornerRadius.png)

### Focused color
When the given editor view is focused, the [FocusedColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~FocusedColor.html) property value will be applied to the label text and border.

{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Name")
        {
            e.DataFormItem.FocusedColor = Color.Violet;
        }
    }
}

![Arranging data form field in floating label layout with customized focused color in Xamarin.Forms DataForm](SfDataForm_images/FocusedColor.png)

### Unfocused color
When the given editor view is unfocused, the [UnfocusedColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~UnfocusedColor.html) property value will be applied to the label text and border.

{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Name")
        {
            e.DataFormItem.UnfocusedColor = Color.Silver;
        }
    }
}

![Arranging data form field in floating label layout with customized unfocused color in Xamarin.Forms DataForm](SfDataForm_images/UnfocusedColor.png)

### Error message color
In case of invalid data, the [ErrorMessageColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~ErrorMessageColor.html) will be applied to the error label, hint label and border.

{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Name")
        {
            e.DataFormItem.ErrorMessageColor = Color.DarkRed;
        }
    }
}

![Arranging data form field in floating label layout with customized error message color in Xamarin.Forms DataForm](SfDataForm_images/ErrorMessage_Color.png)

### Valid message color
In case of valid data,the [ValidMessageColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~ValidMessageColor.html)  will be applied to the valid message label , hint label and border.

{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}" AutoGeneratingDataFormItem="DataForm_AutoGeneratingDataFormItem">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem1(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null)
    {
        if (e.DataFormItem.Name == "Name")
        {
            e.DataFormItem.ValidMessageColor = Color.BlueViolet;
        }
    }
}

![Arranging data form field in floating label layout with customized validation message color in Xamarin.Forms DataForm](SfDataForm_images/ValidationMessage_Color.png)

## Font customization
You can customize the font of assistive labels by setting the FontFamily, FontSize, and FontAttributes properties of the LabelStyle  property.


### Hint label style
You can customize the text of hint label by setting the FontFamily, FontSize, and FontAttributes properties of [HintLabelStyle](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~HintLabelStyle.html) in DataFormItem.

![Arranging data form field in floating label layout with customized hint label text in Xamarin.Forms DataForm](SfDataForm_images/HintText_Style.png)

### Helper label style
You can customize the text of helper label by setting the FontFamily, FontSize, and FontAttributes properties of [HelperLabelStyle](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~HelperLabelStyle.html) in DataFormItem.

![Arranging data form field in floating label layout with customized helper label text in Xamarin.Forms DataForm](SfDataForm_images/HelperText_Style.png)

### Validation label style
You can customize the text of validation label by setting the FontFamily, FontSize, and FontAttributes properties of [ValidationLabelStyle](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItem~ValidationLabelStyle.html) in DataFormItem.

{% tabs %}
{% highlight xaml %}      
<dataForm:SfDataForm x:Name="dataForm" DataObject="{Binding ContactsInfo}"/>
{% endhighlight %}
{% highlight c# %}
dataForm.AutoGeneratingDataFormItem += DataForm_AutoGeneratingDataFormItem;

private void DataForm_AutoGeneratingDataFormItem(object sender, AutoGeneratingDataFormItemEventArgs e)
{
    if (e.DataFormItem != null && e.DataFormItem.Name == "Password")
    {
        (e.DataFormItem.HintLabelStyle  = new LabelStyle() { FontFamily = Device.OnPlatform("Lobster-Regular", "Lobster-Regular.ttf#Lobster-Regular", "Assets/Fonts/Lobster-Regular.ttf#Lobster"), FontSize = 16};
    }
}
{% endhighlight %}
{% endtabs %}

![Arranging data form field in floating label layout with customized validation label text in Xamarin.Forms DataForm](SfDataForm_images/ErrorMessage_Style.png)

## Limitations

* It is recommended not to provide background color for editor view while customizing existing editor inside floating label layout.
* It is recommended not to use non-editable custom editor views inside floating label layout such as range slider,etc.
* It is recommended not to use the [LayoutOptions](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DisplayOptionsAttribute~LayoutOptions.html) attribute for setting default layout for data fields.
* It is recommended not to use null values in [Date Editor](https://help.syncfusion.com/xamarin/sfdataform/editors#date-editor) and [Time Editor](https://help.syncfusion.com/xamarin/sfdataform/editors#time-editor)  with text input layout in initial loading time and runtime in iOS platform.

## Unsupported editors
Floating label layout do not support for the following non-editable editors.

* RadioGroup editor
* Segment editor
* CheckBox editor
* Switch editor
* Drop down editor

You can download the sample from [here](https://github.com/SyncfusionExamples/Floating-label-editors-in-xamarin.forms-dataform)