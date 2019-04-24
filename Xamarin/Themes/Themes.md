---
layout: post
title: Applying themes
description: This section explains about theming in Syncfusion controls and how to override the key values for further customization
platform: xamarin
control: General
documentation: ug
---

# Applying themes

Syncfusion themes allow you apply uniform colors across all the Syncfusion controls which provides consistent look and feel for your application. In this section, we will cover the following items. 

* Applying light and dark theme
* Overrding the default theme 
* Creating your own theme

## Applying light and dark theme

By default, we provide support for light and dark themes. As the name suggests, these themes will have colors which has lighter and darker color contrasts respectively.

In order to apply themes for your application, it is needed to merge the following items.

* Theme resource dictionary
* Control style resource dictionaries

### Theme resource dictionary

This resource file contains *keys* and their respective color codes for all the Syncfusion controls. When this resource file is merged in application resources along with the control style resource dictionaries, themes will be applied to the controls used in application. You can find the keys and the elements to which they are mapped for all the controls in this [link](https://help.syncfusion.com/xamarin/themes/keys). 

### Control style resource dictionaries

Each Syncfusion control has a style resource dictionary whose styles are mapped to the keys declared in theme resource dictionary.

{% highlight xaml %}
<Application xmlns:syncTheme="clr-namespace:Syncfusion.XForms.Themes;assembly=Syncfusion.Core.XForms"
xmlns:inputLayout="clr-namespace:Syncfusion.XForms.TextInputLayout;assembly=Syncfusion.Core.XForms"
             ...>
<Application.Resources>
        <ResourceDictionary>
            < ResourceDictionary.MergedDictionaries>
                <!-- Theme resource dictionary -->
                <syncCore:LightTheme />
                <!-- Control style resource dictionary -->
                <textinputlayout:SfTextInputLayoutStyles/>
            </ ResourceDictionary.MergedDictionaries>
        </ ResourceDictionary >
</Application.Resources>

....

</Application>

{% endhighlight %}

## Merging theme dictionaries

You can merge the resource dictionaries in the following two ways.

### Manual merging

For manual merging, both the common resource and each control style resource dictionaries need to be merged for the required controls in the application resources as follows.

{% highlight xaml %}
<Application xmlns:syncTheme="clr-namespace:Syncfusion.XForms.Themes;assembly=Syncfusion.Core.XForms"
xmlns:inputLayout="clr-namespace:Syncfusion.XForms.TextInputLayout;assembly=Syncfusion.Core.XForms"
             ...>
<Application.Resources>
        <ResourceDictionary>
            < ResourceDictionary.MergedDictionaries>
                <syncCore:LightTheme />
                <textinputlayout:SfTextInputLayoutStyles/>
            </ ResourceDictionary.MergedDictionaries>
        </ ResourceDictionary >
</Application.Resources>

....

</Application>

{% endhighlight %}

### Automatic merging

When using more number of Syncfusion controls in an application, to make the process easier for merging the control style dictionary of the controls, the SyncfusionThemeDictionary class has been provided for automatic merging. When the common theme resource dictionary is merged to this dictionary, control style resource dictionaries will be merged automatically. However, only the styles for the controls will be merged.

{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.XForms.Themes;assembly=Syncfusion.Core.XForms"
             ...>

<Application.Resources>
    <syncTheme:SyncfusionThemeDictionary>
        <syncTheme:SyncfusionThemeDictionary.MergedDictionaries>
            <syncTheme:LightTheme />
        </syncTheme:SyncfusionThemeDictionary.MergedDictionaries>
    </syncTheme:SyncfusionThemeDictionary>
</Application.Resources>

....

</Application>

{% endhighlight %}

## Common and control specific keys

The common theme resource dictionary has the following set of keys, which are mapped to specific elements in all our controls. To override the overall appearance of a theme, change the values for the keys as required.

* SyncPrimaryColor
* SyncPrimaryLightColor
* SyncPrimaryDarkColor
* SyncPrimaryForegroundColor
* SyncPrimaryLightForegroundColor
* SyncPrimaryDarkForegroundColor
* SyncSuccessColor
* SyncErrorColor
* SyncWarningColor
* SyncInfoColor

In addition to this, you can also override the keys that are specific to the controls. You can find the keys and the elements to which they are mapped for all the controls in this [link](https://help.syncfusion.com/xamarin/themes/keys).

The following section explains how to override both the common and control specific keys.

### Overriding key values

You can override the default values for the keys as needed by changing the values for the keys after merging the common theme resource dictionary.

{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.XForms.Themes;assembly=Syncfusion.Core.XForms"
             ...>
<Application.Resources>
    <syncCore:SyncfusionThemeDictionary>
        <syncCore:SyncfusionThemeDictionary.MergedDictionaries>
            <syncCore:LightTheme />
            <ResourceDictionary>
                <Color x:Key="SyncPrimaryColor">Green</Color>
                <Color x:Key="SfTextInputLayoutHintColor">Red</Color>
            </ResourceDictionary>
        </syncCore:SyncfusionThemeDictionary.MergedDictionaries>
    </syncCore:SyncfusionThemeDictionary>
</Application.Resources>

....

</Application>

{% endhighlight %}

## Applying themes without resource dictionaries

You can customize the appearance of the controls without merging common theme resource and control style resource dictionaries in application resources.

In the following example, the UI elements of SfTextInputLayout are customized by merging the resource with the 'SfTextInputLayoutTheme' key name, and values are set to the required keys in the next line. Similar to this, you can customize the appearance of other controls by merging the resource with the "ControlName" + "Theme" key name and setting values to the required keys of the control in the next line. 

You can find the keys and the elements to which they are mapped for all the controls in this [link](https://help.syncfusion.com/xamarin/themes/keys).

{% highlight xaml %}

<Application xmlns:syncTheme="clr-namespace:Syncfusion.XForms.Themes;assembly=Syncfusion.Core.XForms"
             ...>
<Application.Resources>
    <syncCore:SyncfusionThemeDictionary>
        <syncCore:SyncfusionThemeDictionary.MergedDictionaries>
            <ResourceDictionary>
                <x:String x:Key="SfTextInputLayoutTheme">CustomTheme</x:String> 
                <Color x:Key="SfTextInputLayoutCounterLabelColor">Blue</Color> 
                <Color x:Key="SfTextInputLayoutCounterLabelDisabledColor">Green</Color> 
            </ResourceDictionary>
        </syncCore:SyncfusionThemeDictionary.MergedDictionaries>
    </syncCore:SyncfusionThemeDictionary>
</Application.Resources>

....

</Application>

{% endhighlight %}