---
layout: post
title: Chart types
description: What are the different types of Charts available in Essential Xamarin.forms Chart.
platform: xamarin
control: Chart
documentation: ug
---

# Chart Types

## Line Chart

To render a line chart, create an instance of [`LineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.LineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the line.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the line.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:LineSeries ItemsSource ="{Binding Data}" XBindingPath="Year"
	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

LineSeries lineSeries = new LineSeries()
{
	ItemsSource = Data,
	XBindingPath = "Year",
	YBindingPath = "Value"
};
chart.Series.Add(lineSeries);

{% endhighlight %}

{% endtabs %}

![Line chart type in Xamarin.Forms](charttypes_images/charttypes_img1.png)

## Fast Line Chart

[`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) is a line chart, but it loads faster than [`LineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.LineSeries.html). You can use this when there are large number of points to be loaded in chart. To render a fast line chart, create an instance of [`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the fast line segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:FastLineSeries ItemsSource ="{Binding Data}" XBindingPath="XValue" YBindingPath="YValue"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

FastLineSeries fastLineSeries = new FastLineSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "XValue", 
	YBindingPath = "YValue"  
};
chart.Series.Add(fastLineSeries);

{% endhighlight %}

{% endtabs %}

![FastLine chart type in Xamarin.Forms](charttypes_images/charttypes_img14.png)

### Dashed Lines

[`StrokeDashArray`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries~StrokeDashArray.html) property of the [`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) is used to render fast line series with dashes.

{% highlight c# %}
[C#]

FastLineSeries fastLineSeries = new FastLineSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};
fastLineSeries.StrokeDashArray = new double[2] { 2, 3 };

{% endhighlight %}

![Dashed lines support for FastLineSeries in Xamarin.Forms Chart](charttypes_images/charttypes_img15.png)

### EnableAntiAliasing 

Since [`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) can be loaded with a large number of points, the rendering of series should be smooth. This requirement can be achieved by setting [`EnableAntiAliasing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries~EnableAntiAliasing.html) property of [`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) as false.

## Area Chart

To render an area chart, create an instance of [`AreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AreaSeries~StrokeColor.html) – used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:AreaSeries ItemsSource ="{Binding Data}" XBindingPath="Year"
					  YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

AreaSeries areaSeries = new AreaSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};
chart.Series.Add(areaSeries);

{% endhighlight %}

{% endtabs %}

![Area chart type in Xamarin.Forms](charttypes_images/charttypes_img2.png)

## Spline Area Chart

To render a spline area chart, create an instance of [`SplineAreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the spline area appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries~StrokeColor.html) – used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:SplineAreaSeries ItemsSource ="{Binding Data}" XBindingPath="Year"
	                       	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

SplineAreaSeries splineAreaSeries = new SplineAreaSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};
chart.Series.Add(splineAreaSeries);

{% endhighlight %}

{% endtabs %}

![SplineArea chart type in Xamarin.Forms](charttypes_images/charttypes_img3.png)

### Spline Area Series Types

[`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries~SplineType.html) allows you to change the spline area curve in series. 
The following types are used in [`SplineAreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries.html) as 

 * [`Natural`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)
 * [`Monotonic`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)
 * [`Cardinal`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)
 * [`Clamped`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)

By default [`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries~SplineType.html) value is [`Natural`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html).

The following code shows how to set the [`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries~SplineType.html) value as [`Cardinal`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)

{% tabs %}

{% highlight xaml%}

<chart:SfChart>
...

	<chart:SplineAreaSeries ItemsSource ="{Binding Data}" XBindingPath="Month"
	  					YBindingPath="Value" SplineType="Cardinal" />

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

SplineAreaSeries splineAreaSeries = new SplineAreaSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Month", 
	YBindingPath = "Value",
	SplineType = SplineType.Cardinal
};
chart.Series.Add(splineAreaSeries);

{% endhighlight %}

{% endtabs %}


## Step Area Chart

