---
layout: post
title: Getting Started | SfDateTimeRangeNavigator | Xamarin | Syncfusion
description: getting started
platform: xamarin
control: SfDateTimeRangeNavigator
documentation: ug
---

# Getting started

This section walks you through the steps required to add `SfDateTimeRangeNavigator` and populate it with data, and also explains how to respond to range selection performed in the control. 

## Adding RangeNavigator Reference

Syncfusion Xamarin components are available in [nuget.org](https://www.nuget.org/). To add range navigator to your project, open the NuGet package manager in Visual Studio, and search for [“syncfusion.xamarin.sfchart”](https://www.nuget.org/packages/Syncfusion.Xamarin.SfChart/), and then install it. 

![](gettingstarted_images/addref.png)

To know more about obtaining our components, refer to these links: [Mac](https://help.syncfusion.com/xamarin/introduction/download-and-installation/mac) and [Windows](https://help.syncfusion.com/xamarin/introduction/download-and-installation/windows). Also, if you prefer to manually refer the assemblies instead of NuGet, refer to this [link](https://help.syncfusion.com/xamarin/introduction/control-dependencies#sfdatetimerangenavigator) to know about the dependent assemblies for range navigator. 

I> After adding the reference, currently, an additional step is required for iOS and UWP projects. We need to initialize the renderer as explained in this [KB article](https://www.syncfusion.com/kb/7977/how-to-resolve-sfdatetimerangenavigator-not-rendering-issue-in-ios-and-uwp).

I> For UWP alone, one more additional step is required if the project is built in release mode with .NET Native tool chain enabled. You can refer to the [KB article](https://www.syncfusion.com/kb/7944/how-to-make-syncfusion-xamarin-forms-range-navigator-to-work-in-uwp-in-release-mode-when-net-native) for more details.
 
## Adding and configuring SfDateTimeRangeNavigator 

First, let us initialize the control with major and minor date time scales by specifying the minimum and maximum date to be visualized in the control using [`Minimum`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~Minimum.html) and [`Maximum`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~Maximum.html) properties.

Following code example illustrates this,

{% highlight c# %}
[C#]

SfDateTimeRangeNavigator rangeNavigator = new SfDateTimeRangeNavigator();

rangeNavigator.Minimum = new DateTime(2015, 01, 01);

rangeNavigator.Maximum = new DateTime(2016, 01, 01);

{% endhighlight %}

![](gettingstarted_images/gettingstarted_img1.jpeg)

N> If you don’t specify [`Minimum`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~Minimum.html) and [`Maximum`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~Maximum.html) properties, minimum and maximum dates will be chosen automatically based on the provided data using [`ItemsSource`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~ItemsSource.html) property, which is explained in the next step in this section.

Next, create a data model representing the list of sample data.

{% highlight c# %}
[C#]

public class DataModel
{
	public ObservableCollection<Model> DateTimeData;
	
	DataModel()
	{ 		
		DateTimeData = new ObservableCollection<Model>()
		{ 
			
			new Model (new DateTime(2015, 01, 01), 14), 
			new Model (new DateTime(2015, 02, 01), 54), 
			new Model (new DateTime(2015, 03, 01), 23), 
			new Model (new DateTime(2015, 04, 01), 53), 
			new Model (new DateTime(2015, 05, 01), 25), 
			new Model (new DateTime(2015, 06, 01), 32), 
			new Model (new DateTime(2015, 07, 01), 78), 
			new Model (new DateTime(2015, 08, 01), 100), 
			new Model (new DateTime(2015, 09, 01), 55), 
			new Model (new DateTime(2015, 10, 01), 38), 
			new Model (new DateTime(2015, 11, 01), 27), 
			new Model (new DateTime(2015, 12, 01), 56), 
			new Model (new DateTime(2016, 01, 01), 33) 
			
		}; 
	} 
} 

public class Model 
{ 
	public DateTime Date { get; set; } 
	
	public double Value { get; set; } 
	
	public Model(DateTime dateTime, double value) 
	{ 
		Date = dateTime;
		Value = value; 
	} 
} 

{% endhighlight %}

Then, let us populate the chart, which is displayed inside the `SfDateTimeRangeNavigator`, by setting the above data using [`ItemsSource`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~ItemsSource.html) property. And then specify the property names which contain the x and y values in the model using [`XBindingPath`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~XBindingPath.html) and [`YBindingPath`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~YBindingPath.html) properties.

N> By default, data is visualized using line series. You can change the chart type or add more series by accessing the SfChart instance using [`SfDateTimeRangeNavigator.Content`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~Content.html) property. 

{% highlight c# %}
[C#]

SfDateTimeRangeNavigator rangeNavigator = new SfDateTimeRangeNavigator() 
{ 
	rangeNavigator.ItemsSource = dataModel.DateTimeData, 
	rangeNavigator.XBindingPath = "Date", 
	rangeNavigator.YBindingPath = "Value" 
};  

{% endhighlight %}

![](gettingstarted_images/gettingstarted_img2.jpeg)

## Handle range selection

In real time, other controls like chart, grid etc., are updated in response to the range selection performed in SfDateTimeRangeNavigator. You can handle the selection using [`RangeChanged`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~RangeChanged_EV.html) event and update other controls based on the selected date time or perform some other tasks using the selected data.

N> You can get the selected date time using [`ViewRangeStart`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.RangeChangedEventArgs~ViewRangeStartDate.html) and [`ViewRangeEnd`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.RangeChangedEventArgs~ViewRangeEndDate.html) properties or you can get selected data using [`SelectedData`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.RangeNavigator.XForms.SfDateTimeRangeNavigator~SelectedData.html) property.

Following code example illustrates how to handle range selection and update chart's date time axis range,

{% highlight c# %}
[C#]

rangeNavigator.RangeChanged += rangeNavigator_RangeChanged;  


private void rangeNavigator_RangeChanged(object sender, RangeChangedEventArgs e) 
{ 
	//Updating chart's date time range 
	dateTimeAxis.Minimum = e.ViewRangeStartDate; 
	dateTimeAxis.Maximum = e.ViewRangeEndDate; 
}  

{% endhighlight %}

![](gettingstarted_images/gettingstarted_img3.jpeg)