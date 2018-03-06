---
layout: post
title: Zooming and Panning
description: How to add ZoomPan behavior in Essential Xamarin.Forms Chart
platform: xamarin
control: Chart
documentation: ug
---

# Zooming and Panning

## Enable Zooming

Chart allows you to zoom in to view the data clearly. To enable this feature, you need to add an instance of [`ChartZoomPanBehavior`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior.html) to the [`ChartBehaviors`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartBehavior.html) collection property of [`SfChart`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart.html).

Following properties are used to configure the zooming feature,

* [`EnableZooming`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~EnableZooming.html) – used to enable/disable the pinch zooming. Default value is true. 
* [`EnableDoubleTap`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~EnableDoubleTap.html) – when you enable this property, you can double tap on the chart to reset it to the original size or zoom in by one level.
* [`EnableSelectionZooming`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~EnableSelectionZooming.html) – when this property is set to true, you can double tap and drag to select a range on the chart to be zoomed in.
* [`EnablePanning`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~EnablePanning.html) – used to enable/disable the panning. Default value is true.

Following code snippet illustrates how to enable zooming.

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>

	<chart:SfChart.ChartBehaviors>
	
		<chart:ChartZoomPanBehavior/>
		
	</chart:SfChart.ChartBehaviors>
	
</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();

ChartZoomPanBehavior zoomPanBehavior = new ChartZoomPanBehavior();

chart.ChartBehaviors.Add(zoomPanBehavior);

{% endhighlight %}

{% endtabs %}

Following code snippet illustrates how to enable the box selection zooming,

{% tabs %} 

{% highlight xaml %}

<chart:SfChart>

	<chart:SfChart.ChartBehaviors>

		<chart:ChartZoomPanBehavior EnableSelectionZooming="True"/>

	</chart:SfChart.ChartBehaviors>

</chart:SfChart>

{% endhighlight %}

