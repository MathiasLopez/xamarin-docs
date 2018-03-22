---
layout: post
title: Chart Title
description: How to add and customize the chart title in Essential Xamarin.Forms. 
platform: xamarin
control: Chart
documentation: ug
---

# Chart Title

You can define and customize the title of a chart using the [`Title`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Title.html) property of [`SfChart`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). The [`Text`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~Text.html) property of [`ChartTitle`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle.html) is used to set the text for the title. 

The following properties are used to customize its appearance:

* [`TextColor`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~TextColor.html)—Used to change the color of the text.
* [`BackgroundColor`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~BackgroundColor.html)—Used to change the background color.
* [`BorderColor`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~BorderColor.html)—Used to change the border color.
* [`BorderWidth`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~BorderWidth.html)—Used to change the border width.
* [`Font`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~Font.html)—Used to change the text size, font-family, and font-weight.
* [`Margin`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~Margin.html)—Used to change the margin for title.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>

	<chart:SfChart.Title>

		<chart:ChartTitle Text="Efficiency of oil-fired power production" TextColor="Blue"/>

	</chart:SfChart.Title>  

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart sfChart = new SfChart();

sfChart.Title.Text = "Efficiency of oil-fired power production";

sfChart.Title.TextColor = Color.Blue;

{% endhighlight %}

{% endtabs %}

![](charttitle_images/charttitle_img1.png)

## Text alignment

You can align the text of the title to the start, center, or end using the [`TextAlignment`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle~TextAlignment.html) property of [`ChartTitle`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartTitle.html).

{% tabs %} 

{% highlight xaml %}

<chart:SfChart.Title>

	<chart:ChartTitle Text="Efficiency of oil-fired power production" TextAlignment="Start" TextColor="Blue"/>

</chart:SfChart.Title>  

{% endhighlight %}

{% highlight c# %}

sfChart.Title.Text = "Efficiency of oil-fired power production";

sfChart.Title.TextAlignment = TextAlignment.Start;

sfChart.Title.TextColor = Color.Blue;

{% endhighlight %}

{% endtabs %}

![](charttitle_images/charttitle_img2.png)