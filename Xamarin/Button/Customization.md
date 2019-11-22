---
layout: post
title: Customization for Syncfusion Essential Xamarin.Forms SfButton
description: This section describes how to customize the appearance of text, background and image for SfButton in Xamarin.Forms.
platform: xamarin.forms
control: sfbutton
documentation: ug
---

# Customization

The button control supports to customize the border color, image width, corner radius, background color, and more. The button control can be customized using the following properties:

## Text Customization

The text inside the button can be customized by its text color, font size, font attributes, font family and text alignment.

### TextColor

The [`TextColor`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~TextColor.html) property is used to customize the color of text in SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" TextColor = "White">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.TextColor = Color.White;

{% endhighlight %}
{% endtabs %}

![SfButton with text color](images/Button_textcolor.png)

### FontSize

The [`FontSize`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~FontSize.html) property is used to customize the size of text in SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" FontSize = "18">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.FontSize = 18;

{% endhighlight %}
{% endtabs %}

![SfButton with font size](images/Button_fontsize.png)

### FontAttributes

The [`FontAttributes`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~FontAttributes.html) property is used to customize the font style of text in SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" FontAttributes = "Italic">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.FontAttributes = FontAttributes.Italic;

{% endhighlight %}
{% endtabs %}

![SfButton with fontattributes](images/Button_fontattributes.png)

### FontFamily

The [`FontFamily`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~FontFamily.html) property is used to customize the font family of text in SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" FontFamily = "Arial">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.FontFamily = "Arial";

{% endhighlight %}
{% endtabs %}

![SfButton with fontfamily](images/Button_fontfamily.png)

### TextAlignment

The [`HorizontalTextAlignment `](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~HorizontalTextAlignment.html) and [`VerticalTextAlignment `](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~VerticalTextAlignment.html) properties are used to customize the alignment of text in SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" HorizontalTextAlignment="Center" VerticalTextAlignment="Center">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.HorizontalTextAlignment = TextAlignment.Center;
button.VerticalTextAlignment = TextAlignment.Center;

{% endhighlight %}
{% endtabs %}

## Background Customization

The background of the button can be customized by its background color, border color, border width and corner radius.

### BackgroundColor

The [`BackgroundColor`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~BackgroundColor.html) property is used to customize the background color of SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" BackgroundColor = "DeepSkyBlue">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.BackgroundColor = Color.DeepSkyBlue;

{% endhighlight %}
{% endtabs %}

![SfButton with background color](images/Button_backgroundcolor.png)

### BorderColor

The [`BorderColor`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~BorderColor.html) property is used to customize the color of border in SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" BorderColor = "Red" BorderWidth="4">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.BorderWidth = 4;
button.BorderColor = Color.Red;

{% endhighlight %}
{% endtabs %}

![SfButton with border](images/Button_border.png)

### BorderWidth

The [`BorderWidth`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~BorderWidth.html) property is used to customize the thickness of border in SfButton. 

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" BorderColor = "Red" BorderWidth="4">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.BorderWidth = 4;
button.BorderColor = Color.Red;

{% endhighlight %}
{% endtabs %}

### CornerRadius

The `CornerRadius` property is used to customize the rounded edges in SfButton as demonstrated in the following code sample.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" CornerRadius="3">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.CornerRadius = 3;

{% endhighlight %}
{% endtabs %}

![SfButton with cornerradius](images/Button_cornerradius.png)

## Image Customization

The image can be customized by its show icon, image source, image width and image alignment.

### ShowIcon

You can enable the Icon image using the [`ShowIcon`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ShowIcon.html) property to know whether any image appears to the SfButton.

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = True;

{% endhighlight %}
{% endtabs %}

### ImageSource

The [`ImageSource`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ImageSource.html) property is used to customize the icon image of SfButton by adding a custom image.

N> Enable the [`ShowIcon`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ShowIcon.html) property to enable the [`ImageSource`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ImageSource.html) property. 

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = True;

{% endhighlight %}
{% endtabs %}

![SfButton with image with content](images/Button_icon.png)

### ImageWidth

The [`ImageWidth`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ImageWidth.html) property is used to customize the width of icon image in SfButton.

N> Enable the [`ShowIcon`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ShowIcon.html) property to enable the [`ImageSource`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ImageSource.html) property. 

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True" ImageWidth="50">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = true;
button.ImageWidth = 50;

{% endhighlight %}
{% endtabs %}

### ImageAlignment 

The [`ImageAlignment`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ImageAlignment.html) property is used to customize the alignment of icon image in SfButton.

N> Enable the [`ShowIcon`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ShowIcon.html) property to enable the [`ImageSource`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~ImageSource.html) property. 

{% tabs %}
{% highlight xaml %}

<button:SfButton x:Name="button" Text="Button" ImageSource="Heart.png" ShowIcon="True" ImageAlignment="End">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

SfButton button = new SfButton();
button.Text = "Button";
button.ImageSource = "Heart.png";
button.ShowIcon = true;
button.ImageAlignment = Alignment.End;

{% endhighlight %}
{% endtabs %}

![SfButton with image with icon image alignment](images/Button_iconalignment.png)

## Gradient background

You can set the gradient as background of SfButton using the [`BackgroundGradient`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~BackgroundGradient.html) property. It supports the following types of gradients:

* Linear gradient
* Radial gradient

N> UWP platform does not support radial gradient.

