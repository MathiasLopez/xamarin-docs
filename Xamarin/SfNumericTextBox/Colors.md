---
layout: post
title: Colors in Syncfusion NumericTextBox control for Xamarin.Forms
description: Learn what are the color properties in  NumericTextBox
platform: Xamarin
control: NumericTextBox
documentation: ug
---
# Colors

SfNumericTextBox can be set to use a custom background,text and border colors via the following bindable properties:

* `TextColor` - sets the color of the NumericTextBox's value.

* `BackgroundColor` - sets the background color of NumericTextBox's frame.

* `BorderColor` - sets the border custom color of NumericTextBox

* `WatermarkColor` - sets the watermark custom color of NumericTextBox's watermark Text.

### TextColor

To set the TextColor color in XAML as well as in C#:

{% tabs %}

{% highlight xaml %}

	<syncfusion:SfNumericTextBox x:Name="numericTextBox" Value="123" TextColor="Green" />
	
{% endhighlight %}

{% highlight c# %}

SfNumericTextBox numericTextBox=new SfNumericTextBox();
numericTextBox.TextColor = Color.Green;
numericTextBox.Value = 123;
this.Content = numericTextBox;

{% endhighlight %}

{% endtabs %}

![](images/textcolor.png)

### BackgroundColor

To set the BackgroundColor color in XAML as well as in C#:

{% tabs %}

{% highlight xaml %}

	<syncfusion:SfNumericTextBox x:Name="numericTextBox" Value="123" BackgroundColor="Maroon" TextColor="White"/>
	
{% endhighlight %}

{% highlight c# %}

SfNumericTextBox numericTextBox=new SfNumericTextBox();
numericTextBox.BackgroundColor = Color.Maroon;
numericTextBox.TextColor = Color.White;
numericTextBox.Value = 123;
this.Content = numericTextBox;

{% endhighlight %}

{% endtabs %}

![](images/backgroundcolor.png)

### BorderColor

To set the BorderColor color in XAML as well as in C#:

{% tabs %}

{% highlight xaml %}

	<syncfusion:SfNumericTextBox x:Name="numericTextBox" Value="123" BorderColor="Red" />
	
{% endhighlight %}

{% highlight c# %}

SfNumericTextBox numericTextBox=new SfNumericTextBox();
numericTextBox.BorderColor = Color.Red;
numericTextBox.Value = 123;
this.Content = numericTextBox;

{% endhighlight %}

{% endtabs %}

![](images/bordercolor.png)

### WatermarkColor

To set the WatermarkColor color in XAML as well as in C#:

{% tabs %}

{% highlight xaml %}

	<syncfusion:SfNumericTextBox  x:Name="numericTextBox" AllowNull="true" Value="123" WatermarkColor="Blue" />
	
{% endhighlight %}

{% highlight c# %}

SfNumericTextBox numericTextBox=new SfNumericTextBox();
numericTextBox.WatermarkColor = Color.Blue;
numericTextBox.Value = 123;
numericTextBox.AllowNull=true;
this.Content = numericTextBox;

{% endhighlight %}

{% endtabs %}

![](images/watermarkcolor.png)
