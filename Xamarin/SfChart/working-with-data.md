---
layout: post
title: Populating data
description: How to add data point to series in  Essential Xamarin.forms Chart.
platform: xamarin
control: Chart
documentation: ug
---

# Populating Data

[`SfChart`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html) control can be configured with data points using [`ItemsSource`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~ItemsSource.html) property of [`ChartSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries.html). There are two ways, you can create data points for chart.

## Chart Data Point	

One way is to create a collection of [ChartDataPoint](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint.html#) objects and assign this collection to [`ItemsSource`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~ItemsSource.html) property. Here, each [`ChartDataPoint`](http://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint.html#) object represents a data point in a chart series.

N> [`ChartDataPoint`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataPoint.html) class has few overloaded constructors depending on the number of y-values required to plot a data point for a particular series type. For example, you can use a constructor with two parameters to instantiate data point for [`XYDataSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.XyDataSeries.html) like Line, Spline, and Pie etc.

Following code snippet illustrates this,

{% highlight c# %}

public class DataModel
{
	
	public ObservableCollection<ChartDataPoint>  HighTemperature{ get; set; }

	public DataModel ()
	{
	
		HighTemperature = new ObservableCollection<ChartDataPoint> ();

		HighTemperature.Add (new ChartDataPoint ("Jan", 42));
		HighTemperature.Add (new ChartDataPoint ("Feb", 44));
		HighTemperature.Add (new ChartDataPoint ("Mar", 53));
		HighTemperature.Add (new ChartDataPoint ("Apr", 64));
		HighTemperature.Add (new ChartDataPoint ("May", 75));
		HighTemperature.Add (new ChartDataPoint ("Jun", 83));
		HighTemperature.Add (new ChartDataPoint ("Jul", 87));
		HighTemperature.Add (new ChartDataPoint ("Aug", 84));
		HighTemperature.Add (new ChartDataPoint ("Sep", 78));
		HighTemperature.Add (new ChartDataPoint ("Oct", 67));
		HighTemperature.Add (new ChartDataPoint ("Nov", 55));
		HighTemperature.Add (new ChartDataPoint ("Dec", 45));

	}

}

{% endhighlight %}

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>

	<chart:SfChart.Series>

		<chart:ColumnSeries ItemsSource="{Binding HighTemperature}"/>

	</chart:SfChart.Series> 

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

//Adding the series to the chart and set the ItemsSource property

chart.Series.Add (new ColumnSeries () {
	
	ItemsSource = dataModel.HighTemperature

});

{% endhighlight %}

{% endtabs %}

## Custom Object

Another way is to assign a collection of custom objects to the [`ItemsSource`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~ItemsSource.html) property. In this case, you need to set the [`XBindingPath`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSeries~XBindingPath.html) and [`YBindingPath`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.XyDataSeries~YBindingPath.html) properties of chart series with the property names of the custom object which contains the x-value/category and y-value respectively.

N> While using custom objects, XBindingPath property is required for all types of chart series. You need to set [`YBindingPath`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.XyDataSeries~YBindingPath.html) property only for the [`XYDataSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.XyDataSeries.html) types which needs single y-value for a data point. For example, Line, Spline, Column, Bar, Pie etc.  For [`BubbleSeries`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries.html) type, you need to set both YBindingPath and [`Size`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.BubbleSeries~Size.html) properties since it requires two y-values to plot a single bubble data point. In the case of financial series types like Candle and HiLoOpenClose, which requires four y-values for a single data point, you need to set [`High`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~High.html), [`Low`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Low.html), [`Open`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Open.html) and [`Close`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.FinancialSeriesBase~Close.html) properties with the property names of a custom object which contains respective values.

{% highlight c# %}
[C#]

public class MonthDemand

{

	public MonthDemand(string demand, double year2010, double year2011)
	{

		this.Demand = demand;

		this.Year2010 = year2010;

		this.Year2011 = year2011;

	}

	public string Demand { get; set; }

	public double Year2010 { get; set; }

	public double Year2011 { get; set; }

}

public class DataModel
{
	
	public ObservableCollection<MonthDemand>  Demands{ get; set; }

	public DataModel ()
	{

		Demands = new ObservableCollection<MonthDemand>();

		Demands.Add(new MonthDemand("Jan", 42, 27));
		Demands.Add(new MonthDemand("Feb", 44, 28));
		Demands.Add(new MonthDemand("Mar", 53, 35));
		Demands.Add(new MonthDemand("Apr", 64, 44));
		Demands.Add(new MonthDemand("May", 75, 54));
		Demands.Add(new MonthDemand("Jun", 83, 63));
		Demands.Add(new MonthDemand("Jul", 87, 68));
		Demands.Add(new MonthDemand("Aug", 84, 66));
		Demands.Add(new MonthDemand("Sep", 78, 59));
		Demands.Add(new MonthDemand("Oct", 67, 48));
		Demands.Add(new MonthDemand("Nov", 55, 38));
		Demands.Add(new MonthDemand("Dec", 45, 29));

	}

}   

{% endhighlight %}

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>
...

  <chart:SfChart.Series>

	  <chart:ColumnSeries ItemsSource="{Binding Demands}" XBindingPath="Demand" 
	 					  YBindingPath="Year2010"/>

  </chart:SfChart.Series>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

chart.Series.Add (new ColumnSeries () {
	
	ItemsSource = dataModel.Demands,

	XBindingPath = "Demand",

	YBindingPath = "Year2010"

});

{% endhighlight %}

{% endtabs %}