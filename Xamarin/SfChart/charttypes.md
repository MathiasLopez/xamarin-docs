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

To render a line chart, create an instance of [`LineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.LineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the line.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the line.

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

![](charttypes_images/charttypes_img1.png)

## Fast Line Chart

[`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) is a line chart, but it loads faster than [`LineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.LineSeries.html). You can use this when there are large number of points to be loaded in chart. To render a fast line chart, create an instance of [`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the fast line segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

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

![](charttypes_images/charttypes_img14.png)

### Dashed Lines

[`StrokeDashArray`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries~StrokeDashArray.html) property of the [`FastLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FastLineSeries.html) is used to render fast line series with dashes.

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

![](charttypes_images/charttypes_img15.png)

## Area Chart

To render an area chart, create an instance of [`AreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AreaSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img2.png)

## Spline Area Chart

To render a spline area chart, create an instance of [`SplineAreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the spline area appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineAreaSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img3.png)

## Range Area Chart

To render a range area chart, create an instance of [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Since the [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html) requires two Y values for a point, your data should contain high and low values. High and low value specifies the maximum and minimum range of the point.

There are two ways you can provide data to range area chart,

1.You can use [`ChartDataPoint's`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html) three parameter constructor to pass x value, high and low values to [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html),

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

2.Or else you can use [`High`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~High.html) and [`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~Low.html) properties of [`RangeAreaSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeAreaSeries.html) to map the high and low values from custom object to chart.

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

![](charttypes_images/RangeArea.png)

## Stacked Area Chart

To render a stacked area chart, create an instance of [`StackingAreaSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingAreaSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the stacked area appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img4.png)

## 100% Stacked Area Chart

To render a 100% stacked area chart, create an instance of [`StackingArea100Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingArea100Series.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the 100% stacked area appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img5.png)

## Column Chart

To render a column chart, create an instance of [`ColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ColumnSeries~StrokeColor.html) – used to change the stroke color of the series. 

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

![](charttypes_images/charttypes_img6.png)

## Range Column Chart

To render a range column chart, create an instance of [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). 

Since the [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html) requires two Y values for a point, your data should contain high and low values. High and low value specifies the maximum and minimum range of the point. 

There are two ways you can provide data to RangeColumn chart,

1.You can use [`ChartDataPoint's`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html#) three parameter constructor to pass x value, high and low values to  [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html),

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


2.Or else you can use [`High`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~High.html) and [`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeSeriesBase~Low.html) properties of [`RangeColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries.html) to map the high and low values from custom object to chart. 

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

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RangeColumnSeries~StrokeColor.html) – used to change the stroke color of the series.

![](charttypes_images/charttypes_img7.png)

## Stacked Column Chart

To render a stacked column chart, create an instance of [`StackingColumnSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumnSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the stacked column segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img8.png)

## 100% Stacked Column Chart

To render a 100% stacked column chart, create an instance of [`StackingColumn100Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingColumn100Series.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the series appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img9.png)

## Bar Chart

To render a bar chart, create an instance of [`BarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the bar segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BarSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img10.png)

## Stacked Bar Chart

To render a stacked bar chart, create an instance of [`StackingBarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the stacked bar segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img11.png)

## 100% Stacked Bar Chart

To render a 100% stacked bar chart, create an instance of [`StackingBar100Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingBar100Series.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the series appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StackingSeriesBase~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img12.png)

## Spline Chart

To render a spline chart, create an instance of [`SplineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SplineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the spline segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

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

![](charttypes_images/charttypes_img13.png)

## StepLine Chart

To render a step line chart, create an instance of [`StepLineSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.StepLineSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of
[`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the spline segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

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

![](charttypes_images/stepline.png)

## Bubble Chart

To render a bubble chart, create an instance of [`BubbleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). 

Bubble chart requires 3 fields (X, Y and Size) to plot a point. Here `[‘Size’](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~Size.html) is used to specify the size of each bubble segment. 

There are two ways you can provide data to bubble chart,

1.You can use [ChartDataPoint's](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor%28IComparable,Double,Double%29.html#) three parameter constructor to pass x, y and size values to  `BubbleSeries`,

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


2.Or else you can use [`YBindingPath`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.XyDataSeries~YBindingPath.html) and [`Size`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~Size.html) properties of [`BubbleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries.html) to map the Y value and size from custom object to chart. 

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

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`MinimumRadius`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~MinimumRadius.html) – used to change the minimum size of the series.
* [`MaximumRadius`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~MaximumRadius.html) – used to change the maximum size of the series.

![](charttypes_images/charttypes_img16.png)

## Scatter Chart	

To render a scatter chart, create an instance of [`ScatterSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the scatter segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~StrokeColor.html) – used to change the stroke color of the series.
* [`ScatterWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~ScatterWidth.html) – used to change the width of the series.
* [`ScatterHeight`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ScatterSeries~ScatterHeight.html) – used to change the height of the series.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

	<chart:ScatterSeries ScatterHeight="15"
	ScatterWidth="15"
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
	XBindingPath = "Year", 
	YBindingPath = "Value" 
};
chart.Series.Add(scatterSeries);

{% endhighlight %}

{% endtabs %}

![](charttypes_images/charttypes_img17.png)

## OHLC Chart

To render an OHLC chart, create an instance of [`HiLoOpenCloseSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

OHLC chart requires five values (X, Open, High, Low and Close) to plot a point. 

There are two ways you can provide data to an OHLC chart,

1.You can use [`ChartDataPoint's`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor(IComparable,Double,Double,Double,Double).html#) five parameter constructor to pass x, open, high, low and close values to  `HiLoOpenCloseSeries`,

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

2.Or else you can use [`Open`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Open.html),[`High`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~High.html),[`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Low.html) and [`Close`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Close.html) properties of [`HiLoOpenCloseSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.HiLoOpenCloseSeries.html) to map Open, High, Low and Close values from custom object to chart.

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

You can use the following properties to customize the HiLoOpenCloseSeries segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.

![](charttypes_images/charttypes_img18.png)

### Bull and Bear Color	

In OHLC chart, [`BullFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BullFillColor.html) property is used to specify a fill color for the segments that indicates an increase in stock price in the measured time interval and [`BearFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BearFillColor.html) property is used to specify a fill color for the segments that indicates a decrease in stock price in the measured time interval.

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

![](charttypes_images/charttypes_img19.png)

## Candle Chart

To render a candle chart, create an instance of [`CandleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Candle chart requires five values (X, Open, High, Low and Close) to plot a point. 

There are two ways you can provide data to an candle chart,

1.You can use [ChartDataPoint's](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint~_ctor(IComparable,Double,Double,Double,Double).html#) five parameter constructor to pass x, open, high, low and close values to  [`CandleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries.html),

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

2.Or else you can use [`Open`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Open.html),[`High`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~High.html),[`Low`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Low.html) and [`Close`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Close.html) property of [`CandleSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries.html) to map Open, High, Low and Close values from custom object to chart.

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

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries~StrokeColor.html) – used to change the stroke color of the series.

![](charttypes_images/charttypes_img20.png)

### Bull and Bear Color

In Candle chart, [`BullFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BullFillColor.html) property is used to specify a fill color for the segments that indicates an increase in stock price in the measured time interval and [`BearFillColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~BearFillColor.html) property is used to specify a fill color for the segments that indicates a decrease in stock price in the measured time interval.

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

![](charttypes_images/charttypes_img21.png)

### EnableSolidCandles

In Candle Series, [`EnableSolidCandles`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CandleSeries~EnableSolidCandles.html) property is used to specify the filled candles for the Candle Segments.

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

To render a radar chart, create an instance of [`RadarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.RadarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).  

### Draw type

[`DrawType`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~DrawType.html) property is used to specify the radar series rendering type. Following are the two options you can set to this property,

* [`Line`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using line series.
* [`Area`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using area series.

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

![](ChartTypes_images/Radar.png)

### Customize the appearance

You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`BorderWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`BorderColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~StrokeColor.html) – used to change the stroke color of the series when draw types is set to `Area`

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

![](ChartTypes_images/RadarCustomization.png)

### Closed

[`Closed`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~IsClosed.html) property is used to determine, whether to connect the first and last data point of the series. By default, the property is set to `true`.

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

![](ChartTypes_images/RadarClosed.png)

## Polar Chart

To render a polar chart, create an instance of [`PolarSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). 
 

### Draw type

[`DrawType`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~DrawType.html) property is used to specify the polar series rendering type. Following are the two options you can set to this property,

* [`Line`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using line series.
* [`Area`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesDrawType.html) – data points are visualized using area series.

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

![](ChartTypes_images/Polar.png)

### Customize the appearance

You can use the following properties to customize the appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`BorderWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`BorderColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~StrokeColor.html) – used to change the stroke color of the series when draw types is set to `Area`

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

![](ChartTypes_images/PolarCustomization.png)

### Closed

[`Closed`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PolarRadarSeriesBase~IsClosed.html) property is used to determine, whether to connect the first and last data point of the series. By default, the property is set to `true`.

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

![](ChartTypes_images/PolarClosed.png)

## Pie Chart

To render a pie chart, create an instance of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the pie segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img22.png)

### Changing the pie size

You can use [`CircularCoefficient`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~CircularCoefficient.html) property to change the diameter of the pie chart with respect to the plot area. It ranges from 0 to 1 and the default value is `0.8`.

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

![](charttypes_images/charttypes_img23.png)

### Exploding a pie segment

You can explode a pie segment using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property and specify the explode radius using [`ExplodeRadius`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~ExplodeRadius.html) property of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html).

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

![](charttypes_images/charttypes_img24.png)

### Exploding all the segments

Using [`ExplodeAll`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeAll.html) property of [`PieSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PieSeries.html), you can explode all the pie segments.

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

![](charttypes_images/charttypes_img25.png)

### Sector of Pie

SfChart allows you to render all the data points/segments in semi-pie, quarter-pie or in any sector using [`StartAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~StartAngle.html) and [`EndAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~EndAngle.html) properties.

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

![](charttypes_images/charttypes_img26.png)

## Doughnut Chart

To render a doughnut chart, create an instance of [`DoughnutSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the doughnut segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img27.png)

### Changing Doughnut inner radius

You can change the doughnut chart inner radius using [`DoughnutCoefficient`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DoughnutSeries~DoughnutCoefficient.html) with respect to the plot area. It ranges from 0 to 1 and the default value is `0.4`.

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

![](charttypes_images/charttypes_img28.png)

### Changing the doughnut size

You can use the [`CircularCoefficient`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~CircularCoefficient.html) property to change the diameter of the doughnut chart with respect to the plot area. It ranges from 0 to 1 and the default value is 0.8.

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

![](charttypes_images/charttypes_img29.png)

### Exploding a doughnut segment

Exploding a specific doughnut segment, you have to set the index to be exploded using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property of the series.

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

![](charttypes_images/charttypes_img30.png)

### Exploding all the segments

To explode all the segments, you have to enable [`ExplodeAll`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeAll.html) property of the series.

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

![](charttypes_images/charttypes_img31.png)

### Sector of Doughnut

SfChart allows you to render all the data points/segments in semi-doughnut, quarter- doughnut or in any sector using [`StartAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~StartAngle.html) and [`EndAngle`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.CircularSeries~EndAngle.html) properties.

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

![](charttypes_images/charttypes_img32.png)

## Pyramid Chart

To render a pyramid chart, create an instance of [`PyramidSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PyramidSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the pyramid segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img33.png)

### Pyramid Mode

You can render the pyramid series as linear or surface mode. In linear mode, height of the pyramid segment is based on the Y value and in surface mode, area of the pyramid segment is based on the Y values. The default value of [`PyramidMode`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.PyramidSeries~PyramidMode.html) property is [`Linear`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartPyramidMode.html).

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

![](charttypes_images/charttypes_img34.png)

### Gap between the segments

You can control the gap between the two segments using [`GapRatio`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~GapRatio.html) property. Its ranges from 0 to 1.

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

![](charttypes_images/charttypes_img35.png)

### Exploding a pyramid segment

You can explode a pyramid segment using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property, and [`ExplodeOffset`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~ExplodeOffset.html) property is used to specify the exploded segment’s distance.

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

{% endtabs %}

![](charttypes_images/charttypes_img36.png)

## Funnel Chart

To render a funnel chart, create an instance of [`FunnelSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries.html) and add to the [`Series`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Series.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html). You can use the following properties to customize the funnel segment appearance.

* [`Color`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~Color.html) – used to change the color of the series.
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~StrokeWidth.html) – used to change the stroke width of the series.
* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~StrokeColor.html) – used to change the stroke color of the series.

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

![](charttypes_images/charttypes_img37.png)

### Gap between the segments

You can control the gap between the two segments using [`GapRatio`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~GapRatio.html) property. Its ranges from 0 to 1.

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

![](charttypes_images/charttypes_img38.png)

### Exploding a funnel segment

You can explode a pyramid segment using [`ExplodeIndex`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.AccumulationSeries~ExplodeIndex.html) property and [`ExplodeOffset`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.TriangularSeries~ExplodeOffset.html) property is used to specify the exploded segment’s distance.

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

![](charttypes_images/charttypes_img39.png)

### Changing the minimum width of the funnel

You can change the minimum width of the funnel neck using [`MinWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries~MinWidth.html) property of [`FunnelSeries`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FunnelSeries.html). Default value of minWidth is `40`.

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

![](charttypes_images/charttypes_img40.png)