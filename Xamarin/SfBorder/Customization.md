---
layout: post
title: Various customization in Syncfusion border control for Xamarin.Forms
description: Learn how to customize the border control
platform: Xamarin
control: SfBorder
documentation: ug
---

# Customization

The border control supports customizing the border color, width, corner radius, background color, and more. The border can be customized using the following properties.

## Border color

You can customize the color of the border using the `BorderColor` property.

{% tabs %}
{% highlight xaml %}

<border:SfBorder x:Name="border" BorderColor = "Red"  CornerRadius="20" BorderWidth="3">
 <Label Text="James Williamson" 
 TextColor="Black"/>
</border:SfBorder>

{% endhighlight %}
{% highlight c# %}

SfBorder border = new SfBorder();
border.CornerRadius = 20;
border.BorderColor = Color.Red;
border.BorderWidth = 3;
Label label = new Label();
label.Text = "James Williamson";
label.TextColor = Color.Black;
border.Content = label;
this.Content = border;

{% endhighlight %}
{% endtabs %}

![bordercolor](images/Xamarin_Forms_BorderColor.png)

## Background color

The background color of the border control can be customized using the `BackgroundColor` property.

{% tabs %}
{% highlight xaml %}

<border:SfBorder x:Name="border" BorderColor = "Red" BackgroundColor= "Green" CornerRadius="20" BorderWidth="3">
 <Label Text="James Williamson" 
 TextColor="Black"/>
</border:SfBorder>

{% endhighlight %}
{% highlight c# %}

SfBorder border = new SfBorder();
border.CornerRadius = 20;
border.BorderColor = Color.Red;
border.BorderWidth = 3;
Label label = new Label();
label.Text = "James Williamson";
label.TextColor = Color.Black;
border.Content = label;
border.BackgroundColor = Color.Green;
this.Content = border;

{% endhighlight %}
{% endtabs %}

![backgroundcolor](images/Xamarin_Forms_BackgroundColor.png)

## Border width

You can customize the thickness of the border using the `BorderWidth` property.

{% tabs %}
{% highlight xaml %}

<border:SfBorder x:Name="border" BorderColor = "Red" CornerRadius="20" BorderWidth="12">
 <Label Text="James Williamson" 
 TextColor="Black"/>
</border:SfBorder>

{% endhighlight %}
{% highlight c# %}

SfBorder border = new SfBorder();
border.CornerRadius = 20;
border.BorderColor = Color.Red;
border.BorderWidth = 12;
Label label = new Label();
label.Text = "James Williamson";
label.TextColor = Color.Black;
border.Content = label;
this.Content = border;


{% endhighlight %}
{% endtabs %}

![borderwidth](images/Xamarin_Forms_BorderWidth.png)

## Corner radius

You can customize the corner radius of the border on four sides using the `CornerRadius` property with type as `Thickness`.

{% tabs %}
{% highlight xaml %}

<border:SfBorder x:Name="border" BorderColor = "Red" CornerRadius="0,10,10,0" BorderWidth="12">
 <Label Text="James Williamson" 
 TextColor="Black"/>
</border:SfBorder>

{% endhighlight %}
{% highlight c# %}

SfBorder border = new SfBorder();
border.CornerRadius =  new Thickness (0,10,10,0);
border.BorderColor = Color.Red;
border.BorderWidth = 12;
Label label = new Label();
label.Text = "James Williamson";
label.TextColor = Color.Black;
border.Content = label;
this.Content = border;

{% endhighlight %}
{% endtabs %}

![cornerradius](images/Xamarin_Forms_CornerRadius.png)

## Adding circular image

You can add any view inside the border control by adding the Content property. The following code sample demonstrates how to apply border using the `CornerRadius` property for a circular image.

{% tabs %}
{% highlight xaml %}

<Grid HeightRequest="100" WidthRequest="100" HorizontalOptions="Center" VerticalOptions="Center">
    <border:SfBorder BorderColor="Black" HorizontalOptions="Center" VerticalOptions="Center" CornerRadius="50">
    <Image Source="plus.jpeg" />
    </border:SfBorder>
</Grid>

{% endhighlight %}
{% highlight c# %}

Grid grid = new Grid();
grid.HeightRequest = 100;
grid.WidthRequest = 100;
grid.HorizontalOptions = LayoutOptions.Center;
grid.VerticalOptions = LayoutOptions.Center;
SfBorder border = new SfBorder();
border.BorderColor = Color.Black;
border.HorizontalOptions = LayoutOptions.Center;
border.VerticalOptions = LayoutOptions.Center;
border.CornerRadius = 50;
Image image = new Image();
image.Source = "plus.jpeg";
border.Content = image;
grid.Children.Add(border);
this.Content = grid;

{% endhighlight %}
{% endtabs %}

![circularimage](images/Xamarin_Forms_CircularImage.png)

## Shadow Effect

The border control provides shadow effect support. To enable shadow effect, set the `HasShadow` property to true.

You can customize the color of shadow using the `ShadowColor` property. 

{% tabs %}

{% highlight xaml %}

  <border:SfBorder 
                HorizontalOptions="Center" 
                VerticalOptions="Center"
                BackgroundColor="Green"
                HeightRequest="50"
                WidthRequest="200" 
                CornerRadius="20" 
                BorderWidth="0" 
                HasShadow="True"
                ShadowColor="Gray">
            <Label 
                    Text="James Williamson" 
                    HorizontalTextAlignment="Center" 
                    VerticalTextAlignment="Center" 
                    TextColor="White"/>
        </border:SfBorder>
	
{% endhighlight %}

{% highlight C# %}

SfBorder border = new SfBorder()
            {
                BackgroundColor = Color.Green,
                CornerRadius = 20,
                BorderWidth = 0,
                HeightRequest = 50,
                WidthRequest = 200,
                HorizontalOptions = LayoutOptions.Center,
                VerticalOptions = LayoutOptions.Center,
                HasShadow = true,
                ShadowColor = Color.Gray
            };

            Label label = new Label()
            {
                Text = "James Williamson",
                HorizontalTextAlignment = TextAlignment.Center,
                VerticalTextAlignment = TextAlignment.Center,
                TextColor = Color.White
            };

            border.Content = label;
            this.Content = border;

{% endhighlight %}

{% endtabs %}

N> Shadow support has not been provided for UWP Platform.

![ShadowImage](images/Xamarin_Forms_Shadow.png)