---
layout: post
title: Date Navigation and Gestures with Syncfusion Calendar control for Xamarin.Forms
description: Learn the complete navigation and gestures support
platform: Xamarin
control: Calendar
documentation: ug
---

# Date Navigation

SfCalendar control provides option to navigate through items either programmatically or by using gesture.

## Animation on Transition

Month navigation can be animated by using `TransitionMode` property in SfCalendar. The following types of Transition modes are available here,

1. Scroll

2. Card

3. Reveal

4. Float

N> By default those navigations are performed along with `Scroll` animation

{% tabs %}

{% highlight xaml %}

<syncfusion:SfCalendar  x:Name="calendar"  TransitionMode="Float"/>

{% endhighlight %}

{% highlight c# %}
	
SfCalendar calendar = new SfCalendar();

calendar.TransitionMode=TransitionMode.Float;

this.Content = calendar
	
{% endhighlight %}

{% endtabs %}

N> This transitions works only for Month view.

## Programmatic Navigation 

By using the following methods, we can navigate the months or year in SfCalendar with programmatically without applying gesture.

1. Forward

2. Backward

### Forward

By default, the date can be navigated to next view using touch gesture and swiping the control in right to left direction. The view can also be changed programmatically using `Forward` method available in SfCalendar. It will move to next month, if the view mode is month or it will move to next Year,if the view mode is year.

{% highlight c# %}

	DependencyService.Get<ICalendarDirection>().Forward();

{% endhighlight %}

N> It can be navigated until it reaches the MaxDate.

### Backward

By default, the date can be navigated to previous view using touch gesture and swiping the control in left to right direction. The view can also be changed programmatically using `Backward` method available in SfCalendar. It will move to previous month, if the view mode is month or it will move to previous year, if the view mode is year view.

{% highlight c# %}

	DependencyService.Get<ICalendarDirection>().Backward();

{% endhighlight %}

N> It can be navigated until it reaches the MinDate.

### Move to Date 

Visible dates can be moved to specific date using `MoveToDate` property available in SfCalendar. It will move to any specific month if the view mode is month view or move to year if it is a year view.

N>  The specified date should lie between MinDate and MaxDate, if the specified date is greater than MaxDate then the view will be moved to MaxDate and if the specified date is lesser than the MinDate then the view will be moved to MinDate.


{% highlight c# %}

SfCalendar calendar = new SfCalendar();

calendar.MoveToDate = new DateTime(2017,5,5);

this.Content = calendar;
	
{% endhighlight %}

