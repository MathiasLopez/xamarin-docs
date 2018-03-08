---
layout: post
title: Accessing View modes in Syncfusion Calendar control for Xamarin.Forms
description: Learn how to set month view and year view in Calendar
platform: Xamarin
control: Calendar
documentation: ug
---

# View of SfCalendar

SfCalendar control provides two types of views to display dates such as month view and year view. It can be assigned to the SfCalendar control by using `ViewMode` property.Based on the user’s preference SfCalendar can be viewed in any of the available two types.

N> By default SfCalendar control is assigned with month view. 

## MonthView

This displays entire dates of a particular month, by default current month will be displayed on loading. The current date is provided with separate color different from the rest of the dates color in a month. The events availability will be denoted within the cell based on its duration.

The dates in month view can be selected by three ways such as single, multiple and range which can be modified using `SelectionMode`

### Customization of SfCalendar's dates in MonthView

We can customize the calendar view in monthView mode by using `MonthViewSettings`. 

* Current day text color can be modified using `TodayTextColor`.

* It also has API `MonthLabelSettings` to change the date text size, day text size and format options.

* The background color of the inline view can be modified using `InlineBackgroundColor` property.

* The BlackOutDate color can be modified with `BlackOutColor` property.

{% highlight c# %}
	
SfCalendar calendar = new SfCalendar();    

MonthLabelSettings labelSettings = new MonthLabelSettings();
labelSettings.DateFormat = "dd";
labelSettings.DayLabelSize = 20;
labelSettings.DayFormat = "EEE";
labelSettings.DateLabelSize = 12;

MonthViewSettings monthViewSettings = new MonthViewSettings();
monthViewSettings.CurrentMonthBackgroundColor = Color.FromHex("#800080");
monthViewSettings.CurrentMonthTextColor = Color.FromHex("#ffffff");
monthViewSettings.PreviousMonthBackgroundColor = Color.FromHex("#9895F0");
monthViewSettings.PreviousMonthTextColor = Color.FromHex("#000000");
monthViewSettings.DateSelectionColor = Color.FromHex("#ffffff");
monthViewSettings.SelectedDayTextColor = Color.FromHex("#000000");

monthViewSettings.MonthLabelSettings = labelSettings;
calendar.MonthViewSettings = monthViewSettings;

this.Content = calendar;
	
{% endhighlight %}

![](images/monthviewset.png)


N> Similar way there are many settings available to modify Text and Background colors of month view in `MonthViewSettings` class.

## YearView

This displays entire dates/month of a particular year, by default current year will be displayed on loading. The Years can be changed by swiping back and forth or `Forward` and `Backward` methods. The Months can be navigated quickly by selecting on the particular month in year view.

{% tabs %}

{% highlight xaml %}

<syncfusion:SfCalendar  x:Name="calendar" ViewMode="YearView"/>

{% endhighlight %}

{% highlight c# %}

SfCalendar calendar = new SfCalendar();

calendar.ViewMode=ViewMode.YearView;

this.Content = calendar;
 
{% endhighlight %}

{% endtabs %}
 
![](images/yearviewset.png)

### Customization of SfCalendar's dates in YearView

We can customize the calendar view in yearView mode by using `YearViewSettings`. 

*  date text color can be modified using `DateTextColor`.

* We can also customize the header, monthLayout in yearView 's textColor and background color.

{% highlight c# %}
	
SfCalendar calendar = new SfCalendar();    
    
YearViewSettings yearViewSettings = new YearViewSettings();
yearViewSettings.BackgroundColor = Color.FromHex("#ffe4b5");
yearViewSettings.DateTextColor = Color.FromHex("#E6E6FA");
yearViewSettings.HeaderBackground = Color.FromHex("#8B4513");
yearViewSettings.YearHeaderTextColor = Color.FromHex("#FFFFFF");

calendar.YearViewSettings = yearViewSettings;
this.Content = calendar;

{% endhighlight %}


