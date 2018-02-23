---

layout: post
title: Customize the Schedule WorkWeekView at SfSchedule control for Xamarin.Forms
description: Learn how to Customize the schedule WorkWeekView in SfSchedule control
platform: xamarin.Forms
control: SfSchedule
documentation: ug

---


# WorkWeekView

WorkWeekView is to view only working days of a particular week. By default, Saturday and Sunday are the non-working days. You can be customize it with any days of a Week. Appointments arranged in timeslots based on its duration with respective day of the week.


## ViewHeader Appearance
You can customize the default appearance of view header in [WorkWeekView](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleView.html) by using [ViewHeaderStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderStyle.html) property of [SfSchedule](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule.html).

{% tabs %}
{% highlight c# %}

            //Create new instance of Schedule
			SfSchedule schedule = new SfSchedule();
			schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Customize the schedule view header
			ViewHeaderStyle viewHeaderStyle = new ViewHeaderStyle();
			viewHeaderStyle.BackgroundColor = Color.FromHex("#009688");
			viewHeaderStyle.DayTextColor = Color.FromHex("#FFFFFF");
			viewHeaderStyle.DateTextColor = Color.FromHex("#FFFFFF");
			viewHeaderStyle.DayTextStyle = Font.OfSize("Arial", 15);
			viewHeaderStyle.DateTextStyle = Font.OfSize("Arial", 15);
			schedule.ViewHeaderStyle = viewHeaderStyle;
			
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView ="WorkWeekView">
     <schedule:SfSchedule.ViewHeaderStyle>
         <schedule:ViewHeaderStyle
            BackgroundColor="#009688" 
            DayTextColor="#FFFFFF" 
            DateTextColor="#FFFFFF" 
            DayTextStyle="Arial,15" 
            DateTextStyle="Arial,15">
         </schedule:ViewHeaderStyle>
      </schedule:SfSchedule.ViewHeaderStyle>
    </schedule:SfSchedule>

{% endhighlight %}
{% endtabs %} 

![](daymodule_images/viewheaderappearance_workweek.png)

>**Note**:  FontAttributes and FontFamily are native to the platform. Custom font and the font which are not available in the specified platform will not be applied.

You can customize the height of the ViewHeader in `WeekView` by setting [ViewHeaderHeight](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ViewHeaderHeight.html) property of `SfSchedule`.

{% tabs %} 
{% highlight C# %}

        schedule.ScheduleView = ScheduleView.WorkWeekView;
		schedule.ViewHeaderHeight = 50;
			
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView ="WorkWeekView" ViewHeaderHeight="50" />
           
{% endhighlight %}
{% endtabs %}

![](daymodule_images/viewheaderheight_workweek.png)

## Change Time Interval
You can customize the interval of timeslots in `WorkWeekView` by setting [TimeInterval](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~TimeInterval.html)  property of `SfSchedule`.

{% tabs %}
{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WorkWeekView;
	schedule.TimeInterval = 120;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView" TimeInterval="120"/>  
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/timeinterval_workweek.png)

>**Note:**

If you modify the `TimeInterval` value (in minutes), you need to change the time labels format by setting the `TimeFormat` value as "hh:mm". By default, TimeFormat value is `"hh a"`. You can refer [here](https://help.syncfusion.com/xamarin/sfschedule/workweekview#time-label-formatting) for changing TimeFormat value.

## Change Time Interval Height
You can customize the interval height of timeslots in `WorkWeekView` by setting [TimeIntervalHeight](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~TimeIntervalHeight.html)  property of `SfSchedule`.

{% tabs %}
{% highlight C# %}

schedule.ScheduleView = ScheduleView.WorkWeekView;
schedule.TimeIntervalHeight = 180;
{% endhighlight %}
{% highlight XAML %}

<schedule:SfSchedule  x:Name="schedule"  ScheduleView="WorkWeekView" TimeIntervalHeight="180"/>
{% endhighlight %}
{% endtabs %}

![](daymodule_images/workweekview_height.png)

## Change Working hours

Working hours in `WorkWeekView` of Schedule control will be differentiated with non-working hours by separate color. By default, working hours will be between 09 to 18. You can customize the working hours by setting [WorkStartHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~WorkStartHour.html) and [WorkEndHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~WorkEndHour.html) properties of [WorkWeekViewSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~WorkWeekViewSettings.html).

{% tabs %} 
{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WorkWeekView;
	//Create new instance of WorkWeekViewSettings
	WorkWeekViewSettings workWeekViewSettings = new WorkWeekViewSettings();
	workWeekViewSettings.WorkStartHour = 10;
	workWeekViewSettings.WorkEndHour = 18;
	schedule.WorkWeekViewSettings = workWeekViewSettings;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
       <schedule:SfSchedule.WorkWeekViewSettings>
            <!--setting working hours properties -->
             <schedule:WorkWeekViewSettings 
                WorkStartHour="10"
				WorkEndHour="18">
             </schedule:WorkWeekViewSettings>
        </schedule:SfSchedule.WorkWeekViewSettings>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %}

![](daymodule_images/changeworkinghours_workweek.png)

>**Note**:
	`WorkStartHour` and `WorkEndHour` should be in integer value to represent hours.

## Changing StartHour and EndHour

Default value for [StartHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~StartHour.html) and [EndHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~EndHour.html) value is 0 to 24 to show all the time slots in `WorkWeekView`. You need to set [StartHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~StartHour.html) and [EndHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~EndHour.html) property of 'WorkWeekView', to show only the required time duration for end users.

{% tabs %} 
{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WorkWeekView;
	//Create new instance of WorkWeekViewSettings
	WorkWeekViewSettings workWeekViewSettings = new WorkWeekViewSettings();
	workWeekViewSettings.StartHour = 08;
	workWeekViewSettings.EndHour = 15;
	schedule.WorkWeekViewSettings = workWeekViewSettings;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
       <schedule:SfSchedule.WorkWeekViewSettings>
            <!--setting working hours properties -->
             <schedule:WorkWeekViewSettings 
			 StartHour =”08” 
			 EndHour =”15”>
             </schedule:WorkWeekViewSettings>
        </schedule:SfSchedule.WorkWeekViewSettings>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %}

![](daymodule_images/changestartendhour_workweek.png)

>**Note**:
* `StartHour` and `EndHour` should be in integer value to represent hours.
* `StartHour` must be greater than or equal to 0 and `EndHour` must be lesser than or equal to 24, otherwise `InvalidDataException` will be thrown.
* `EndHour` value must be greater than `StartHour`, otherwise `InvalidDataException` will be thrown.
* Schedule UI such as Appointments and NonAccessibleBlocks which does not fall within the `StartHour` and `EndHour` will not be visible and if it falls partially, it will be clipped.

## Timeslot Appearance
You can customize the appearance of timeslots in `WeekView`.

 * [Timeslot customization in Work hours](#timeslot-customization-in-work-hours)
* [Timeslot customization in Non Working hours](#timeslot-customization-in-non-working-hours)

### Timeslot customization in Work hours

You can customize the appearance of the working hour timeslots by its color using[TimeSlotColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~TimeSlotColor.html), [TimeSlotBorderColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~TimeSlotBorderColor.html), [VerticalLineStrokeWidth](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~VerticalLineStrokeWidth.html),  [VerticalLineColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~VerticalLineColor.html) and  [TimeSlotBorderStrokeWidth](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~TimeSlotBorderStrokeWidth.html) properties of `WorkWeekViewSettings`.

{% tabs %}
{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Create new instance of WorkWeekViewSettings
			WorkWeekViewSettings workWeekViewSettings = new WorkWeekViewSettings();
			workWeekViewSettings.TimeSlotBorderColor = Color.Aqua;
			workWeekViewSettings.VerticalLineColor = Color.Blue;
			workWeekViewSettings.TimeSlotColor = Color.Yellow;
			workWeekViewSettings.TimeSlotBorderStrokeWidth = 5;
			workWeekViewSettings.VerticalLineStrokeWidth = 5;
			schedule.WorkWeekViewSettings = workWeekViewSettings;
{% endhighlight %}
{% highlight XAML %}

     <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
     <schedule:SfSchedule.WorkWeekViewSettings>
      <!--setting work week view settings properties -->
        <schedule:WorkWeekViewSettings
          TimeSlotColor="Yellow"
          TimeSlotBorderColor="Aqua" 
          TimeSlotBorderStrokeWidth="5"
          VerticalLineStrokeWidth="5" 
          VerticalLineColor="Blue">
       </schedule:WorkWeekViewSettings>
     </schedule:SfSchedule.WorkWeekViewSettings>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/timeslotappearance_workweek.png)

### Timeslot customization in Non Working hours

You can customize the appearance of the non-working hour timeslots by its color using [NonWorkingHoursTimeSlotBorderColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~NonWorkingHoursTimeSlotBorderColor.html),[NonWorkingHoursTimeSlotColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~NonWorkingHoursTimeSlotColor.html),`VerticalLineStrokeWidth`, `VerticalLineColor` and `TimeSlotBorderStrokeWidth` properties of `WorkWeekViewSettings`.

{% tabs %}
{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Create new instance of WorkWeekViewSettings
			WorkWeekViewSettings workWeekViewSettings = new WorkWeekViewSettings();
			workWeekViewSettings.NonWorkingHoursTimeSlotBorderColor = Color.Aqua;
			workWeekViewSettings.VerticalLineColor = Color.Blue;
			workWeekViewSettings.NonWorkingHoursTimeSlotColor = Color.Yellow;
			workWeekViewSettings.TimeSlotBorderStrokeWidth = 5;
			workWeekViewSettings.VerticalLineStrokeWidth = 5;
			schedule.WorkWeekViewSettings = workWeekViewSettings;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
     <schedule:SfSchedule.WorkWeekViewSettings>
      <!--setting work week view settings properties -->
        <schedule:WorkWeekViewSettings
           NonWorkingHoursTimeSlotColor="Yellow"
           NonWorkingHoursTimeSlotBorderColor="Aqua" 
           TimeSlotBorderStrokeWidth="5"
           VerticalLineStrokeWidth="5" 
           VerticalLineColor="Blue">
        </schedule:WorkWeekViewSettings>
     </schedule:SfSchedule.WorkWeekViewSettings>
    </schedule:SfSchedule> 
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/nonworkinghours_workweek.png)

>**Note**:
` TimeSlotBorderStrokeWidth`and ` VerticalLineStrokeWidth` properties are common to both Working hours and Non-Working hour time slot customization.

## Non-Accessible timeslots

You can restrict or allocate certain timeslot as Non-accessible blocks by using [NonAccessibleBlocks](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~NonAccessibleBlocks.html) of `WorkWeekViewSettings` so that you can allocate those timeslots for predefined events/activities like Lunch hour.

{% tabs %}
{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Create new instance of NonAccessibleBlock
			NonAccessibleBlock nonAccessibleBlock = new NonAccessibleBlock();
			//Create new instance of NonAccessibleBlocksCollection
			NonAccessibleBlocksCollection nonAccessibleBlocksCollection = new NonAccessibleBlocksCollection();
			WorkWeekViewSettings workWeekViewSettings = new WorkWeekViewSettings();
			nonAccessibleBlock.StartTime = 13;
			nonAccessibleBlock.EndTime = 14;
			nonAccessibleBlock.Text = "LUNCH";
			nonAccessibleBlock.Color = Color.Black;
			nonAccessibleBlocksCollection.Add(nonAccessibleBlock);
			workWeekViewSettings.NonAccessibleBlocks = nonAccessibleBlocksCollection;
			schedule.WorkWeekViewSettings = workWeekViewSettings;
{% endhighlight %}

{% highlight XAML %}

        <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
            <!--setting non-accessing blocks-->
            <schedule:SfSchedule.WorkWeekViewSettings>
                <schedule:WorkWeekViewSettings>
                    <schedule:WorkWeekViewSettings.NonAccessibleBlocks>
                        <schedule:NonAccessibleBlock 
                            StartTime="13" 
			        EndTime="14" 
				 Text="LUNCH" 
				 Color="Black" />
                    </schedule:WorkWeekViewSettings.NonAccessibleBlocks>
                </schedule:WorkWeekViewSettings>
            </schedule:SfSchedule.WorkWeekViewSettings>
        </schedule:SfSchedule> 
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/nonaccessibleblock_workweek.png)

>**Note**:
Selection and related events will not be working in this blocks.

## Change first day of week
By default, schedule control will be rendered with Sunday as the first day of the week, it can be customized to any day of the week by using[FirstDayOfWeek](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~FirstDayOfWeek.html) property of `SfSchedule`.

{% tabs %}
{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WorkWeekView;
	schedule.FirstDayOfWeek = 3;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView" FirstDayOfWeek="3"/>
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/firstdayofweek_workweek.png)

## Time Label Formatting

You can customize the format for the labels which are mentioning the time, by setting [TimeFormat](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekLabelSettings~TimeFormat.html) property of [WorkWeekLabelSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekViewSettings~WorkWeekLabelSettings.html) in `WorkWeekViewSettings`.


{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			WorkWeekViewSettings workweekViewSettings = new WorkWeekViewSettings();
			WorkWeekLabelSettings workWeekLabelSettings = new WorkWeekLabelSettings();
			workWeekLabelSettings.TimeFormat = "hh mm";
			workweekViewSettings.WorkWeekLabelSettings = workWeekLabelSettings;
			schedule.WorkWeekViewSettings = workweekViewSettings;
{% endhighlight %}

![](daymodule_images/timelabelformat_workweek.png)

## Time Label Appearance

You can customize the color for the labels which are mentioning the time, by setting [TimeLabelColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WorkWeekLabelSettings~TimeLabelColor.html) property of `WorkWeekLabelSettings` in `WorkWeekViewSettings`.


{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Create new instance of WorkWeekViewSettings
			WorkWeekViewSettings workWeekViewSettings = new WorkWeekViewSettings();
			//Create new instance of WorkWeekLabelSettings
			WorkWeekLabelSettings workWeekLabelSettings = new WorkWeekLabelSettings();
			workWeekLabelSettings.TimeLabelColor = Color.Blue;
			workWeekViewSettings.WorkWeekLabelSettings = workWeekLabelSettings;
			schedule.WorkWeekViewSettings = workWeekViewSettings;
{% endhighlight %}

![](daymodule_images/timelabelappearance_workweek.png)

## Selection
You can customize the default appearance of selection UI in the timeslots.

* [Selection customization using style](#selection-customization-using-style)
* [Selection customization using custom View](#selection-customization-using-custom-view)

### Selection customization using style
You can customize the timeslot selection by using [SelectionStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectionStyle.html) property of `SfSchedule`.

{% tabs %}
{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Create new instance of SelectionStyle 
			SelectionStyle selectionStyle = new SelectionStyle();
			selectionStyle.BackgroundColor = Color.Blue;
			selectionStyle.BorderColor = Color.Black;
			selectionStyle.BorderThickness = 5;
			selectionStyle.BorderCornerRadius = 5;
			schedule.SelectionStyle = selectionStyle;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
            <schedule:SfSchedule.SelectionStyle>
                <schedule:SelectionStyle 
                   BackgroundColor="Blue" 
                   BorderColor="Black" 
                   BorderThickness="5" 
                   BorderCornerRadius="5">
                </schedule:SelectionStyle>
            </schedule:SfSchedule.SelectionStyle>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/selectionstyle_workweek.png)

### Selection customization using custom View
You can replace the default selection UI with your custom view by setting [SelectionView](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectionView.html) property of `SfSchedule`.

{% tabs %}
{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WorkWeekView;
			//Add the CustomView 
			Button customView = new Button();
			customView.Text = "+NewEvent";
			customView.BackgroundColor = Color.FromHex("#FF9800");
			customView.TextColor = Color.White;
			schedule.SelectionView = customView;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView">
     <schedule:SfSchedule.SelectionView>
          <Button
              BackgroundColor="#FF9800" 
		 Text="+NewEvent" 
		 TextColor="White"/>
      </schedule:SfSchedule.SelectionView>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %} 

![](daymodule_images/selectioncustomview_workweek.png)

### Programmatic selection
You can programmatically select the specific timeslot by setting corresponding date and time value to [SelectedDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectedDate.html) property of `SfSchedule`. By default, it is null.

{% highlight C# %}

    // Setting a date and time to select
    schedule.SelectedDate = new DateTime(2017, 10, 04, 10, 0, 0);

{% endhighlight %}

You can clear the selection by setting [SelectedDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectedDate.html) as null.

{% highlight C# %}

    // Setting null value to deselect
    schedule.SelectedDate = null;

{% endhighlight %}

You can download the entire source code of this demo for Xamarin.Forms from here [Date_Selection](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Date_Selection1072247797.zip)

>**Note**:
* `SfSchedule` does not support multiple selection.
* `SfSchedule` supports two-way binding of `SelectedDate` property.

![](daymodule_images/selection_WorkWeek.png)
