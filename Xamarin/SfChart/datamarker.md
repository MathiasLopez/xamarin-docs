---
layout: post
title: Markers and data labels in Essential Xamarin.Forms Chart
description: Learn how to add markers and data point labels to a Chart series
platform: xamarin
control: Chart
documentation: ug
---

# Data Markers

Data markers are used to provide information about the data points to the user. You can add a shape and label to adorn each data point. This can be enabled using following code snippet,

{% tabs %} 

{% highlight xaml %}

<chart:LineSeries>

	<chart:LineSeries.DataMarker>

		<chart:ChartDataMarker/>

	</chart:LineSeries.DataMarker>

</chart:LineSeries>

{% endhighlight %}

{% highlight c# %}

lineSeries.DataMarker = new ChartDataMarker();

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img1.png)

## Customizing Labels

Data labels are enabled by default but you can also change the visibility of the labels using [`ShowLabel`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~ShowLabel.html) property of ChartDataMarker. The label appearance can be customized using following properties,

* [`TextColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLabelStyle~TextColor.html) – used to change the color of the label.
* [`BackgroundColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLabelStyle~BackgroundColor.html) – used to change the label background color.
* [`BorderColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLabelStyle~BorderColor.html) – used to change the border color.
* [`BorderThickness`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLabelStyle~BorderThickness.html) – used to change the thickness of the border.
* [`Font`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLabelStyle~Font.html) – used to change the text size, font family and font weight.
* [`Margin`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLabelStyle~Margin.html) - used to change the margin size for labels.
* [`Angle`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerLabelStyle~Angle.html) – used to rotate the labels.

Following code snippet illustrates the customization of label and its background,

{% tabs %} 

{% highlight xaml %}

<chart:LineSeries.DataMarker>

	<chart:ChartDataMarker ShowLabel="True">

		<chart:ChartDataMarker.LabelStyle>

			<chart:DataMarkerLabelStyle TextColor="Blue"
										BorderColor="Red" 
										BorderThickness="2"
										BackgroundColor="Aqua"
										Angle="315"
										Margin="5">

				<chart:DataMarkerLabelStyle.Font>

					<Font FontSize="18" FontAttributes="Italic"/>

				</chart:DataMarkerLabelStyle.Font>

			</chart:DataMarkerLabelStyle>

		</chart:ChartDataMarker.LabelStyle>

	</chart:ChartDataMarker>

</chart:LineSeries.DataMarker>

{% endhighlight %}

{% highlight c# %}

lineSeries.DataMarker = new ChartDataMarker();

lineSeries.DataMarker.ShowLabel = true;

lineSeries.DataMarker.LabelStyle.TextColor = Color.Blue;

lineSeries.DataMarker.LabelStyle.BorderColor = Color.Red;

lineSeries.DataMarker.LabelStyle.BorderThickness = 2;

lineSeries.DataMarker.LabelStyle.BackgroundColor = Color.Aqua;

lineSeries.DataMarker.LabelStyle.Angle = 315;

lineSeries.DataMarker.LabelStyle.Margin = 5;

lineSeries.DataMarker.LabelStyle.Font = Font.SystemFontOfSize(18, FontAttributes.Italic);

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img2.png)

## Formatting Label Content

You can customize the content of the label using LabelContent property. Following are the two options that are supported now,

* [`Percentage`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.LabelContent.html) – This will show the percentage value of corresponding data point Y value, this is often used in pie, doughnut, funnel and pyramid series types.
* [`YValue`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.LabelContent.html) – This will show the corresponding Y value.

{% tabs %} 

{% highlight xaml %}

<chart:PieSeries>

	<chart:PieSeries.DataMarker>

		<chart:ChartDataMarker LabelContent="Percentage"/>

	</chart:PieSeries.DataMarker>

</chart:PieSeries>

{% endhighlight %}

{% highlight c# %}

pieSeries.DataMarker.LabelContent = LabelContent.Percentage;

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img3.png)

## Label Position

This feature is used to position the data marker labels at Center, Inner and Outer position of the actual data point position. By default, labels are positioned based on the series types for better readability. You can move the labels horizontally and vertically using [`OffsetX`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerLabelStyle~OffsetX.html) and [`OffsetY`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.DataMarkerLabelStyle~OffsetY.html) properties respectively.

The following screenshot illustrates the default position of data marker labels,

![](datamarker_images/datamarker_img4.png)

The following code sample illustrates the center position of data marker labels,

{% tabs %} 

{% highlight xaml %}

<chart:ChartDataMarker>

	<chart:ChartDataMarker.LabelStyle>

		<chart:DataMarkerLabelStyle LabelPosition="Center"/>

	</chart:ChartDataMarker.LabelStyle>

</chart:ChartDataMarker>

{% endhighlight %}

{% highlight c# %}

series.DataMarker.LabelStyle.LabelPosition = DataMarkerLabelPosition.Center;

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img5.png)

The following code sample illustrates the Inner position of data marker labels,

{% tabs %} 

{% highlight xaml %}

<chart:ChartDataMarker>

	<chart:ChartDataMarker.LabelStyle>

		<chart:DataMarkerLabelStyle LabelPosition="Inner"/>

	</chart:ChartDataMarker.LabelStyle>

</chart:ChartDataMarker>

{% endhighlight %}

{% highlight c# %}

series.DataMarker.LabelStyle.LabelPosition = DataMarkerLabelPosition.Inner;

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img6.png)

The following code sample illustrates the outer position of data marker labels, 

{% tabs %} 

{% highlight xaml %}

<chart:ChartDataMarker>

	<chart:ChartDataMarker.LabelStyle>

		<chart:DataMarkerLabelStyle LabelPosition="Outer"/>

	</chart:ChartDataMarker.LabelStyle>

</chart:ChartDataMarker>

{% endhighlight %}

{% highlight c# %}

series.DataMarker.LabelStyle.LabelPosition = DataMarkerLabelPosition.Outer;

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img7.png)

## Smart Labels

This feature is used to arrange the data marker labels smartly and avoid the intersection when there is overlapping of labels. The property `EnableSmartLabels` in CircularSeries, is used to arrange the data marker labels smartly. By default, it is false, we need to enable this property.

The following code sample illustrates how to enable the smart labels.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart.Series>

	<chart:PieSeries ItemsSource="{Binding Data}"
					 XBindingPath="Expense"
					 YBindingPath="Value" 
					 StartAngle="75"
					 EndAngle ="435"
					 EnableSmartLabels="True"
					 ConnectorLineType = "Bezier" 
					 DataMarkerPosition = "OutsideExtended">
	
		<chart:PieSeries.DataMarker>
			<chart:ChartDataMarker />
		</chart:PieSeries.DataMarker>
		
	</chart:PieSeries>
	
</chart:SfChart.Series> 

{% endhighlight %}

{% highlight c# %}        

SfChart chart = new SfChart();
...

PieSeries pieSeries = new PieSeries()
{
	
	ItemsSource = Data,
	XBindingPath = "Expense",
	YBindingPath = "Value",
	EnableSmartLabels = true,
	DataMarkerPosition = CircularSeriesDataMarkerPosition.OutsideExtended,
	ConnectorLineType= ConnectorLineType.Bezier,
	StartAngle=75,
	EndAngle=435,
	DataMarker=new ChartDataMarker(),
	
};

chart.Series.Add(pieSeries);

{% endhighlight %}

{% endtabs %}

![](datamarker_images/smartlabels.png)

## Customizing Marker Shapes

Shapes can be added to chart data marker by setting the [`ShowMarker`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~ShowMarker.html) property to `true`. There are different shapes you can set to the chart using [`MarkerType`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~MarkerType.html) property such as rectangle, circle, diamond etc. Following properties are used to customize marker appearance,

* [`MarkerWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~MarkerWidth.html) - used to change the width of the marker
* [`MarkerHeight`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~MarkerHeight.html) - used to change the height of the marker
* [`MarkerColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~MarkerColor.html) - used to change the color of the marker
* [`MarkerBorderColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~MarkerBorderColor.html) - used to change the border color of the shape
* [`MarkerBorderWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~MarkerBorderWidth.html) – used to change the marker border thickness

The following code example shows how to enable marker and specify its types,

{% tabs %} 

{% highlight xaml %}

<chart:LineSeries.DataMarker>

	<chart:ChartDataMarker ShowLabel="False" 
						   ShowMarker="True"
						   MarkerType="Hexagon"
						   MarkerWidth="20" 
						   MarkerHeight="20"
						   MarkerColor="Aqua" 
						   MarkerBorderColor="Red"
						   MarkerBorderWidth="2"/>

</chart:LineSeries.DataMarker>

{% endhighlight %}

{% highlight c# %}  

lineSeries.DataMarker = new ChartDataMarker();

lineSeries.DataMarker.ShowLabel = false;

lineSeries.DataMarker.ShowMarker = true;

lineSeries.DataMarker.MarkerType = DataMarkerType.Hexagon;

lineSeries.DataMarker.MarkerWidth = 20;

lineSeries.DataMarker.MarkerHeight = 20;

lineSeries.DataMarker.MarkerColor = Color.Aqua;

lineSeries.DataMarker.MarkerBorderColor = Color.Red;

lineSeries.DataMarker.MarkerBorderWidth = 2;

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img8.png)

## Connector Line

This feature is used to connect label and data point using a line. It can be enabled for any chart types but this is often used with Pie and Doughnut chart types. Following properties used to customize connector line,

* [`StrokeColor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLineStyle~StrokeColor.html) – used to change the color of the line
* [`StrokeWidth`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLineStyle~StrokeWidth.html) – used to change the stroke thickness of the line
* [`StrokeDashArray`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartLineStyle~StrokeDashArray.html) – used to set the dashes for the line