To render a step area chart, create an instance of [`StepAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StepAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) - used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) - used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StepAreaSeries~StrokeColor.html) - used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

    <chart:StepAreaSeries ItemsSource ="{Binding Data}" XBindingPath="Year"
                            YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StepAreaSeries stepAreaSeries = new StepAreaSeries() 
{ 
    ItemsSource = Data, 
    XBindingPath = "Year", 
    YBindingPath = "Value" 
};
chart.Series.Add(stepAreaSeries);

{% endhighlight %}

{% endtabs %}

![StepArea chart type in Xamarin.Forms](charttypes_images/StepArea.png)

## Range Area Chart

To render a range area chart, create an instance of [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Since the [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html) requires two Y values for a point, your data should contain high and low values. High and low value specifies the maximum and minimum range of the point.

There are two ways you can provide data to range area chart,

1.You can use [`ChartDataPoint's`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html) three parameter constructor to pass [`XValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~XValue.html), [`High`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~High.html) and [`Low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Low.html) values to [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html),

{% highlight c# %}
[C#] 

SfChart chart = new SfChart();
...

ObservableCollection<ChartDataPoint> data = new ObservableCollection<ChartDataPoint>()
{
     new ChartDataPoint("Jan/10", 30, 18),
     new ChartDataPoint("Feb/10", 24, 12),
     new ChartDataPoint("Mar/10", 29, 15),
     new ChartDataPoint("Apr/10", 24, 10),
     new ChartDataPoint("May/10", 30, 18),
     new ChartDataPoint("Jun/10", 24, 10),
};

RangeAreaSeries rangeAreaSeries = new RangeAreaSeries()
{
     ItemsSource = data
};

chart.Series.Add(rangeAreaSeries);

{% endhighlight %}

2.Or else you can use [`High`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~High.html) and [`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~Low.html) properties of [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html) to map the high and low values from custom object to chart.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...
    <chart:SfChart.Series>
        <chart:RangeAreaSeries ItemsSource="{Binding RangeAreaData}" XBindingPath="Name" High="High" Low="Low"/>
    </chart:SfChart.Series>
</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

RangeAreaSeries rangeAreaSeries = new RangeAreaSeries()
{
     ItemsSource = RangeAreaData,
     XBindingPath = "Name",
     High = "High",
     Low = "Low"
};
chart.Series.Add(rangeAreaSeries);

{% endhighlight %}

{% endtabs %}

You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries~StrokeColor.html) – used to change the stroke color of the series.

![RangeArea chart type in Xamarin.Forms](charttypes_images/RangeArea.png)

## Spline Range Area Chart

To render a spline range area chart, create an instance of the [`SplineRangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries.html), and add that instance to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Since the [`SplineRangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries.html) requires two Y values for a point, data should contain high and low values. The high and low values specify the maximum and minimum ranges of a point.

The data can be provided to a spline range area chart by using the following two ways:

1.Using the [`ChartDataPoint’s`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html) three parameter constructor to pass [`XValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~XValue.html), [`High`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~High.html), and [`Low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Low.html) values to the [`SplineRangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries.html).

{% highlight c# %}
[C#] 

SfChart chart = new SfChart();
...

ObservableCollection<ChartDataPoint> data = new ObservableCollection<ChartDataPoint>()
{
     new ChartDataPoint("Jan", 30, 18),
     new ChartDataPoint("Feb", 24, 12),
     new ChartDataPoint("Mar", 29, 15),
     new ChartDataPoint("Apr", 24, 10),
     new ChartDataPoint("May", 30, 18),
     new ChartDataPoint("Jun", 24, 10),
};

SplineRangeAreaSeries splineRangeAreaSeries = new SplineRangeAreaSeries() 
{
	ItemsSource = data 
};

chart.Series.Add(splineRangeAreaSeries);

{% endhighlight %}

2.Or else, using the [`high`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~High.html) and [`low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~Low.html) properties of [`SplineRangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries.html) to map the high and low values from custom object to chart.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart> 
... 
	<chart:SfChart.Series> 
		<chart:SplineRangeAreaSeries ItemsSource="{Binding SplineRangeAreaData}" XBindingPath="Name" High="High" Low="Low"/> 
	</chart:SfChart.Series> 
</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart(); 
...

SplineRangeAreaSeries splineRangeAreaSeries = new SplineRangeAreaSeries() 
{ 
	ItemsSource = SplineRangeAreaData, 
	XBindingPath = "Name", 
	High = "High", 
	Low = "Low" 
}; 

chart.Series.Add(splineRangeAreaSeries);

{% endhighlight %}

{% endtabs %}

![SplineRangeArea chart type in Xamarin.Forms](charttypes_images/SplineRangeArea.png)

### Spline Range Area Series Type

[`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries~SplineType.html) property allows you to change the spline range area curve in series.

The following types can be used for SplineRangeAreaSeries
*	Natural 
*	Monotonic
*	Cardinal
*	Clamped

By default [`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries~SplineType.html) value is Natural.

The following code shows how to set the [`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineRangeAreaSeries~SplineType.html) value as Cardinal.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
… 
   <chart:SplineRangeAreaSeries ItemsSource="{Binding SplineRangeAreaData}" XBindingPath="Name" High="High" Low="Low" SplineType="Cardinal"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SplineRangeAreaSeries splineRangeAreaSeries = new SplineRangeAreaSeries
            {
                ItemsSource = SplineRangeAreaData,
                XBindingPath = "Name",
                High = "High",
                Low = "Low",
                SplineType = SplineType.Cardinal
            };

            chart.Series.Add(splineRangeAreaSeries);
			
{% endhighlight %}

{% endtabs %}

## Stacked Area Chart

To render a stacked area chart, create an instance of [`StackingAreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the stacked area appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:StackingAreaSeries ItemsSource ="{Binding Data1}" XBindingPath="Year" 
							  YBindingPath="Value"/>

	<chart:StackingAreaSeries ItemsSource ="{Binding Data2}" XBindingPath="Year" 
							  YBindingPath="Value"/>

	<chart:StackingAreaSeries ItemsSource ="{Binding Data3}" XBindingPath="Year" 
							  YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StackingAreaSeries stackingAreaSeries1 = new StackingAreaSeries() 
{ 
	ItemsSource = Data1, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingAreaSeries stackingAreaSeries2 = new StackingAreaSeries() 
{ 
	ItemsSource = Data2, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingAreaSeries stackingAreaSeries3 = new StackingAreaSeries() 
{ 
	ItemsSource = Data3, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

chart.Series.Add(stackingAreaSeries1);
chart.Series.Add(stackingAreaSeries2);
chart.Series.Add(stackingAreaSeries3);

{% endhighlight %}

{% endtabs %}

![StackedArea chart type in Xamarin.Forms](charttypes_images/charttypes_img4.png)

## 100% Stacked Area Chart

To render a 100% stacked area chart, create an instance of [`StackingArea100Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingArea100Series.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the 100% stacked area appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:StackingArea100Series ItemsSource ="{Binding Data1}" XBindingPath="Year" 
								 YBindingPath="Value"/>

	<chart:StackingArea100Series ItemsSource ="{Binding Data2}" XBindingPath="Year" 
								 YBindingPath="Value"/>

	<chart:StackingArea100Series ItemsSource ="{Binding Data3}" XBindingPath="Year" 
								 YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StackingArea100Series stackingArea100Series1 = new StackingArea100Series() 
{ 
	ItemsSource = Data1, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingArea100Series stackingArea100Series2 = new StackingArea100Series() 
{ 
	ItemsSource = Data2, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingArea100Series stackingArea100Series3 = new StackingArea100Series() 
{ 
	ItemsSource = Data3, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

chart.Series.Add(stackingArea100Series1);
chart.Series.Add(stackingArea100Series2);
chart.Series.Add(stackingArea100Series3);

{% endhighlight %}

{% endtabs %}

![StackingArea100 chart type in Xamarin.Forms](charttypes_images/charttypes_img5.png)

## Column Chart

To render a column chart, create an instance of [`ColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~StrokeColor.html) – used to change the stroke color of the series. 
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~DataMarkerPosition.html) - used to position the data marker at [`Bottom`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html), [`Top`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html) and [`Center`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html) of the rectangle. 
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~Spacing.html) - used to change the spacing between two segments. The default value of spacing is 0, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available space, respectively.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~Width.html) - used to change the width of the rectangle. The default value of the width is 0.8, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available width, respectively. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:ColumnSeries ItemsSource ="{Binding Data}" XBindingPath="Country" 
						YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

ColumnSeries columnSeries = new ColumnSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Country", 
	YBindingPath = "Value" 
};
chart.Series.Add(columnSeries);

{% endhighlight %}

{% endtabs %}

![Column chart type in Xamarin.Forms](charttypes_images/charttypes_img6.png)

## Overlapped placement

By default, all the column series which has the same x and y axes are placed side by side in a chart. If you want place the series one over the other (overlapped), set the [`SideBySideSeriesPlacement`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~SideBySideSeriesPlacement.html) property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html#) to false and configure the [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~Width.html) property to differentiate the series. The following code snippet and screenshot illustrate the overlapped placement of column series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart x:Name="Chart" SideBySideSeriesPlacement="False" >
      . . .
    <chart:SfChart.Series>
      <chart:ColumnSeries ItemsSource="{Binding Data1}" Label="2014" XBindingPath="Month" YBindingPath="Year2014">
       
      </chart:ColumnSeries>
     <chart:ColumnSeries  Width="0.5" ItemsSource="{Binding Data2}" Label="2015" XBindingPath="Month" YBindingPath="Year2015" >
       
      </chart:ColumnSeries>
    </chart:SfChart.Series>
    . . .
</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart()
  {
      SideBySideSeriesPlacement = false
  };
 chart.PrimaryAxis = new CategoryAxis();
 chart.SecondaryAxis = new NumericalAxis();
 ColumnSeries series1 = new ColumnSeries()
 {
                ItemsSource = view.Data1,
                XBindingPath = "Month",
                YBindingPath = "Year2014"
 };
 ColumnSeries series2 = new ColumnSeries()
 {
                ItemsSource = view.Data2,
                XBindingPath = "Month",
                YBindingPath = "Year2015",
                 Width="0.5"
 };

chart.Series.Add(series1);
chart.Series.Add(series2);

{% endhighlight %}

{% endtabs %}

![Overlapped placement support in Xamarin.Forms Chart](charttypes_images/SideBySide-false.png)

## Histogram Chart

To render a histogram chart, create an instance of [`HistogramSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HistogramSeries.html), and add it to the series collection of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Histogram chart provides a visual display of large amount of data that are difficult to understand in a tabular or data grid form.

You can customize intervals using the [`Interval`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HistogramSeries~Interval.html) property and collapse the normal distribution curve using the [`ShowNormalDistributionCurve`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HistogramSeries~ShowNormalDistributionCurve.html) property.  You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HistogramSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`CurveColor`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HistogramSeries~CurveColor.html) – used to change the color of the normal distribution curve.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HistogramSeries~DataMarkerPosition.html) - used to position the data marker at Bottom, Top and Center of the rectangle.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:HistogramSeries ItemsSource ="{Binding Data}" XBindingPath="XValue" 
						YBindingPath="YValue" Interval="20"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

HistogramSeries histogramSeries = new HistogramSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "XValue", 
	YBindingPath = "YValue",
	Interval = 20 
};
chart.Series.Add(histogramSeries);

{% endhighlight %}

{% endtabs %}

![Histogram chart type in Xamarin.Forms](charttypes_images/charttypes_img42.png)

## Range Column Chart

To render a range column chart, create an instance of [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). 

Since the [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html) requires two Y values for a point, your data should contain high and low values. High and low value specifies the maximum and minimum range of the point. 

There are two ways you can provide data to RangeColumn chart,

1.You can use [`ChartDataPoint's`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html#) three parameter constructor to pass [`XValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~XValue.html), [`High`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~High.html) and [`Low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Low.html) values to  [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html),

{% highlight c# %}
[C#] 

SfChart chart = new SfChart();
...

ObservableCollection<ChartDataPoint> data = new ObservableCollection<ChartDataPoint>()
{    
	new ChartDataPoint("Jan", 7.6, 1.8),
	new ChartDataPoint("Feb", 10, 3),
	new ChartDataPoint("Mar", 7.5, 1.7),
	new ChartDataPoint("Apr", 7.8, 4.5),
	new ChartDataPoint("May", 11.4, 5),
	new ChartDataPoint("Jun", 10.1, 4.2),
};
	
RangeColumnSeries rangeColumnSeries = new RangeColumnSeries() 
{ 
	ItemsSource = data 
};
	
chart.Series.Add(rangeColumnSeries);

{% endhighlight %}


2.Or else you can use [`High`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~High.html) and [`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~Low.html) properties of [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html) to map the high and low values from custom object to chart. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:RangeColumnSeries ItemsSource ="{Binding Data}"
							 XBindingPath="Month"
							 High="Value1" 
							 Low="Value2"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}
   
SfChart chart = new SfChart();
...
   
RangeColumnSeries rangeColumnSeries = new RangeColumnSeries() 
{ 
	ItemsSource = Data,
	XBindingPath = "Month", 
	High = "Value1",
	Low = "Value2" 
};
chart.Series.Add(rangeColumnSeries);

{% endhighlight %}

{% endtabs %}

Following properties are used to customize the range column segment appearance,

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries~Spacing.html) - used to change the spacing between two segments. The default value of spacing is 0, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available space, respectively.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries~Width.html) - used to change the width of the rectangle. The default value of the width is 0.8, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available width, respectively. 

![RangeColumn chart type in Xamarin.Forms](charttypes_images/charttypes_img7.png)

## Stacked Column Chart

To render a stacked column chart, create an instance of [`StackingColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the stacked column segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~DataMarkerPosition.html) - used to position the data marker at [`Bottom`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html), [`Top`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html) and [`Center`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html) of the rectangle. 
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~Spacing.html) - used to change the spacing between two segments. The default value of spacing is 0, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available space, respectively.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~Width.html) - used to change the width of the rectangle. The default value of the width is 0.8, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available width, respectively. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:StackingColumnSeries ItemsSource ="{Binding Data1}" XBindingPath="Month" 
								YBindingPath="Value"/>

	<chart:StackingColumnSeries ItemsSource ="{Binding Data2}" XBindingPath="Month" 
								YBindingPath="Value"/>

	<chart:StackingColumnSeries ItemsSource ="{Binding Data3}" XBindingPath="Month" 
								YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StackingColumnSeries stackingColumnSeries1 = new StackingColumnSeries() 
{ 
	ItemsSource = Data1, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};

StackingColumnSeries stackingColumnSeries2 = new StackingColumnSeries() 
{ 
	ItemsSource = Data2, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};

StackingColumnSeries stackingColumnSeries3 = new StackingColumnSeries() 
{ 
	ItemsSource = Data3, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};

chart.Series.Add(stackingColumnSeries1);
chart.Series.Add(stackingColumnSeries2);
chart.Series.Add(stackingColumnSeries3);

{% endhighlight %}

{% endtabs %}

![StackingColumn chart type in Xamarin.Forms](charttypes_images/charttypes_img8.png)

## 100% Stacked Column Chart

To render a 100% stacked column chart, create an instance of [`StackingColumn100Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumn100Series.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the series appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~DataMarkerPosition.html) - used to position the data marker at [`Bottom`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html), [`Top`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html) and [`Center`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerPosition.html) of the rectangle. 
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~Spacing.html) -  used to change the spacing between two segments. The default value of spacing is 0, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available space, respectively.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries~Width.html) - used to change the width of the rectangle. The default value of the width is 0.8, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available width, respectively. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:StackingColumn100Series ItemsSource ="{Binding Data1}" XBindingPath="Year" 
								   YBindingPath="Value"/>

	<chart:StackingColumn100Series ItemsSource ="{Binding Data2}" XBindingPath="Year" 
								   YBindingPath="Value"/>

	<chart:StackingColumn100Series ItemsSource ="{Binding Data3}" XBindingPath="Year" 
								   YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StackingColumn100Series stackingColumn100Series1 = new StackingColumn100Series() 
{ 
	ItemsSource = Data1, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingColumn100Series stackingColumn100Series2 = new StackingColumn100Series() 
{ 
	ItemsSource = Data2, 
	XBindingPath = "Year", 
	YBindingPath = "Value"  
};

StackingColumn100Series stackingColumn100Series3 = new StackingColumn100Series() 
{ 
	ItemsSource = Data3, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

chart.Series.Add(stackingColumn100Series1);
chart.Series.Add(stackingColumn100Series2);
chart.Series.Add(stackingColumn100Series3);

{% endhighlight %}

{% endtabs %}

![StackingColumn100 chart type in Xamarin.Forms Chart](charttypes_images/charttypes_img9.png)

## Bar Chart

To render a bar chart, create an instance of [`BarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the bar segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries~DataMarkerPosition.html) - used to position the data marker at left, right and center of the rectangle. 
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries~Spacing.html) - used to change the spacing between two segments. The default value of spacing is 0, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available space, respectively.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries~Width.html) - used to change the width of the rectangle. The default value of the width is 0.8, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available width, respectively. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:BarSeries ItemsSource ="{Binding Data}" XBindingPath="Year"
					 YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

BarSeries barSeries = new BarSeries () 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};
chart.Series.Add(barSeries);

{% endhighlight %}

{% endtabs %}

![Bar chart type in Xamarin.Forms](charttypes_images/charttypes_img10.png)

## Stacked Bar Chart

To render a stacked bar chart, create an instance of [`StackingBarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the stacked bar segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~DataMarkerPosition.html) - used to position the data marker at left, right and center of the rectangle.
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~Spacing.html) - used to change the spacing between two segments.The default value of spacing is 0 and the value ranges from 0 to 1. Here 1 and 0 corresponds to 100% and 0% of available space respectively. 
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~Width.html) - used to change the width of the rectangle. The default value of width is 0.8 and the value ranges from 0 to 1. Here 1 and 0 corresponds to 100% and 0% of available width respectively. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:StackingBarSeries ItemsSource ="{Binding Data1}" XBindingPath="Month" 
							 YBindingPath="Value"/>

	<chart:StackingBarSeries ItemsSource ="{Binding Data2}" XBindingPath="Month" 
 							 YBindingPath="Value"/>

	<chart:StackingBarSeries ItemsSource ="{Binding Data3}" XBindingPath="Month" 
							 YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StackingBarSeries stackingBarSeries1 = new StackingBarSeries() 
{ 
	ItemsSource = Data1, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};

StackingBarSeries stackingBarSeries2 = new StackingBarSeries() 
{ 
	ItemsSource = Data2, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};

StackingBarSeries stackingBarSeries3 = new StackingBarSeries() 
{ 
	ItemsSource = Data3, 
	XBindingPath = "Month", 
	YBindingPath = "Value" 
};

chart.Series.Add(stackingBarSeries1);
chart.Series.Add(stackingBarSeries2);
chart.Series.Add(stackingBarSeries3);

{% endhighlight %}

{% endtabs %}

![StackingBar chart type in Xamarin.Forms](charttypes_images/charttypes_img11.png)

## 100% Stacked Bar Chart

To render a 100% stacked bar chart, create an instance of [`StackingBar100Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBar100Series.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the series appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.
* [`CornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~CornerRadius.html) - used to add the rounded corners to the rectangle. The [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopLeft.html), [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~TopRight.html), [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomLeft.html) and [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius~BottomRight.html) of [`ChartCornerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartCornerRadius.html) properties are used to set the radius value for each corner.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~DataMarkerPosition.html) - used to position the data marker at left, right and center of the rectangle.
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~Spacing.html) - used to change the spacing between two segments.The default value of spacing is 0 and the value ranges from 0 to 1. Here 1 and 0 corresponds to 100% and 0% of available space respectively.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries~Width.html) - used to change the width of the rectangle. The default value of width is 0.8 and the value ranges from 0 to 1. Here 1 and 0 corresponds to 100% and 0% of available width respectively. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:StackingBar100Series ItemsSource ="{Binding Data1}" XBindingPath="Year" 
								YBindingPath="Value"/>

	<chart:StackingBar100Series ItemsSource ="{Binding Data2}" XBindingPath="Year" 
								YBindingPath="Value"/>

	<chart:StackingBar100Series ItemsSource ="{Binding Data3}" XBindingPath="Year" 
								YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StackingBar100Series stackingBar100Series1 = new StackingBar100Series() 
{ 
	ItemsSource = Data1, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingBar100Series stackingBar100Series2 = new StackingBar100Series() 
{ 
	ItemsSource = Data2, 
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};

StackingBar100Series stackingBar100Series3 = new StackingBar100Series() 
{ 
	ItemsSource = Data3, 
	XBindingPath = "Year", 
	YBindingPath = "Value"  
};

chart.Series.Add(stackingBar100Series1);
chart.Series.Add(stackingBar100Series2);
chart.Series.Add(stackingBar100Series3);

{% endhighlight %}

{% endtabs %}

![StackingBar100 chart type in Xamarin.Forms](charttypes_images/charttypes_img12.png)

## Spline Chart

To render a spline chart, create an instance of [`SplineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the spline segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:SplineSeries ItemsSource ="{Binding Data}" XBindingPath="Month"
	  					YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

SplineSeries splineSeries = new SplineSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Month", 
	YBindingPath = "Value"  
};
chart.Series.Add(splineSeries);

{% endhighlight %}

{% endtabs %}

![Spline chart type in Xamarin.Forms](charttypes_images/charttypes_img13.png)

### SplineSeries Types

[`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineSeries~SplineType.html) allows you to change the spline curve in series. 
The following types are used in [`SplineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineSeries.html) as 

 * Natural
 * Monotonic
 * Cardinal
 * Clamped

By default [`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html) value is [`Natural`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html).

The following code shows how to set the [`SplineType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html) value as [`Cardinal`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)

{% tabs %}

{% highlight xaml%}

<chart:SfChart>
...

	<chart:SplineSeries ItemsSource ="{Binding Data}" XBindingPath="Month"
	  					YBindingPath="Value" SplineType="Cardinal" />

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

SplineSeries splineSeries = new SplineSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Month", 
	YBindingPath = "Value",
	SplineType = SplineType.Cardinal
};
chart.Series.Add(splineSeries);

{% endhighlight %}

{% endtabs %}

[`Cardinal`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html) 

![SplineType support in Xamarin.Forms Chart](charttypes_images/CardinalSplineType.png)

[`Monotonic`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)

![SplineType support in Xamarin.Forms Chart](charttypes_images/MonotonicSplineType.png)

[`Clamped`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineType.html)

![SplineType support in Xamarin.Forms Chart](charttypes_images/ClampedSplineType.png)

## Step Line Chart

To render a step line chart, create an instance of [`StepLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StepLineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of
[`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the spline segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart.Series>

	<chart:StepLineSeries ItemsSource="{Binding Data}" XBindingPath="Month"
	   					  YBindingPath="Value" />
	
</chart:SfChart.Series>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

StepLineSeries stepLine = new StepLineSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Month", 
	YBindingPath = "Value"
};
chart.Series.Add(stepLine);

{% endhighlight %}

{% endtabs %}

![StepLine chart type in Xamarin.Forms](charttypes_images/stepline.png)

## Bubble Chart

To render a bubble chart, create an instance of [`BubbleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). 

Bubble chart requires 3 fields (X, Y and Size) to plot a point. Here [`Size`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~Size.html) is used to specify the size of each bubble segment. 

There are two ways you can provide data to bubble chart,

1.You can use [ChartDataPoint's](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html#) three parameter constructor to pass [`XValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~XValue.html), [`YValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~YValue.html) and [`Size`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Size.html) values to  [`BubbleSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries.html),

{% highlight c# %}
[C#]

SfChart chart = new SfChart();
...

ObservableCollection<ChartDataPoint> data = new ObservableCollection<ChartDataPoint>()
{    
	new ChartDataPoint(64, 14.4, 20),
	new ChartDataPoint(71, 2, 15),
	new ChartDataPoint(74, 7, 30),
	new ChartDataPoint(80, 4, 22),
	new ChartDataPoint(82, 10.3, 28),
	new ChartDataPoint(94, 1, 8),
	new ChartDataPoint(96, 6, 18),
	new ChartDataPoint(98, 12.3, 28),                       
};
   
BubbleSeries bubbleSeries = new BubbleSeries() 
{ 
	ItemsSource = data 
};

chart.Series.Add(bubbleSeries);

{% endhighlight %}


2.Or else you can use [`YBindingPath`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.XyDataSeries~YBindingPath.html) and [`Size`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~Size.html) properties of [`BubbleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries.html) to map the Y value and size from custom object to chart. 

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:BubbleSeries ItemsSource ="{Binding Data}"
						XBindingPath="XValue"
						YBindingPath="YValue" 
						Size="Size"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

BubbleSeries bubbleSeries = new BubbleSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "XValue", 
	YBindingPath = "YValue", 
	Size = "Size” 
};
chart.Series.Add(bubbleSeries);

{% endhighlight %}

{% endtabs %}

Following properties are used to customize the bubble segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`MinimumRadius`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~MinimumRadius.html) – used to change the minimum size of the series.
* [`MaximumRadius`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~MaximumRadius.html) – used to change the maximum size of the series.

![Bubble chart type in Xamarin.Forms](charttypes_images/charttypes_img16.png)

## Scatter Chart	

To render a scatter chart, create an instance of [`ScatterSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the scatter segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`ScatterWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~ScatterWidth.html) – used to change the width of the series.
* [`ScatterHeight`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~ScatterHeight.html) – used to change the height of the series.
* [`ShapeType`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~ShapeType.html) - used to change the rendering shape of scatter series. The available shapes are [`Cross`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`Diamond`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`Ellipse`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`Hexagon`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`InvertedTriangle`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`Pentagon`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`Plus`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html), [`Rectangle`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html) and [`Triangle`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScatterShapeType.html).

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:ScatterSeries ScatterHeight="15"
	ScatterWidth="15"
	ShapeType="Ellipse"
	ItemsSource ="{Binding Data}" 
	XBindingPath="Year"
	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

ScatterSeries scatterSeries = new ScatterSeries ()
{ 
	ItemsSource = Data, 	
	ScatterHeight = 15, 
	ScatterWidth = 15, 
	ShapeType = ChartScatterShapeType.Ellipse,
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};
chart.Series.Add(scatterSeries);

{% endhighlight %}

{% endtabs %}

![Scatter chart type in Xamarin.Forms](charttypes_images/charttypes_img17.png)

## OHLC Chart

To render an OHLC chart, create an instance of [`HiLoOpenCloseSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

OHLC chart requires five values (X, Open, High, Low and Close) to plot a point. 

There are two ways you can provide data to an OHLC chart,

1.You can use [`ChartDataPoint's`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor(IComparable,Double,Double,Double,Double).html#) five parameter constructor to pass [`XValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~XValue.html), [`Open`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Open.html), [`High`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~High.html), [`Low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Low.html), [`Close`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Close.html) , [`Volume`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Volume.html) values to [`HiLoOpenCloseSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries.html) and [`technical indicators`](https://help.syncfusion.com/xamarin/sfchart/technicalindicators#accumulation-distribution-indicator).

{% highlight c# %}
[C#]

SfChart chart = new SfChart();
...

ObservableCollection<ChartDataPoint> data = new ObservableCollection<ChartDataPoint>()
{
	new ChartDataPoint("2010", 873.8, 878.85, 855.5, 860.5),
	new ChartDataPoint("2011", 861, 868.4, 835.2, 843.45),
	new ChartDataPoint("2012", 846.15, 853, 838.5, 847.5),
	new ChartDataPoint("2013", 846, 860.75, 841, 855),
	new ChartDataPoint("2014", 841, 845, 827.85, 838.65)
};
	
HiLoOpenCloseSeries hiLoOpenCloseSeries = new HiLoOpenCloseSeries() 
{ 
	ItemsSource = data
};
	
chart.Series.Add(hiLoOpenCloseSeries);

{% endhighlight %}

2.Or else you can use [`Open`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Open.html),[`High`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~High.html),[`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Low.html) and [`Close`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Close.html) properties of [`HiLoOpenCloseSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries.html) to map Open, High, Low and Close values from custom object to chart.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:HiLoOpenCloseSeries ItemsSource ="{Binding Data}" XBindingPath="Year" 
				High="Value1" Low="Value2"
				Open="Value3" Close="Value4"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

HiLoOpenCloseSeries hiLoOpenCloseSeries = new HiLoOpenCloseSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	Open = "Value1", 
	High = "Value2", 
	Low = "Value3", 
	Close = "Value4" 
};
chart.Series.Add(hiLoOpenCloseSeries);

{% endhighlight %}

{% endtabs %}

You can use the following properties to customize the [`HiLoOpenCloseSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries.html) segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`Spacing`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries~Spacing.html) - used to change the spacing between two segments.
* [`Width`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries~Width.html) - used to change the width of the rectangle.

![HiLoOpenClose chart type in Xamarin.Forms](charttypes_images/charttypes_img18.png)

### Bull and Bear Color	

In OHLC chart, [`BullFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BullFillColor.html) property is used to specify a fill color for the segments that indicates an increase in stock price in the measured time interval and [`BearFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BearFillColor.html) property is used to specify a fill color for the segments that indicates a decrease in stock price in the measured time interval.

{% tabs %} 

{% highlight xaml %}

<chart:HiLoOpenCloseSeries BearFillColor="Blue" 
			BullFillColor="Purple"
			ItemsSource ="{Binding Data}" 
			XBindingPath="Year" 
			High="Value1" 
			Low="Value2" 
			Open="Value3" 
			Close="Value4"/>

{% endhighlight %}

{% highlight c# %}

HiLoOpenCloseSeries hiLoOpenCloseSeries = new HiLoOpenCloseSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	Open = "Value1", 
	High = "Value2", 
	Low = "Value3", 
	Close = "Value4",
	BearFillColor = Color.Blue,
	BullFillColor = Color.Purple
};

{% endhighlight %}

{% endtabs %}

![Bull and bear Color support for financial series in Xamarin.Forms Chart](charttypes_images/charttypes_img19.png)

## Candle Chart

To render a candle chart, create an instance of [`CandleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Candle chart requires five values (X, Open, High, Low and Close) to plot a point. 

There are two ways you can provide data to an candle chart,

1.You can use [ChartDataPoint's](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor(IComparable,Double,Double,Double,Double).html#) five parameter constructor to pass [`XValue`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~XValue.html), [`Open`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Open.html), [`High`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~High.html), [`Low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~Low.html) and close values to  [`CandleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries.html),

{% highlight c# %}
[C#]

SfChart chart = new SfChart();
...

ObservableCollection<ChartDataPoint> data = new ObservableCollection<ChartDataPoint>()
{
	new ChartDataPoint("2010", 873.8, 878.85, 855.5, 860.5),
	new ChartDataPoint("2011", 861, 868.4, 835.2, 843.45),
	new ChartDataPoint("2012", 846.15, 853, 838.5, 847.5),
	new ChartDataPoint("2013", 846, 860.75, 841, 855),
	new ChartDataPoint("2014", 841, 845, 827.85, 838.65)
};

CandleSeries candleSeries = new CandleSeries () 
{ 
	ItemsSource = data
};

chart.Series.Add(candleSeries);

{% endhighlight %}

2.Or else you can use [`Open`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Open.html),[`High`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~High.html),[`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Low.html) and [`Close`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Close.html) property of [`CandleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries.html) to map Open, High, Low and Close values from custom object to chart.

{% tabs %} 

{% highlight xaml %}  

<chart:SfChart>
...

	<chart:CandleSeries ItemsSource ="{Binding Data}"
	XBindingPath="Year" 
	High="Value1"
	Low="Value2"
	Open="Value3"
	Close="Value4"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %} 

SfChart chart = new SfChart();
...

CandleSeries candleSeries = new CandleSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	Open = "Value1", 
	High = "Value2", 
	Low = "Value3", 
	Close = "Value4"
};
chart.Series.Add(candleSeries);

{% endhighlight %}

{% endtabs %}
   
You can use the following properties to customize the candle segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries~StrokeColor.html) – used to change the stroke color of the series.

![Candle chart type in Xamarin.Forms](charttypes_images/charttypes_img20.png)

### Bull and Bear Color

In Candle chart, [`BullFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BullFillColor.html) property is used to specify a fill color for the segments that indicates an increase in stock price in the measured time interval and [`BearFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BearFillColor.html) property is used to specify a fill color for the segments that indicates a decrease in stock price in the measured time interval.

{% tabs %} 

{% highlight xaml %}

<chart:CandleSeries BearFillColor="Blue"
	BullFillColor="Purple"
	ItemsSource ="{Binding Data}" 
	XBindingPath="Year"
	High="Value1"
	Low="Value2"
	Open="Value3"
	Close="Value4" />

{% endhighlight %}

{% highlight c# %}

CandleSeries candleSeries = new CandleSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	Open = "Value1", 
	High = "Value2", 
	Low = "Value3", 
	Close = "Value4",
	BearFillColor = Color.Blue,
	BullFillColor = Color.Purple
};

{% endhighlight %}

{% endtabs %}

![Bull and bear Color support for financial series in Xamarin.Forms Chart](charttypes_images/charttypes_img21.png)

### EnableSolidCandles

In Candle Series, [`EnableSolidCandles`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries~EnableSolidCandles.html) property is used to specify whether the candle segment should be filled or hollow. The default value of this property is false.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
    ...
    <chart:SfChart.Series>

        <chart:CandleSeries ItemsSource="{Binding FinancialData}" EnableSolidCandles="True"/>

    </chart:SfChart.Series>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart()

{
     ...
     Series =
     {
         new CandleSeries()
         {
               ItemsSource = viewModel.FinancialData,
   
               EnableSolidCandles = true,
         }
     }
};

{% endhighlight %}

{% endtabs %}

## Radar Chart

To render a radar chart, create an instance of [`RadarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RadarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).  

### Draw type

[`DrawType`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~DrawType.html) property is used to specify the radar series rendering type. Following are the two options you can set to this property,

* [`Line`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using line series.
* [`Area`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using area series.

{% tabs %}
{% highlight xaml %}
<chart:RadarSeries ItemsSource="{Binding RadarData}" DrawType="Line"
          XBindingPath="Name" YBindingPath="Value"  />

{% endhighlight %}
{% highlight c# %}
RadarSeries radar = new RadarSeries ();
radar.ItemsSource = viewModel.RadarData;
radar.XBindingPath = "Name";
radar.YBindingPath = "Value";
radar.DrawType = PolarRadarSeriesDrawType.Line;

{% endhighlight %}
{% endtabs %}

![Draw type support for radar series in Xamarin.Forms Chart](ChartTypes_images/Radar.png)

### Customize the appearance

You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~StrokeColor.html) – used to change the stroke color of the series when draw types is set to `Area`
* [`StrokeDashArray`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~StrokeDashArray.html) – used to render lines with dashes when the draw type is set to `Line`.

{% tabs %}
{% highlight xaml %}
<chart:RadarSeries ItemsSource="{Binding RadarData}" Color="Aqua" StrokeColor="Blue" 
StrokeWidth="3" XBindingPath="Name" YBindingPath="Value"  />

{% endhighlight %}
{% highlight c# %}
RadarSeries radar = new RadarSeries ();
radar.ItemsSource = viewModel.RadarData;
radar.XBindingPath = "Name";
radar.YBindingPath = "Value";
radar.Color = Color.Aqua;
radar.StrokeColor = Color.Blue;
radar.StrokeWidth = 3;

{% endhighlight %}
{% endtabs %}

![Customizing the appearance of radar series in Xamarin.Forms Chart](ChartTypes_images/RadarCustomization.png)

### Closed

[`Closed`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~IsClosed.html) property is used to determine, whether to connect the first and last data point of the series. By default, the property is set to `true`.

{% tabs %}
{% highlight xaml %}
<chart:RadarSeries ItemsSource="{Binding RadarData}" IsClosed="false"
         XBindingPath="Name" YBindingPath="Value"  />

{% endhighlight %}
{% highlight c# %}
RadarSeries radar = new RadarSeries ();
radar.ItemsSource = viewModel.RadarData;
radar.XBindingPath = "Name";
radar.YBindingPath = "Value";
radar.IsClosed = false;

{% endhighlight %}
{% endtabs %}

![Closed radar series in Xamarin.Forms Chart](ChartTypes_images/RadarClosed.png)

### Radar start angle for primary axis

The start position of the radar series can be set by using [`PolarAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartAxis~PolarAngle.html) property of axis. Default value of [`PolarAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartAxis~PolarAngle.html) property is [`Rotate270`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartPolarAngle.html). [`PolarAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartAxis~PolarAngle.html) property can be set for primary axis, secondary axis, or both axes

{% tabs %}

{% highlight xaml %}

<chart:SfChart.PrimaryAxis>

    <chart:CategoryAxis PolarAngle = “Rotate0”/>

</chart:SfChart.PrimaryAxis >
 
<chart:SfChart.SecondaryAxis>

    <chart:NumericalAxis/>

</chart:SfChart.SecondaryAxis >
 
{% endhighlight %}

{% highlight c# %}

chart.PrimaryAxis  = new CategoryAxis(){ PolarAngle = ChartPolarAngle.Rotate0 };

chart.SecondaryAxis =  new NumericalAxis(); 

{% endhighlight %}

{% endtabs %}

![Radar start angle support for primary axis in Xamarin.Forms Chart](charttypes_images/radarangle_img1.png)

### Radar start angle for secondary axis

{% tabs %}

{% highlight xaml %}

<chart:SfChart.PrimaryAxis>

    <chart:CategoryAxis/>

</chart:SfChart.PrimaryAxis>

<chart:SfChart.SecondaryAxis>

    <chart:NumericalAxis  PolarAngle="Rotate0"/>

</chart:SfChart.SecondaryAxis>
 
{% endhighlight %}

{% highlight c# %}

chart.PrimaryAxis  = new CategoryAxis();

chart.SecondaryAxis =  new NumericalAxis() { PolarAngle = ChartPolarAngle.Rotate0 }; 

{% endhighlight %}

{% endtabs %}

![Radar start angle support for secondary axis in Xamarin.Forms Chart](charttypes_images/radarangle_img2.png)

### Radar start angle for both axis

{% tabs %}

{% highlight xaml %}

<chart:SfChart.PrimaryAxis>

    <chart:CategoryAxis PolarAngle = “Rotate0” />

</chart:SfChart.PrimaryAxis>
 
<chart:SfChart.SecondaryAxis>

    <chart:NumericalAxis  PolarAngle = “Rotate0” />

</chart:SfChart.SecondaryAxis >
 
{% endhighlight %}

{% highlight c# %}

chart.PrimaryAxis  = new CategoryAxis(){ PolarAngle = ChartPolarAngle.Rotate0 };

chart.SecondaryAxis =  new NumericalAxis() { PolarAngle = ChartPolarAngle.Rotate0 }; 

{% endhighlight %}

{% endtabs %}
![Radar start angle support for both axes in Xamarin.Forms Chart](charttypes_images/radarangle_img3.png)

## Polar Chart

To render a polar chart, create an instance of [`PolarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). 
 

### Draw type

[`DrawType`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~DrawType.html) property is used to specify the polar series rendering type. Following are the two options you can set to this property,

* [`Line`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using line series.
* [`Area`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using area series.

{% tabs %}
{% highlight xaml %}
<chart:PolarSeries ItemsSource="{Binding PolarData}" DrawType="Line" 
XBindingPath="Name" YBindingPath="Value"  />

{% endhighlight %}
{% highlight c# %}
PolarSeries polar = new PolarSeries ();
polar.ItemsSource = viewModel.PolarData;
polar.XBindingPath = "Name";
polar.YBindingPath = "Value";
polar.DrawType = PolarRadarSeriesDrawType.Line;

{% endhighlight %}
{% endtabs %}

![Draw type support for polar series in Xamarin.Forms Chart](ChartTypes_images/Polar.png)

### Customize the appearance

You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~StrokeColor.html) – used to change the stroke color of the series when draw types is set to [`Area`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html)
* [`StrokeDashArray`](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~StrokeDashArray.html) – used to render lines with dashes when the draw type is set to [`Line`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html)

{% tabs %}
{% highlight xaml %}
<chart:PolarSeries ItemsSource="{Binding PolarData}" StrokeColor="Blue" Color="Aqua" 
StrokeWidth="3" XBindingPath="Name" YBindingPath="Value"  />

{% endhighlight %}
{% highlight c# %}
PolarSeries polar = new PolarSeries ();
polar.ItemsSource = viewModel.PolarData;
polar.XBindingPath = "Name";
polar.YBindingPath = "Value";
polar.Color = Color.Aqua;
polar.StrokeColor = Color.Blue;
polar.StrokeWidth = 3;

{% endhighlight %}
{% endtabs %}

![Customizing the appearance of polar series in Xamarin.Forms Chart](ChartTypes_images/PolarCustomization.png)

### Closed

[`Closed`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~IsClosed.html) property is used to determine, whether to connect the first and last data point of the series. By default, the property is set to `true`.

{% tabs %}
{% highlight xaml %}
<chart:PolarSeries ItemsSource="{Binding PolarData}" IsClosed="false"
         XBindingPath="Name" YBindingPath="Value"  />

{% endhighlight %}
{% highlight c# %}
PolarSeries polar = new PolarSeries ();
polar.ItemsSource = viewModel.PolarData;
polar.XBindingPath = "Name";
polar.YBindingPath = "Value";
polar.IsClosed = false;

{% endhighlight %}
{% endtabs %}

![Closed polar series in Xamarin.Forms Chart](ChartTypes_images/PolarClosed.png)

### Polar start angle for primary axis

The start position of the polar series can be set by using [`PolarAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartAxis~PolarAngle.html) property of axis. Default value of [`PolarAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartAxis~PolarAngle.html) property is [`Rotate270`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartPolarAngle.html). [`PolarAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartAxis~PolarAngle.html) property can be set for primary axis, secondary axis, or both axes.

{% tabs %}

{% highlight xaml %}

<chart:SfChart.PrimaryAxis>

    <chart:CategoryAxis PolarAngle = “Rotate0”/>

</chart:SfChart.PrimaryAxis >
 
<chart:SfChart.SecondaryAxis>

    <chart:NumericalAxis/>

</chart:SfChart.SecondaryAxis >
 
{% endhighlight %}

{% highlight c# %}

chart.PrimaryAxis  = new CategoryAxis(){ PolarAngle = ChartPolarAngle.Rotate0 };

chart.SecondaryAxis =  new NumericalAxis(); 

{% endhighlight %}

{% endtabs %}

![Polar start angle support for primary axis in Xamarin.Forms Chart](charttypes_images/polarangle_img1.png)

### Polar start angle for secondary axis

{% tabs %}

{% highlight xaml %}

<chart:SfChart.PrimaryAxis>

    <chart:CategoryAxis/>

</chart:SfChart.PrimaryAxis>

<chart:SfChart.SecondaryAxis>

    <chart:NumericalAxis PolarAngle="Rotate0"/>

</chart:SfChart.SecondaryAxis>
 
{% endhighlight %}

{% highlight c# %}

chart.PrimaryAxis  = new CategoryAxis();

chart.SecondaryAxis =  new NumericalAxis() { PolarAngle = ChartPolarAngle.Rotate0 }; 

{% endhighlight %}

{% endtabs %}

![Polar start angle support for secondary axis in Xamarin.Forms Chart](charttypes_images/polarangle_img2.png)

### Polar start angle for both axis

{% tabs %}

{% highlight xaml %}

<chart:SfChart.PrimaryAxis>

    <chart:CategoryAxis PolarAngle = “Rotate0” />

</chart:SfChart.PrimaryAxis >
 
<chart:SfChart.SecondaryAxis>

    <chart:NumericalAxis  PolarAngle = “Rotate0” />

</chart:SfChart.SecondaryAxis >
 
{% endhighlight %}

{% highlight c# %}

chart.PrimaryAxis  = new CategoryAxis(){ PolarAngle = ChartPolarAngle.Rotate0 };

chart.SecondaryAxis =  new NumericalAxis() { PolarAngle = ChartPolarAngle.Rotate0 }; 

{% endhighlight %}

{% endtabs %}

![Polar start angle support for both axes in Xamarin.Forms Chart](charttypes_images/polarangle_img3.png)

## Pie Chart

To render a pie chart, create an instance of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the pie segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~DataMarkerPosition.html) - used to change the position of data marker at [`Inside`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeriesDataMarkerPosition.html), [`Outside`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeriesDataMarkerPosition.html) or [`OutsideExtended`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeriesDataMarkerPosition.html).

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:PieSeries ItemsSource ="{Binding Data}" XBindingPath="Expense"
	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

PieSeries pieSeries = new PieSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value" 
};
chart.Series.Add(pieSeries);

{% endhighlight %}

{% endtabs %}

![Pie chart type in Xamarin.Forms](charttypes_images/charttypes_img22.png)

### Changing the pie size

You can use [`CircularCoefficient`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~CircularCoefficient.html) property to change the diameter of the pie chart with respect to the plot area. It ranges from 0 to 1 and the default value is `0.8`.

{% tabs %} 

{% highlight xaml %}

<chart:PieSeries CircularCoefficient="0.5"
ItemsSource ="{Binding Data}"
XBindingPath="Expense" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

PieSeries pieSeries = new PieSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	CircularCoefficient = 0.5
};

{% endhighlight %}

{% endtabs %}

![Changing the pie size in Xamarin.Forms Chart](charttypes_images/charttypes_img23.png)

### Exploding a pie segment

You can explode a pie segment using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property and specify the explode radius using [`ExplodeRadius`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~ExplodeRadius.html) property of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html).

{% tabs %} 

{% highlight xaml %}

<chart:PieSeries ExplodeIndex="1"
ItemsSource ="{Binding Data}"
XBindingPath="Expense" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

PieSeries pieSeries = new PieSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	ExplodeIndex = 1
};

{% endhighlight %}

{% endtabs %}

Also, the segments can be exploded by touch using [`ExplodeOnTouch`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeOnTouch.html) property of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html). Default value of this property is false.

![Exploding a pie segment support in Xamarin.Forms Chart](charttypes_images/charttypes_img24.png)

### Exploding all the segments

Using [`ExplodeAll`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeAll.html) property of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html), you can explode all the pie segments.

{% tabs %} 

{% highlight xaml %}

<chart:PieSeries ExplodeAll="True" ItemsSource ="{Binding Data}" XBindingPath="Expense" 
				 YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

PieSeries pieSeries = new PieSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	ExplodeAll = true	
};

{% endhighlight %}

{% endtabs %}

![Exploding all the segments of pie series in Xamarin.Forms Chart](charttypes_images/charttypes_img25.png)

### Sector of Pie

SfChart allows you to render all the data points/segments in semi-pie, quarter-pie or in any sector using [`StartAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~StartAngle.html) and [`EndAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~EndAngle.html) properties.

{% tabs %} 

{% highlight xaml %}

<chart:PieSeries StartAngle="180"
EndAngle="360"
ItemsSource ="{Binding Data}"
XBindingPath="Expense" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

PieSeries pieSeries = new PieSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	StartAngle = 180,
	EndAngle = 360
};

{% endhighlight %}

{% endtabs %}

![Sector support for pie series in Xamarin.Forms Chart](charttypes_images/charttypes_img26.png)

### Group small data points into “others”

The small segments in the pie chart can be grouped into “others” category using the [`GroupTo`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupTo.html) and [`GroupMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupMode.html) properties of PieSeries. The [`GroupMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupMode.html) property is used to specify the grouping type based on slice [`Angle`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieGroupMode.html), actual data point value, or [`Percentage`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieGroupMode.html), and the [`GroupTo`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupTo.html) property is used to set the limit to group data points into a single slice. The grouped segment is labeled as “Others” in legend and toggled as any other segment. The default value of the [`GroupTo`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupTo.html) property is [`double.NAN`], and [`GroupMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupMode.html) property is Value.

## Doughnut Chart

To render a doughnut chart, create an instance of [`DoughnutSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the doughnut segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`DataMarkerPosition`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~DataMarkerPosition.html) - used to change the position of data marker at [`Inside`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeriesDataMarkerPosition.html), [`Outside`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeriesDataMarkerPosition.html) or [`OutsideExtended`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeriesDataMarkerPosition.html).

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:DoughnutSeries ItemsSource ="{Binding Data}"
	XBindingPath="Expense"
	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value" 
};
chart.Series.Add(doughnutSeries);

{% endhighlight %}

{% endtabs %}

![Doughnut chart type in Xamarin.Forms](charttypes_images/charttypes_img27.png)

### Stacked doughnut

Doughnut segments can be separated as individual circles using the [`IsStackedDoughnut`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~IsStackedDoughnut.html) property. The following properties are used to customize the stacked doughnut chart:

* [`CapStyle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~CapStyle.html) - Specifies the shape of the start and end points of the circular segment. The supported values are `BothFlat`, `BothCurve`, `StartCurve`, and `EndCurve`. The default value of the this property is [`BothFlat`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutCapStyle.html).
* [`Spacing`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~Spacing.html) - Changes the spacing between two individual segments. The default value of spacing is 0, and the value ranges from 0 to 1. Here, 1 and 0 correspond to 100% and 0% of the available space, respectively.
* [`MaximumValue`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~MaximumValue.html) - Represents the entire span of an individual circle. The default value of the this property is `double.NaN`.
* [`TrackColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~TrackColor.html) - Changes the color of the track area.
* [`TrackBorderColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~TrackBorderColor.html) - Changes the color of the track border.
* [`TrackBorderWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~TrackBorderWidth.html) - Changes the width of the track border.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

    <chart:DoughnutSeries ItemsSource ="{Binding Data}"
    XBindingPath="Expense"
    YBindingPath="Value"
    IsStackedDoughnut="true"
    CapStyle="BothCurve"
    Spacing=”0.4”
    MaximumValue=“100” />

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
    ItemsSource = Data, 
    XBindingPath = "Expense", 
    YBindingPath = "Value",
    IsStackedDoughnut = true,
    CapStyle = DoughnutCapStyle.BothCurve,
    Spacing = 0.4,
    MaximumValue = 100 
};
chart.Series.Add(doughnutSeries);

{% endhighlight %}

{% endtabs %}

![Stacked doughnut support for doughnut series in Xamarin.Forms Chart](charttypes_images/stacked_doughnut.png)

### Changing Doughnut inner radius

You can change the doughnut chart inner radius using [`DoughnutCoefficient`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~DoughnutCoefficient.html) with respect to the plot area. It ranges from 0 to 1 and the default value is `0.4`.

{% tabs %} 

{% highlight xaml %}

<chart:DoughnutSeries DoughnutCoefficient="0.6"
ItemsSource ="{Binding Data}"
XBindingPath="Expense" 
YBindingPath="Value" />

{% endhighlight %}

{% highlight c# %}

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value", 
	DoughnutCoefficient = 0.6 
};

{% endhighlight %}

{% endtabs %}

![DoughnutCoefficient support for doughnut series in Xamarin.Forms Chart](charttypes_images/charttypes_img28.png)

### Changing the doughnut size

You can use the [`CircularCoefficient`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~CircularCoefficient.html) property to change the diameter of the doughnut chart with respect to the plot area. It ranges from 0 to 1 and the default value is 0.8.

{% tabs %} 

{% highlight xaml %}

<chart:DoughnutSeries CircularCoefficient="0.5"
ItemsSource ="{Binding Data}"
XBindingPath="Expense" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value", 
	CircularCoefficient = 0.5 
};

{% endhighlight %}

{% endtabs %}

![CircularCoefficient support for doughnut series in Xamarin.Forms Chart](charttypes_images/charttypes_img29.png)

### Exploding a doughnut segment

Exploding a specific doughnut segment, you have to set the index to be exploded using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property of the series.

{% tabs %} 

{% highlight xaml %}

<chart:DoughnutSeries ExplodeIndex="1" ItemsSource ="{Binding Data}" XBindingPath="Expense" 
					  YBindingPath="Value" />

{% endhighlight %}

{% highlight c# %}

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	ExplodeIndex = 1
};

{% endhighlight %}

{% endtabs %}

Also, the segments can be exploded by touch using [`ExplodeOnTouch`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeOnTouch.html) property of [`DoughnutSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries.html). Default value of this property is false.

![Exploding a doughnut segment support in Xamarin.Forms Chart](charttypes_images/charttypes_img30.png)

### Exploding all the segments

To explode all the segments, you have to enable [`ExplodeAll`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeAll.html) property of the series.

{% tabs %} 

{% highlight xaml %}

<chart:DoughnutSeries ExplodeAll="True" ItemsSource ="{Binding Data}" XBindingPath="Expense" 
					  YBindingPath="Value" />

{% endhighlight %}

{% highlight c# %}

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	ExplodeAll = true
};

{% endhighlight %}

{% endtabs %}

![Exploding all the segments of doughnut series in Xamarin.Forms Chart](charttypes_images/charttypes_img31.png)

### Sector of Doughnut

[`SfChart`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html) allows you to render all the data points/segments in semi-doughnut, quarter- doughnut or in any sector using [`StartAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~StartAngle.html) and [`EndAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~EndAngle.html) properties.

{% tabs %} 

{% highlight xaml %}

<chart:DoughnutSeries StartAngle="180" EndAngle="360" ItemsSource ="{Binding Data}" 
					  XBindingPath="Expense" YBindingPath="Value" />

{% endhighlight %}

{% highlight c# %}

DoughnutSeries doughnutSeries = new DoughnutSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Expense", 
	YBindingPath = "Value",
	StartAngle = 180,
	EndAngle = 360
};

{% endhighlight %}

{% endtabs %}

![Sector support for doughnut series in Xamarin.Forms Chart](charttypes_images/charttypes_img32.png)

### Group small data points into “others”

The small segments in the doughnut chart can be grouped into “others” category using the [`GroupTo`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupTo.html) and [`GroupMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupMode.html) properties of DoughnutSeries. The [`GroupMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupMode.html) property is used to specify the grouping type based on slice angle, actual data point value, or percentage, and the [`GroupTo`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupTo.html) property is used to set the limit to group data points into a single slice. The grouped segment is labeled as “Others” in legend and toggled as any other segment. The default value of the [`GroupTo`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupTo.html) property is [`double.NAN`], and [`GroupMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~GroupMode.html) property is Value.

### Add view to the center of doughnut chart

Any view can be added to the center of doughnut chart using the [`CenterView`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~CenterView.html) property of [`DoughnutSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries.html). The binding context of the [`CenterView`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~CenterView.html) will be the respective [`DoughnutSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries.html).

{% tabs %} 

{% highlight xaml %}

<chart:DoughnutSeries>
...

	<chart:DoughnutSeries.CenterView>
		<StackLayout HorizontalOptions = "FillAndExpand" 
		             VerticalOptions = "FillAndExpand">
		...
		</StackLayout>
	</chart:DoughnutSeries.CenterView>
...
</chart:DoughnutSeries>
	
{% endhighlight %}

{% highlight C# %}

DoughnutSeries doughnutSeries = new DoughnutSeries()
{
	...
}
doughnutSeries.CenterView = new Label() { Text = "CenterView" };

{% endhighlight %}

{% endtabs %}

![CenterView support for doughnut series in Xamarin.Forms Chart](charttypes_images/charttypes_img41.png)

### InnerRadius

The [`InnerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~InnerRadius.html) property of [`DoughnutSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries.html) is used to get only the inner radius. Using this [`InnerRadius`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~InnerRadius.html) value, you can provide [`CentreView`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~CenterView.html) for series to avoid the view from being cropped outside the series.

## Pyramid Chart

To render a pyramid chart, create an instance of [`PyramidSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PyramidSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the pyramid segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:PyramidSeries ItemsSource ="{Binding Data}" XBindingPath="Country"
	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

PyramidSeries pyramidSeries = new PyramidSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Country", 
	YBindingPath = "Value" 
};
chart.Series.Add(pyramidSeries);

{% endhighlight %}

{% endtabs %}

![Pyramid chart type in Xamarin.Forms](charttypes_images/charttypes_img33.png)

### Pyramid Mode

You can render the pyramid series as linear or surface mode. In linear mode, height of the pyramid segment is based on the Y value and in surface mode, area of the pyramid segment is based on the Y values. The default value of [`PyramidMode`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PyramidSeries~PyramidMode.html) property is [`Linear`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartPyramidMode.html).

{% tabs %} 

{% highlight xaml %}

<chart:PyramidSeries ItemsSource ="{Binding Data}" PyramidMode="Surface" XBindingPath="Country" 
					 YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

PyramidSeries pyramidSeries = new PyramidSeries ()
{ 
	ItemsSource = Data, 
	XBindingPath = "Country", 
	YBindingPath = "Value",
	PyramidMode = ChartPyramidMode.Surface 
};

{% endhighlight %}

{% endtabs %}

![Pyramid mode support in Xamarin.Forms Chart](charttypes_images/charttypes_img34.png)

### Gap between the segments

You can control the gap between the two segments using [`GapRatio`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~GapRatio.html) property. Its ranges from 0 to 1.

{% tabs %} 

{% highlight xaml %}

<chart:PyramidSeries ItemsSource ="{Binding Data}" GapRatio="0.1"
XBindingPath="Country" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

PyramidSeries pyramidSeries = new PyramidSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Country", 
	YBindingPath = "Value",
	GapRatio = 0.1
};

{% endhighlight %}

{% endtabs %}

![Gap between the pyramid segments support in Xamarin.Forms Chart](charttypes_images/charttypes_img35.png)

### Exploding a pyramid segment

You can explode a pyramid segment using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property, and [`ExplodeOffset`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~ExplodeOffset.html) property is used to specify the exploded segment’s distance.

{% tabs %} 

{% highlight xaml %}

<chart:PyramidSeries ItemsSource ="{Binding Data}" ExplodeIndex="2"
XBindingPath="Country" 
YBindingPath="Value" />

{% endhighlight %}

{% highlight c# %}

PyramidSeries pyramidSeries = new PyramidSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Country", 
	YBindingPath = "Value",
	ExplodeIndex = 2
};

{% endhighlight %}

Also, the segments can be exploded by touch using [`ExplodeOnTouch`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeOnTouch.html) property of [`PyramidSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PyramidSeries.html). Default value of this property is false.

{% endtabs %}

![Exploding a pyramid segment support in Xamarin.Forms Chart](](charttypes_images/charttypes_img36.png)

## Funnel Chart

To render a funnel chart, create an instance of [`FunnelSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the funnel segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`Opacity`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Opacity.html) - used to control the transparency of the chart series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:FunnelSeries ItemsSource ="{Binding Data}" XBindingPath="Status"
	YBindingPath="Value"/>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();
...

FunnelSeries funnelSeries = new FunnelSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Status", 
	YBindingPath = "Value" 
};
chart.Series.Add(funnelSeries);

{% endhighlight %}

{% endtabs %}

![Funnel chart type in Xamarin.Forms](charttypes_images/charttypes_img37.png)

### Gap between the segments

You can control the gap between the two segments using [`GapRatio`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~GapRatio.html) property. Its ranges from 0 to 1.

{% tabs %} 

{% highlight xaml %}

<chart:FunnelSeries ItemsSource ="{Binding Data}" GapRatio="0.1"
XBindingPath="Year" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

FunnelSeries funnelSeries = new FunnelSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	YBindingPath = "Value",
	GapRatio = 0.1
};

{% endhighlight %}

{% endtabs %}

![Gap between the funnel segments support in Xamarin.Forms Chart](charttypes_images/charttypes_img38.png)

### Exploding a funnel segment

You can explode a pyramid segment using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property and [`ExplodeOffset`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~ExplodeOffset.html) property is used to specify the exploded segment’s distance.

{% tabs %} 

{% highlight xaml %}

<chart:FunnelSeries ItemsSource ="{Binding Data}" ExplodeIndex="1"
XBindingPath="Status" 
YBindingPath="Value" />

{% endhighlight %}

{% highlight c# %}

FunnelSeries funnelSeries = new FunnelSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Status", 
	YBindingPath = "Value", 
	ExplodeIndex = 1 
};

{% endhighlight %}

{% endtabs %}

Also, the segments can be exploded by touch using [`ExplodeOnTouch`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeOnTouch.html) property of [`FunnelSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries.html). Default value of this property is false.

![Exploding a funnel segment support in Xamarin.Forms Chart](charttypes_images/charttypes_img39.png)

### Changing the minimum width of the funnel

You can change the minimum width of the funnel neck using [`MinWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries~MinWidth.html) property of [`FunnelSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries.html). Default value of minWidth is `40`.

{% tabs %} 

{% highlight xaml %}

<chart:FunnelSeries ItemsSource ="{Binding Data}" MinWidth="20"
XBindingPath="Year" 
YBindingPath="Value"/>

{% endhighlight %}

{% highlight c# %}

FunnelSeries funnelSeries = new FunnelSeries() 
{ 
	ItemsSource = Data, 
	XBindingPath = "Year", 
	YBindingPath = "Value",
	MinWidth = 20 
};

{% endhighlight %}

{% endtabs %}

![Minimum width support for funnel series in Xamarin.Forms Chart](charttypes_images/charttypes_img40.png)