{% highlight c# %}

SfChart chart = new SfChart();

ChartZoomPanBehavior zoomPanBehavior = new ChartZoomPanBehavior();

zoomPanBehavior.EnableSelectionZooming = true;

chart.ChartBehaviors.Add(zoomPanBehavior);

{% endhighlight %}

{% endtabs %}

Following screenshot shows the box selection on chart area,

![](zoompan_images/zoompan_img1.png)

Following screenshot shows the zoomed area,

![](zoompan_images/zoompan_img2.png)

## Zoom Mode

The [`ZoomMode`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~ZoomMode.html) property specifies whether chart should be allowed to scale along horizontal axis or vertical axis or along both axis. The default value of [`ZoomMode`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ZoomMode.html) is [`XY`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ZoomMode.html) (both axis).

Following code example illustrates how to restrict the chart to be zoomed only along horizontal axis,

{% tabs %} 

{% highlight xaml %}

<chart:SfChart.ChartBehaviors>

	<chart:ChartZoomPanBehavior ZoomMode="X"/>

</chart:SfChart.ChartBehaviors>

{% endhighlight %}

{% highlight c# %}

ChartZoomPanBehavior zoomPanBehavior = new ChartZoomPanBehavior();

zoomPanBehavior.ZoomMode = ZoomMode.X;

{% endhighlight %}

{% endtabs %}

![](zoompan_images/zoompan_img3.png)

## Events

**ZoomStart**

[`ZoomStart`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~ZoomStart_EV.html) event is triggered when the user starts zooming the chart through pinch gesture, and this is a cancelable event. The argument contains the following information.

* [`Axis`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~Axis.html) – the zoom start event will be triggered for all the axis in the Chart.
* [`CurrentZoomFactor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~CurrentZoomFactor.html) – used to get the new zoom factor of the corresponding axis.
* [`CurrentZoomPosition`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~CurrentZoomPosition.html) – used to get the new zoom position of the corresponding axis.
* [`Cancel`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomStartEventArgs~Cancel.html) – used to set the value indicating whether the zooming should be canceled.

**ZoomDelta**

[`ZoomDelta`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~ZoomDelta_EV.html) event is triggered while zooming, and this is a cancelable event. The argument contains the following information.

* [`Axis`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~Axis.html) – Instance of the axis whose range is changed because of zooming. This event is triggered for each axis in the chart.
* [`PreviousZoomFactor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomDeltaEventArgs~PreviousZoomFactor.html) – used to get the previous zoom factor of the axis.
* [`PreviousZoomPosition`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomDeltaEventArgs~PreviousZoomPosition.html) – used to get the previous zoom position of the axis.
* [`CurrentZoomFactor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~CurrentZoomFactor.html) – used to get the current zoom factor of the axis.
* [`CurrentZoomPosition`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~CurrentZoomPosition.html) – used to get the current zoom position of the axis.
* [`Cancel`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomDeltaEventArgs~Cancel.html) – used to set the value indicating whether the zooming should be canceled.

**ZoomEnd**

[`ZoomEnd`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~ZoomEnd_EV.html) event is triggered after the zooming is stopped. The argument contains the following information.

* [`Axis`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~Axis.html) – Instance of the axis whose range is changed because of zooming. This event is triggered for each axis in the chart.
* [`CurrentZoomFactor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~CurrentZoomFactor.html) – the axis zoom factor after zoom.
* [`CurrentZoomPosition`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomEventArgs~CurrentZoomPosition.html) - the axis zoom position after zoom.

**SelectionZoomStart**

[`SelectionZoomStart`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~SelectionZoomStart_EV.html) event is triggered when the user starts the box selection zooming. The argument contains the following information.

* [`ZoomRect`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSelectionZoomEventArgs~ZoomRect.html) – used to get the initial bounds of the box selection.

**SelectionZoomDelta**

[`SelectionZoomDelta`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~SelectionZoomDelta_EV.html) event is triggered while selecting a region to be zoomed, and this is a cancelable event. The argument contains the following information.

* [`ZoomRect`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSelectionZoomEventArgs~ZoomRect.html) – contains the bounds of the currently selected region.
* [`Cancel`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSelectionZoomDeltaEventArgs~Cancel.html) – used to set the value indicating whether the box selection zooming should be canceled.

**SelectionZoomEnd**

[`SelectionZoomEnd`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~SelectionZoomEnd_EV.html) event is triggered after selection zooming ends. The argument contains the following information.

* [`ZoomRect`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartSelectionZoomEventArgs~ZoomRect.html) – used to get the final bounds of the zoomed region.

**Scroll**

[`Scroll`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~Scroll_EV.html) event is triggered while panning, and this is a cancelable event. The argument contains the following information.

* [`Axis`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScrollEventArgs~Axis.html) – Instance of the axis whose range is changed while panning. This event is triggered for each axis in the chart.
* [`ZoomPosition`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScrollEventArgs~ZoomPosition.html) – the current zoom position of the axis.
* [`Cancel`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartScrollEventArgs~Cancel.html) – used to set a value indicating whether the scrolling should be canceled.

**ResetZoom**

[`ResetZoom`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.SfChart~ResetZoom_EV.html) event is triggered after the chart is reset on double tap. The argument contains the following information.

* [`Axis`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartResetZoomEventArgs~Axis.html) – Instance of the axis whose range is changed because of this event. This event is triggered for each axis in the chart.
* [`PreviousZoomFactor`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartResetZoomEventArgs~PreviousZoomFactor.html) – used to get the previous zoom factor.
* [`PreviousZoomPosition`](http://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartResetZoomEventArgs~PreviousZoomPosition.html) – used to get the previous zoom position.

## Methods

Zooming and panning can be performed programmatically with the following methods:

### ZoomIn

[`ZoomIn`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~ZoomIn.html) method is used to increase the magnification of the plot area to view the data clearly.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.ZoomIn();

{% endhighlight %}

### ZoomOut

[`ZoomOut`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~ZoomOut.html) is used to decrease the magnification of the plot area to reset the default view.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.ZoomOut();

{% endhighlight %}

### Zoom

**Zoom(factor)**

This method is used to change the zoom level by using zoom factor.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.Zoom(0.5f);

{% endhighlight %}

**Zoom(Rect)**

This method is used to zoom the chart for a given rectangle value.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.Zoom(new Rect(10, 10, 200, 350));

{% endhighlight %}

**Zoom(chartAxis, cumulativeLevel, origin)**

This method is used to change the zoom level of given axis to the specified level and origin.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.Zoom(axis, 0.5f, 0.5f);

{% endhighlight %}

### ZoomByRange

**ZoomByRange(chartAxis, start, end)**

This method is used to zoom the given axis to the given range.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.ZoomByRange(axis, 20, 25);

{% endhighlight %}

**ZoomByRange(dateTimeAxis, start, end)**

This method is used to zoom the given axis to the given date time range.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.ZoomByRange(axis, new DateTime(2017,3,1), new DateTime(2017,5,1));

{% endhighlight %}

### ZoomToFactor(chartAxis,zoomPosition,zoomFactor)

[`ZoomToFactor`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~ZoomToFactor.html) method is used to change the zoom level by using zoom position and zoom factor. Zoom position value specifies the starting point of zooming, and zoom factor value specifies the level of zooming.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.ZoomToFactor(axis, 0.5f, 0.5f);

{% endhighlight %}


### Reset

[`Reset`](https://help.syncfusion.com/cr/cref_files/xamarin/sfchart/Syncfusion.SfChart.XForms~Syncfusion.SfChart.XForms.ChartZoomPanBehavior~Reset.html) method is used to return the plot area back to its original position after zooming.

{% highlight c# %}

ChartZoomPanBehavior zoomPan = new ChartZoomPanBehavior();

zoomPan.Reset();

{% endhighlight %}