Refer to this [documentation](https://help.syncfusion.com/xamarin/sfgradientview/customization) to learn more details about gradient.

{% tabs %}
{% highlight xaml %}

xmlns:gradient ="clr-namespace:Syncfusion.XForms.Graphics;assembly=Syncfusion.Core.XForms"

. . . 

<button:SfButton Text="Linear Gradient" CornerRadius="20">
    <button:SfButton.BackgroundGradient>
        <gradient:SfLinearGradientBrush>
            <gradient:SfLinearGradientBrush.GradientStops>
                <gradient:SfGradientStop Color="#2F9BDF" Offset="0"/>
                <gradient:SfGradientStop Color="#51F1F2" Offset="1"/>
            </gradient:SfLinearGradientBrush.GradientStops>
        </gradient:SfLinearGradientBrush>
    </button:SfButton.BackgroundGradient>
</button:SfButton>

<button:SfButton Text="Radial Gradient" CornerRadius="20">
    <button:SfButton.BackgroundGradient>
        <gradient:SfRadialGradientBrush Radius="1.5">
            <gradient:SfRadialGradientBrush.GradientStops>
                <gradient:SfGradientStop Color="#FFB57B" Offset="0"/>
                <gradient:SfGradientStop Color="#FF5361" Offset="1"/>
            </gradient:SfRadialGradientBrush.GradientStops>
        </gradient:SfRadialGradientBrush>
    </button:SfButton.BackgroundGradient>
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

using Syncfusion.XForms.Graphics;

. . .

SfButton linearButton = new SfButton();
linearButton.Text = "Linear Gradient";
linearButton.CornerRadius = 20;
SfLinearGradientBrush linearGradientBrush = new SfLinearGradientBrush();
linearGradientBrush.GradientStops = new GradientStopCollection()
{
    new SfGradientStop(){ Color = Color.FromHex("#2F9BDF"), Offset = 0 },
    new SfGradientStop(){ Color = Color.FromHex("#51F1F2"), Offset = 1 }
};     
linearButton.BackgroundGradient = linearGradientBrush;

SfButton radialButton = new SfButton();
radialButton.Text = "Radial Gradient";
radialButton.CornerRadius = 20;
SfRadialGradientBrush radialGradientBrush = new SfRadialGradientBrush();
radialGradientBrush.Radius = 1.5;
radialGradientBrush.GradientStops = new GradientStopCollection()
{
    new SfGradientStop(){ Color = Color.FromHex("#FFB57B"), Offset = 0 },
    new SfGradientStop(){ Color = Color.FromHex("#FF5361"), Offset = 1 }
};
radialButton.BackgroundGradient = radialGradientBrush;

{% endhighlight %}
{% endtabs %}

![Xamarin.Forms gradient support](images/Button_gradient.png)

## Command

The [`Command`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfButton~Command.html)  property is used to associate a command with an instance of SfButton. This property is most often set with MVVM pattern to bind callbacks back into the ViewModel.

N> Default value is [`null`].

{% tabs %}
{% highlight xaml %}

 <ContentPage.BindingContext>
    <local:CommandDemoViewModel />
 </ContentPage.BindingContext>

<button:SfButton x:Name="button" Text="Button" BackgroundColor="{Binding Background}" Command="{Binding ButtonCommand}">
</button:SfButton>

{% endhighlight %}
{% highlight c# %}

// ViewModel

public class CommandDemoViewModel : INotifyPropertyChanged
{

    private Color _background = Color.Accent;

    public Color Background
    {
        get { return _background; }
        set
        {
            _background = value;
            NotifyPropertyChanged();
        }
    }

    private void NotifyPropertyChanged([CallerMemberName] String propertyName = "")
    {
        PropertyChanged?.Invoke(this, new PropertyChangedEventArgs(propertyName));
    }

    public event PropertyChangedEventHandler PropertyChanged;

    public CommandDemoViewModel()
    {
        SetBackgroundColor();
        this.Background=Color.Accent;
    }

    private void SetBackgroundColor()
    {
	    //do whatever you want to do here
        this.Background = this.Background == Color.DeepSkyBlue ? Color.Accent : Color.DeepSkyBlue;
    }

    public ICommand ButtonCommand => new Command(SetBackgroundColor);

}

{% endhighlight %}
{% endtabs %}

## Shadow Effect

The button control provides shadow effect support. To enable shadow effect, set the `HasShadow` property to true.

You can customize the color of shadow using the `ShadowColor` property. 

{% tabs %}

{% highlight xaml %}

          <SyncfusionButton:SfButton
                                     HeightRequest="50"
                                     WidthRequest="200"
                                     VerticalOptions="Center"
                                     HorizontalOptions="Center"
                                     CornerRadius="25"
                                     HasShadow="True"
                                     BorderWidth="1"
                                     BorderColor="Gray"
                                     BackgroundColor="#538EEC"
                                     ImageSource="Basket.png"
                                     ShowIcon="True"
                                     ImageAlignment="End"
                                     Text="ADD To CART"/>
	
{% endhighlight %}

{% highlight C# %}

SfButton button = new SfButton()
            {
                HeightRequest = 50,
                WidthRequest = 200,
                HorizontalOptions = LayoutOptions.Center,
                VerticalOptions = LayoutOptions.Center,
                CornerRadius = new Thickness(25),
                HasShadow = true,
                BorderWidth = 1,
                BorderColor = Color.Gray,
                BackgroundColor = Color.FromHex("#538EEC"),
                ImageSource = "Basket.png",
                ShowIcon = true,
                ImageAlignment = Alignment.Start,
                Text = "ADD To CART"
            };

            this.Content = button;

{% endhighlight %}

{% endtabs %}

N> Shadow support has not been provided for UWP Platform.

![ShadowImage](images/Xamarin_Forms_Shadow.png)

The complete customization sample:[Customization](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Customization-1070507783)