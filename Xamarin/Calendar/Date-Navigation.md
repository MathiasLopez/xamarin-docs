---
layout: post
title: Date Navigation and Gestures | SfCalendar | Xamarin.Forms | Syncfusion
description: Learn the complete navigation and gestures support
platform: Xamarin
control: Calendar
documentation: ug
---

# Date Navigation

`SfCalendar` control provides option to navigate through items either programmatically or by using gesture.

## Programmatic Navigation 

By using the following methods, we can navigate the months or year in `SfCalendar` with programmatically without applying gesture.

1. Forward

2. Backward

### Forward

By default, the date can be navigated to next view using touch gesture and swiping the control in right to left direction. The view can also be changed programmatically using [Forward](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~Forward.html) method available in `SfCalendar`. It will move to next month,next year,next period of decade years,next period of century years based on the `ViewMode`.

{% tabs %}

{% highlight c# %}

	calendar.Forward();

{% endhighlight %}

{% endtabs %}

N> It can be navigated until it reaches the MaxDate.

### Backward

By default, the date can be navigated to previous view using touch gesture and swiping the control in left to right direction. The view can also be changed programmatically using [Backward](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~Backward.html) method available in `SfCalendar`. It will move to previous month,previous year,previous period of decade years,previous period century years based on the `ViewMode`.

{% tabs %}

{% highlight c# %}

	calendar.Backward();

{% endhighlight %}

{% endtabs %}

N> It can be navigated until it reaches the MinDate.

### Move to Date 

Visible dates can be moved to specific date using [MoveToDate](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~MoveToDate.html) property available in `SfCalendar`. it will move to any specific month,year,decade,century view based on the `ViewMode`.

N>  The specified date should lie between MinDate and MaxDate, if the specified date is greater than MaxDate then the view will be moved to MaxDate and if the specified date is lesser than the MinDate then the view will be moved to MinDate.

{% tabs %}

{% highlight c# %}

SfCalendar calendar = new SfCalendar();
calendar.MoveToDate = new DateTime(2017,5,5);
this.Content = calendar;
	
{% endhighlight %}

{% endtabs %}

### Navigation Direction

You can navigate the calendar `MonthView`, `YearView`, `DecadeView` and `CenturyView` either `Vertical` or `Horizontal` directions by setting the [NavigationDirection](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~NavigationDirection.html).

{% tabs %}

{% highlight c# %}

SfCalendar calendar = new SfCalendar();
Calendar.NavigationDirection = NavigationDirection.Vertical;

{% endhighlight %}

{% endtabs %}

![YearView Navigation in Xamarin.Forms Calendar ](images/Xamarin.forms-Calendar-NavigationDirection.png)