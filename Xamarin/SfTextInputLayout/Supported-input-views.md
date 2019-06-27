---
layout: post
title: Syncfusion supported input views
description: How to add supported input views in text input layout.
platform: xamarin
control: SfTextInputLayout
documentation: ug
---

# Supported input views

Input views can be added to the text input layout control by setting the [InputView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Core.XForms~Syncfusion.XForms.TextInputLayout.SfTextInputLayout~InputView.html) property. To reduce the XAML syntax, [InputView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Core.XForms~Syncfusion.XForms.TextInputLayout.SfTextInputLayout~InputView.html) property is applied with [ContentPropertyAttribute](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.contentpropertyattribute?view=xamarin-forms).

## Entry

To enter a single line text input, add [Entry](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/entry).

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout
   Hint="Name"
   HelperText="Enter your name">
   <Entry />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Name"; 
inputLayout.HelperText = "Enter your name"
inputLayout.InputView = new Entry(); 

{% endhighlight %}

{% endtabs %}

![Entry](Supported-input-views-images/textInput_input_img1.PNG)

## Editor


To enter multi line text input, add [Editor](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/editor).


{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout
   Hint="Notes">
   <Editor />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Notes"; 
inputLayout.InputView = new Editor(); 

{% endhighlight %}

{% endtabs %}

![Editor](Supported-input-views-images/textInput_input_img2.PNG)

## Masked edit

To initialize the masked edit control and launch it in each platform, refer to the [getting started with masked edit](https://help.syncfusion.com/xamarin/sfmaskededit/getting-started) documentation.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout
   Hint="Card number"
   HelperText="Required *">
   <maskededit:SfMaskedEdit
        Keyboard="Numeric"
        Mask="0000 0000 0000 0000" />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Card number"; 
inputLayout.HelperText = "Required *"
inputLayout.InputView = new SfMaskedEdit() { Keyboard = Keyboard.Numeric, Mask = "0000 0000 0000 0000" }; 

{% endhighlight %}

{% endtabs %}

![Masked edit](Supported-input-views-images/textInput_input_img3.PNG)

## Numeric text box

To initialize the numeric text box control and launch it in each platform, refer to the [getting started with numeric text box](https://help.syncfusion.com/xamarin/sfnumerictextbox/getting-started) documentation.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout
   Hint="Amount"
   HelperText="Required *">
   <numericBox:SfNumericTextBox 
      Value="123.45"
      FormatString="c" />
</inputLayout:SfTextInputLayout>  

{% endhighlight %}

{% highlight C# %} 

var inputLayout = new SfTextInputLayout();
inputLayout.Hint = "Amount"; 
inputLayout.HelperText = "Required *"
inputLayout.InputView = new SfNumericTextBox() { Value = 123.45, FormatString="c" }; 

{% endhighlight %}

{% endtabs %}


![Numerictextbox](Supported-input-views-images/textInput_input_img4.PNG)

## Auto complete

To initialize the auto complete control and launch it in each platform, refer to the [getting started with auto complete](https://help.syncfusion.com/xamarin/sfautocomplete/getting-started) documentation.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Country name">
   <autocomplete:SfAutoComplete x:Name="autoComplete"/>
</inputLayout:SfTextInputLayout>

{% endhighlight %}

{% highlight C# %} 

List<String> countryNames = new List<String>();
countryNames.Add("Uganda");
countryNames.Add("Ukraine");
countryNames.Add("Canada");
countryNames.Add("United Arab Emirates");
countryNames.Add("France");
countryNames.Add("United Kingdom");
countryNames.Add("China");
countryNames.Add("United States");
countryNames.Add("Japan");
autoComplete.DataSource = countryNames;

{% endhighlight %}

{% endtabs %}

![Autocomplete](Supported-input-views-images/textInput_input_img5.PNG)

## Combo box

To initialize the combo box control and launch it in each platform, refer to the [getting started with combo box](https://help.syncfusion.com/xamarin/sfcombobox/getting-started) documentation.

{% tabs %} 

{% highlight xaml %} 

<inputLayout:SfTextInputLayout Hint="Country name">
   <combobox:SfComboBox  x:Name="combobox"/>
</inputLayout:SfTextInputLayout> 

{% endhighlight %}

{% highlight C# %} 

List<String> countryNames = new List<String>();
countryNames.Add("Uganda");
countryNames.Add("Ukraine");
countryNames.Add("Canada");
countryNames.Add("United Arab Emirates");
countryNames.Add("France");
countryNames.Add("United Kingdom");
countryNames.Add("China");
countryNames.Add("United States");
countryNames.Add("Japan");
combobox.DataSource = countryNames;

{% endhighlight %}

{% endtabs %}

![Combobox](Supported-input-views-images/textInput_input_img6.PNG)