The following code illustrates how to specify the connector height and its angle,

{% tabs %} 

{% highlight xaml %}
      
<chart:LineSeries.DataMarker>

	<chart:ChartDataMarker>

		<chart:ChartDataMarker.ConnectorLineStyle>

			<chart:ConnectorLineStyle ConnectorHeight="50"
									  ConnectorRotationAngle="175" 
									  StrokeColor="Blue"
									  StrokeWidth="3"/>

		</chart:ChartDataMarker.ConnectorLineStyle>

	</chart:ChartDataMarker>

</chart:LineSeries.DataMarker>

{% endhighlight %}

{% highlight c# %}

lineSeries.DataMarker.ConnectorLineStyle.ConnectorHeight = 50;

lineSeries.DataMarker.ConnectorLineStyle.ConnectorRotationAngle = 175;

lineSeries.DataMarker.ConnectorLineStyle.StrokeColor = Color.Blue;

lineSeries.DataMarker.ConnectorLineStyle.StrokeWidth = 3;

lineSeries.DataMarker.ConnectorLineStyle.StrokeDashArray = new double[2] { 2, 3 };

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img9.png)

N> For Pie and Doughnut series, you can set the Bezier curve for connector line using ConnectorType property of Pie and Doughnut series.

## Label Template

You can customize the appearance of the data marker label with your own template by using [`LabelTemplate`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker~LabelTemplate.html) property of [`ChartDataMarker`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartDataMarker.html).

