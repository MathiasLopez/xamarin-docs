---
layout: post
title: Range in Syncfusion RangeSlider control for Xamarin.Forms
description: Learn how to set Dual thumb slider and its ranges in RangeSlider control.
platform: Xamarin
control: RangeSlider
documentation: ug
---

# Range

The SfRangeSlider control supports to select range of value by using two Thumbs.

## Set Show Range

The `ShowRange` property should be set to true for displaying two thumbs in track with range of values.

N> When this property is set to false, single thumb is displayed without any range 

{% tabs %}

{% highlight xaml %}

	<range:SfRangeSlider x:Name="rangeslider" ShowRange="true"/>
	
{% endhighlight %}

{% highlight c# %}

	rangeslider.ShowRange= true;

{% endhighlight %}

{% endtabs %}


## Set Range values

This section explains about setting Range start and end value.

## RangeStart

Gets and sets the start value of the range.

{% tabs %}

{% highlight xaml %}

	<range:SfRangeSlider x:Name="rangeslider"  RangeStart="4" />
	
{% endhighlight %}

{% highlight c# %}

	rangeslider.RangeStart=0;

{% endhighlight %}

{% endtabs %}

## RangeEnd

Gets and sets the end value of the range.

{% tabs %}

{% highlight xaml %}

	<range:SfRangeSlider x:Name="rangeslider" RangeEnd="20" />
	
{% endhighlight %}

{% highlight c# %}

	rangeslider.RangeEnd=10;

{% endhighlight  %}

{% endtabs %}
