---
layout: post
title: Visual customization for Syncfusion.Xamarin.Forms SfCheckBox
description: Learn how to customize the basic features of SfCheckBox
platform: Xamarin.Forms
control: SfCheckBox
documentation: ug 
keywords: button, SfCheckBox, CheckBox

---

# Visual Customization

## Customizing shape
The check box shape can be customized using the `CornerRadius` property. This property specifies uniform radius value for every corner of the check box.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfCheckBox x:Name="checkBox" Text="CheckBox" IsChecked="True" CornerRadius="5.0"/>            
{% endhighlight %}
{% highlight c# %}
SfCheckBox checkBox = new SfCheckBox();
checkBox.Text = "CheckBox";
checkBox.IsChecked = true;
checkBox.CornerRadius = 5.0f;
{% endhighlight %}
{% endtabs %}

![Radius Image](Images/Radius.png)

## Customizing state color
The default state colors can be customized using the `CheckedColor` and `UncheckedColor` properties. The checked/indeterminate state color is updated to the `CheckedColor` property value when the state is changed to the checked/indeterminate.The unchecked state color is updated to `UncheckedColor` property value when the state is changed to unchecked. 
{% tabs %}
{% highlight xaml %}
<syncfusion:SfCheckBox x:Name="check" Text="CheckBox" IsChecked="True" CheckedColor="Green"/>
<syncfusion:SfCheckBox x:Name="uncheck" Text="CheckBox" UncheckedColor="Violet"/>
<syncfusion:SfCheckBox x:Name="indeterminate " Text="CheckBox" IsThreeState="True" IsChecked="{x:Null}" CheckedColor="Purple"/> 
{% endhighlight %}
{% highlight c# %}
SfCheckBox check= new SfCheckBox();
check.Text = "CheckBox";
check.IsChecked = true;
check.CheckedColor = Color.Green;
SfCheckBox uncheck = new SfCheckBox();
uncheck.Text = "CheckBox";
uncheck.UncheckedColor = Color.Violet;
SfCheckBox indeterminate = new SfCheckBox();
indeterminate.IsChecked = null;
indeterminate.IsThreeState = true;
indeterminate.Text = "CheckBox";
indeterminate.CheckedColor = Color.Purple;
{% endhighlight %}
{% endtabs %}

![State color image](Images/StateColor.png)

## Setting caption text appearance 
You can customize the display text appearance of the `SfCheckBox` control using the following properties:

* `TextColor`: Changes the color of the text.
* `HorizontalTextAlignment`: Changes the horizontal alignment of the caption text.
* `FontFamily`: Changes the font family of the caption text.
* `FontAttributes`: Sets font attributes(bold/italic/none) of the caption text.
* `FontSize`: Sets font size of the caption text.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfCheckBox x:Name="caption" Text="CheckBox" IsChecked="True" TextColor="Violet" HorizontalTextAlignment="Center" FontFamily="Arial" FontAttributes="Bold" FontSize="20"/>           
{% endhighlight %}
{% highlight c# %}
SfCheckBox caption = new SfCheckBox();
caption.IsChecked = true;
caption.Text = "CheckBox";
caption.TextColor = Color.Violet;
caption.HorizontalTextAlignment = TextAlignment.Center;
caption.FontFamily = "Arial";
caption.FontAttributes = FontAttributes.Bold;
caption.FontSize = 20;
{% endhighlight %}
{% endtabs %}

![CaptionAppearance image](Images/CaptionAppearance.png)

## LineBreakMode
`LineBreakMode` allows you to wrap or truncate the text. The default value of this property is `NoWrap`. Other available options of LineBreakMode are listed below.

 * `NoWrap` - Used to avoid the text wrap. 
 * `WordWrap` - Used to wrap by words.
 * `CharacterWrap` - Used to wrap words by characters.
 * `HeadTruncation` - Truncate the head of text. 
 * `MiddleTruncation` - Truncate the center of text.
 * `TailTruncation` - Truncate the tail of text.
 
## TickColor Customization
The `TickColor` property customizes the color of the tick in SfCheckBox.

{% tabs %}
{% highlight xaml %}
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:syncfusion="clr-namespace:Syncfusion.XForms.Buttons;assembly=Syncfusion.Buttons.XForms"  x:Class="CheckBoxCustomization.checkbox">
     <ContentPage.Content>
            <StackLayout>
                <syncfusion:SfCheckBox x:Name="checkBox" IsChecked="True" CheckedColor="Aqua" TickColor="Fuchsia" Text="CheckBox" />
            </StackLayout>
        </ContentPage.Content>
</ContentPage>
{% endhighlight %}
{% highlight c# %}
using System;
using Syncfusion.XForms.Buttons;
using Xamarin.Forms;

namespace CheckBoxCustomization
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            StackLayout stackLayout = new StackLayout();
            SfCheckBox checkBox = new SfCheckBox();
            checkBox.IsChecked = true;
            checkBox.Text = "CheckBox";
            checkBox.CheckedColor = Color.Aqua;
            checkBox.TickColor = Color.Fuchsia;
            stackLayout.Children.Add(checkBox);
            this.Content = stackLayout;
{% endhighlight %}
{% endtabs %}

![SfCheckBox with TickColor](Images/TickColor.png)

N> The `TickColor` is not applicable for Android Platform. The default value of TickColor is [`Color.White`].

This demo can be downloaded from this [link](http://www.syncfusion.com/downloads/support/directtrac/general/ze/CheckBox_VisualCustomization881578223).