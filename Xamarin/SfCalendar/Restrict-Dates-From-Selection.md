---
layout: post
title: Blackout dates | SfCalendar | Xamarin.Forms | Syncfusion
description: Learn how to set min and max date in calendar
platform: Xamarin
control: Calendar
documentation: ug
---

# Restrict Dates From Selection

Dates can be restricted or a collection of dates can be blacked out in `SfCalendar` Control.

## Range of Min / Max Dates

Visible dates can be restricted between certain range of dates using [MinDate](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~MinDate.html) and [MaxDate](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~MaxDate.html) properties available in `SfCalendar` control. It is applicable in all the calendar views.

The inline feature in month view will work only within the min max date range.

Beyond the min max date range, following restrictions will be applied.

* Date navigation features of move to date will be restricted.
* Cannot swipe the control using touch gesture.
* Selection does not work for month view.
* The tapped delegates will not be triggered while tapped on the MonthCell.
    

{% highlight c# %}
	
SfCalendar calendar = new SfCalendar();    
DateTime minDate=new DateTime(2015,1,1);
calendar.MinDate=minDate;
DateTime maxDate=new DateTime(2040,12,12);
calendar.MaxDate=maxDate;
this.Content = calendar;
	
{% endhighlight %}

## Blackout Dates

In `SfCalendar`, [BlackoutDates](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~BlackoutDates.html) refers the disabled dates that restrict the user from selecting it. These dates will be marked with slanted Stripes.

The BlackoutDays can be achieved in two ways.

A date collection can be provided to set the [BlackoutDates](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~BlackoutDates.html). This is useful when one wants to block dates where holidays or any other events occur.

By invoking the [AddDatesInPast](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~AddDatesInPast.html) method, all past dates will be blacked out till current date.

{% highlight c# %}
	
SfCalendar calendar = new SfCalendar();        
List<DateTime> black_dates = new List<DateTime>();
black_dates.Add (new DateTime(2016,1,20));
black_dates.Add (new DateTime(2016,1,21));
black_dates.Add (new DateTime(2016,1,22));
black_dates.Add (new DateTime(2016,1,23));
black_dates.Add (new DateTime(2016,1,24));
calendar.BlackoutDates= black_dates ;
this.Content = calendar;
	
{%  endhighlight %}
	
![BlackoutDate support in Xamarin.Forms Calendar](images/xamarin.forms-calendar-Blackout.jpg)

### Customize the blackout dates Color
You can customize the color of [BlackoutDates](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~BlackoutDates.html) in month view mode using the [BlackOutColor](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.MonthViewSettings~BlackoutColor.html) property of [MonthViewSettings](https://help.syncfusion.com/cr/xamarin/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.MonthViewSettings.html).

{% tabs %}
{% highlight xaml %}
<syncfusion:SfCalendar x:Name="calendar">
<syncfusion:SfCalendar.MonthViewSettings>
<syncfusion:MonthViewSettings BlackOutColor="Red">
</syncfusion:SfCalendar.MonthViewSettings>
</syncfusion:SfCalendar>
{% endhighlight %}
{% highlight c# %}
SfCalendar calendar = new SfCalendar(); 
MonthViewSettings monthViewSettings = new MonthViewSettings();
monthViewSettings.BlackOutColor = Color.Red;
calendar.MonthViewSettings = monthViewSettings;
this.Content = calendar;
{% endhighlight %}
{% endtabs %}

![BlackoutDate color support in Xamarin.Forms Calendar](images/xamarin.forms-calendar-Blackout-color.jpg)

### Rendering Blackout dates using MonthCellLoaded event
Using[OnMonthCellLoaded](https://help.syncfusion.com/cr/cref_files/xamarin/sfcalendar/Syncfusion.SfCalendar.XForms~Syncfusion.SfCalendar.XForms.SfCalendar~OnMonthCellLoaded_EV.html) event you can render the black out dates.

{% tabs %}
{% highlight c# %}

private void Calendar_OnMonthCellLoaded(object sender, EventArgs e)
{
	List<DateTime> blackoutDates = new List<DateTime>();
	var dayOfWeek = e.Date.DayOfWeek;
    if(dayOfWeek==DayOfWeek.Saturday || dayOfWeek == DayOfWeek.Sunday)
    {
		blackoutDates.Add(e.Date);
		calendar.BlackoutDates = blackoutDates;
	}
}

{% endhighlight %}
{% endtabs %}