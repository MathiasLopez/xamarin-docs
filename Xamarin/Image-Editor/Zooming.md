---
layout: post
title: Zooming and Panning operations in Syncfusion SfImageEditor
description: Learn how to perform Zooming and panning in the image in SfImageEditor control for Xamarin.Forms platform
platform: xamarin.forms
control: ImageEditor
documentation: ug
---

# Zooming in SfImageEditor

The image editor control provides support to zoom and pan actions over an image.

The following properties are used for zooming feature of the image editor control:

* EnableZooming
* Maximum ZoomLevel
* PanningMode

## Enable zooming

You can enable or disable the zooming functionality by setting the [`EnableZooming`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfImageEditor.XForms~Syncfusion.SfImageEditor.XForms.SfImageEditor~EnableZooming.html) value to true or false. By default, the `EnableZooming` value is set to true.

{% tabs %}

{% highlight XAML %}
  
    <imageeditor:SfImageEditor  EnableZooming="false"/>
     
{% endhighlight %}

{% highlight C# %}
   
     editor.EnableZooming = false;

{% endhighlight %}

{% endtabs %}

## Maximum zoom level

You can set the maximum zoom level to image using the [`MaximumZoomLevel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfImageEditor.XForms~Syncfusion.SfImageEditor.XForms.SfImageEditor~MaximumZoomLevel.html) property.

{% tabs %}

{% highlight XAML %}
  
    <imageeditor:SfImageEditor EnableZooming="true"  MaximumZoomLevel="8"/>
     
{% endhighlight %}

{% highlight C# %}

     editor.EnableZooming = true;
     editor.MaximumZoomLevel = 8;

{% endhighlight %}

{% endtabs %}

## Panning mode

The image editor control provides support for panning and allows to pan the image with two fingers or single finger by setting the [`PanningMode`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfImageEditor.XForms~Syncfusion.SfImageEditor.XForms.SfImageEditor~PanningMode.html).

The following properties are used for panning:

* `SingleFinger`: Zooms or pans the image with single finger, but shapes and text selection cannot be performed with this mode.
* `TwoFinger`: Zooms or pans the image with two finger. The shapes and text selection can be performed with this mode.

By default, the [`PanningMode`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfImageEditor.XForms~Syncfusion.SfImageEditor.XForms.SfImageEditor~PanningMode.html) value is set to `TwoFinger`.

{% tabs %}

{% highlight XAML %}

    <imageeditor:SfImageEditor  EnableZooming="true" PanningMode="TwoFinger"/>

{% endhighlight %}

{% highlight C# %}

editor.PanningMode = PanningMode.TwoFinger;

{% endhighlight %}

{% endtabs %}
