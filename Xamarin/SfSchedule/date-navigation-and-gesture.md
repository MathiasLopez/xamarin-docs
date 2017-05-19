﻿# Date Navigations
## Enabling Navigation 
By default, Schedule views can be moved backwards and forwards using touch swipe gesture. This navigation gesture can be enabled or disabled by setting [EnableNavigation](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~EnableNavigation.html) property of `SfSchedule`. By default, it is enabled.

{% tabs %}   
{% highlight xaml %} 

        <schedule:SfSchedule EnableNavigation="False"/>
{% endhighlight %}   
{% highlight c# %} 

         //disabling navigation gesture
           schedule.EnableNavigation = false;

{% endhighlight %}   
{% endtabs %}  

## Programmatically change to specific dates 
Visible dates can be moved to specific date using [NavigateTo](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~NavigateTo.html) method and [MoveToDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~MoveToDate.html) property available in SfSchedule. It will move to any specific date if the schedule view is Day View, similarly it will move to the specific week if it is week view and to specific month if it is month view

{% tabs %}   
{% highlight c# %} 

            //using NavigateTo

            DateTime currentDate = DateTime.Now;
            DateTime SpecificDate = new DateTime(currentDate.Year - 5,                    currentDate.Month - 3, currentDate.Day, 0, 0, 0);
            Schedule.NavigateTo(SpecificDate);

            //using MoveToDate
            DateTime currentDate = DateTime.Now;
            DateTime SpecificDate = new DateTime(currentDate.Year - 5,                    currentDate.Month - 3, currentDate.Day, 0, 0, 0);
            Schedule.MoveToDate = SpecificDate;

{% endhighlight %}   
{% endtabs %}  

## Programmatically change to adjacent dates.
By default the date can be navigated to next and previous view using touch gesture, by swiping the control in right to left and right to left direction. The view can be also changed programmatically using [Forward](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~Forward.html) and [Backward](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~Backward.html) method available in SfSchedule. 

*  	Forward
*	Backward

### Forward
You can use the `Forward` method for viewing the next immediate visible dates in the SfSchedule. It will move to next month if the schedule view is month, similarly it will move to next week for week view and next day for day view.

{% tabs %}   
{% highlight c# %} 

          //Viewing next immediate visible dates
            schedule.Forward();

{% endhighlight %}   
{% endtabs %}  

### Backward
You can use the `Backward` method for viewing the previous immediate visible dates in the SfSchedule. It will move to previous month if the schedule view is month, similarly it will move to previous week for week view and previous day for day view.
{% tabs %}   
{% highlight c# %} 

           //Viewing previous immediate visible dates
            schedule.Backward();


{% endhighlight %}   
{% endtabs %} 

## Range for visible dates
Visible dates can be restricted between certain range of dates, using [MinDisplayDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~MinDisplayDate.html)  and [MaxDisplayDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~MaxDisplayDate.html)  property in `SfSchedule`. It is applicable in all the schedule views.

### Minimum Display Date
`MinDisplayDate` will restrict date navigations features of `Backward`, `MoveToDate` and also can’t swipe the control using touch gesture beyond the min max date range. Thus, Inline and selection feature in month view will works only within the min max date range.

{% tabs %}   
{% highlight c# %} 

             int monthRange = 2; DateTime currentDate = DateTime.Now;
            //setting minimum display date
            DateTime minDate = new DateTime(currentDate.Year, currentDate.Month -         monthRange, currentDate.Day, 10, 0, 0);
            schedule.MinDisplayDate = minDate;

{% endhighlight %}   
{% endtabs %} 
### Maximum Display Date
`MaxDisplayDate` will restrict date navigations features of `Forward`, `MoveToDate` and also can’t swipe the control using touch gesture beyond the max date range. Thus, Inline and selection in month view will works only within the max date range.

{% tabs %}   
{% highlight c# %} 

            int monthRange = 2; DateTime currentDate = DateTime.Now;
            //setting maximum display date
            DateTime maxDate = new DateTime(currentDate.Year, currentDate.Month +         monthRange, currentDate.Day, 10, 0, 0);
            schedule.MaxDisplayDate = maxDate


{% endhighlight %}   
{% endtabs %} 