{% tabs %} 

{% highlight xaml %}

<ContentPage.Resources>
    <ResourceDictionary>
       <DataTemplate x:Key="dataMarkerTemplate">
          <StackLayout Orientation="Horizontal">
             <Label Text="{Binding Value}" VerticalOptions="Center" FontSize = "15"/>
             <Image Source="Down.jpg" WidthRequest="30" HeightRequest="30"/>
          </StackLayout>
       </DataTemplate>    
    </ResourceDictionary>
</ContentPage.Resources>

<chart:SfChart.Series>
    <chart:BarSeries ItemsSource="{Binding Data}" XBindingPath="Name" YBindingPath="Value">
        <chart:BarSeries.DataMarker>
            <chart:ChartDataMarker ShowLabel="True" LabelTemplate="{StaticResource dataMarkerTemplate}">
	            <chart:ChartDataMarker.LabelStyle>
		            <chart:DataMarkerLabelStyle LabelPosition="Outer" />
	            </chart:ChartDataMarker.LabelStyle>
	        </chart:ChartDataMarker>
        </chart:BarSeries.DataMarker>
    </chart:BarSeries>
</chart:SfChart.Series>


{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart ();
...

var barSeries = new BarSeries();
barSeries.Color = Color.FromRgb(231, 87, 89);
barSeries.ItemsSource = Data;
barSeries.XBindingPath = "Name";
barSeries.YBindingPath = "Value";
barSeries.DataMarker = new ChartDataMarker();
barSeries.DataMarker.ShowLabel = true;
barSeries.DataMarker.LabelStyle.LabelPosition = DataMarkerLabelPosition.Outer;

DataTemplate dataMarkerTemplate = new DataTemplate(() => 
{
    StackLayout stack = new StackLayout();
    stack.Orientation = StackOrientation.Horizontal;
    Label label = new Label();
    label.SetBinding(Label.TextProperty, "Value");
    label.FontSize = 15;
    label.VerticalOptions = LayoutOptions.Center;
    Image image = new Image();
    image.Source = "Down.jpg";
    image.WidthRequest = 30;
    image.HeightRequest = 30;
    stack.Children.Add(label);
    stack.Children.Add(image);
    return stack;
});

barSeries.DataMarker.LabelTemplate = dataMarkerTemplate;
chart.Series.Add(barSeries);

{% endhighlight %}

{% endtabs %}

![](datamarker_images/datamarker_img10.png)

