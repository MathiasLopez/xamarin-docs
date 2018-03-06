---

layout: post
title: Customize the Schedule WeekView at SfSchedule control for Xamarin.Forms
description: Learn how to Customize the schedule WeekView in SfSchedule control
platform: xamarin.Forms
control: SfSchedule
documentation: ug

---


# WeekView

WeekView is to view all days of a particular week. Appointments will be arranged based on the dates on the week in respective timeslots.

## ViewHeader Appearance
You can customize the default appearance of view header in [WeekView](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleView.html) by using [ViewHeaderStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderStyle.html) property of [SfSchedule](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule.html).

{% tabs %}

{% highlight c# %}

            //Create new instance of Schedule
			SfSchedule schedule = new SfSchedule();
			schedule.ScheduleView = ScheduleView.WeekView;
			//Customize the schedule view header
			ViewHeaderStyle viewHeaderStyle = new ViewHeaderStyle();
			viewHeaderStyle.BackgroundColor = Color.FromHex("#009688");
			viewHeaderStyle.DayTextColor = Color.FromHex("#FFFFFF");
			viewHeaderStyle.DateTextColor = Color.FromHex("#FFFFFF");
			viewHeaderStyle.DayFontFamily = Device.OnPlatform("Lobster-Regular", "Lobster-Regular.ttf", "Assets/Lobster-Regular.ttf#Lobster");
			viewHeaderStyle.DateFontFamily = Device.OnPlatform("Lobster-Regular", "Lobster-Regular.ttf", "Assets/Lobster-Regular.ttf#Lobster");
			viewHeaderStyle.DayFontSize = 15;
			viewHeaderStyle.DateFontSize = 15;
			viewHeaderStyle.DayFontAttributes = FontAttributes.Bold;
			viewHeaderStyle.DateFontAttributes = FontAttributes.Bold;
			schedule.ViewHeaderStyle = viewHeaderStyle;
			
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView ="WeekView">
     <schedule:SfSchedule.ViewHeaderStyle>
         <schedule:ViewHeaderStyle
             BackgroundColor="#009688" 
             DayTextColor="#FFFFFF" 
             DateTextColor="#FFFFFF" 
             DayFontSize="15"
			 DateFontSize="15"
			 DayFontAttributes="Bold"
			 DateFontAttributes="Bold">
	     <schedule:ViewHeaderStyle.DayFontFamily>
                 <OnPlatform x:TypeArguments="x:String" iOS="Lobster-Regular" Android="Lobster-Regular.ttf" WinPhone="Assets/Lobster-Regular.ttf#Lobster" />
         </schedule:ViewHeaderStyle.DayFontFamily>
		 <schedule:ViewHeaderStyle.DateFontFamily>
                 <OnPlatform x:TypeArguments="x:String" iOS="Lobster-Regular" Android="Lobster-Regular.ttf" WinPhone="Assets/Lobster-Regular.ttf#Lobster" />
         </schedule:ViewHeaderStyle.DateFontFamily>
        </schedule:ViewHeaderStyle>
    </schedule:SfSchedule.ViewHeaderStyle>
</schedule:SfSchedule> 

{% endhighlight %}
{% endtabs %}

![](daymodule_images/viewheader_appearance_week.png)

>**Note**:  FontAttributes and FontFamily are native to the platform. Custom font and the font which are not available in the specified platform will not be applied.
    
You can customize the height of the ViewHeader in `WeekView` by setting [ViewHeaderHeight](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ViewHeaderHeight.html) property of `SfSchedule`.

{% tabs %}

{% highlight C# %}

        schedule.ScheduleView = ScheduleView.WeekView;
		schedule.ViewHeaderHeight = 50;
			
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView ="WeekView"           ViewHeaderHeight="50" /> 
           
{% endhighlight %}
{% endtabs %}
![](daymodule_images/viewheaderheight_week.png)

### ViewHeader Date Format
We can customize the date and day format of `SfSchedule` ViewHeader by using [DateFormat](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.DayLabelSettings~DateFormat.html) and [DayFormat](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.DayLabelSettings~DayFormat.html) properties of `WeekLabelSettings`

{% tabs %}
{% highlight xaml %}
<schedule:SfSchedule>
    <schedule:SfSchedule.WeekViewSettings>
        <schedule:WeekViewSettings>
            <schedule:WeekViewSettings.WeekLabelSettings>
                <schedule:WeekLabelSettings DateFormat=“dd”>
                    <schedule:WeekLabelSettings.DayFormat>
                        <OnPlatform x:TypeArguments="x:String" iOS="EEEE" Android="EEEE" WinPhone="dddd" />
                    </schedule:WeekLabelSettings.DayFormat>
                </schedule:WeekLabelSettings>
            </schedule:WeekViewSettings.WeekLabelSettings>
        </schedule:WeekViewSettings>
    </schedule:SfSchedule.WeekViewSettings>
</schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
schedule.ScheduleView = ScheduleView.WeekView;
//Creating new instance of WeekViewSettings
WeekViewSettings weekViewSettings = new WeekViewSettings();
//Creating new instance of WeekLabelSettings
WeekLabelSettings weekLabelSettings = new WeekLabelSettings();
//Customizing date format
weekLabelSettings.DateFormat = "dd";
weekLabelSettings.DayFormat = Device.OnPlatform("EEEE", "EEEE", "dddd");
weekViewSettings.WeekLabelSettings = weekLabelSettings;
schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}
{% endtabs %}

![](daymodule_images/DateFormat_Week.png)


### ViewHeader Tapped Event
We can handle single tap action of `ViewHeader` by using [ViewHeaderTapped](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ViewHeaderTapped_EV.html) event of `SfSchedule`. This event will be triggered when ViewHeader is Tapped. This event contains [ViewHeaderTappedEventArgs](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderTappedEventArgs.html) argument which holds [DateTime](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.CellTappedEventArgs~Datetime.html) details in it.

{% tabs %}
{% highlight xaml %}
<schedule:SfSchedule x:Name="schedule"
                                     ScheduleView="WeekView"
                                     ViewHeaderTapped="Handle_ViewHeaderTapped" >
</schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
//Creating  new instance of Schedule
SfSchedule schedule = new SfSchedule();
schedule.ScheduleView = ScheduleView.WeekView;
schedule.ViewHeaderTapped += Handle_ViewHeaderTapped;
{% endhighlight %}
{% endtabs %}

{% highlight c# %}
void Handle_ViewHeaderTapped(object sender, ViewHeaderTappedEventArgs e)
{
var dateTime = e.DateTime;
}
{% endhighlight %}

## Change Time Interval
You can customize the interval of timeslots in `WeekView` by setting [TimeInterval](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~TimeInterval.html)  property of `SfSchedule`.

{% tabs %}

{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WeekView;
	schedule.TimeInterval = 120;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView" TimeInterval="120"/> 
{% endhighlight %}
{% endtabs %}
![](daymodule_images/timeinterval_week.png)


>**Note**:

If you modify the `TimeInterval` value (in minutes), you need to change the time labels format by setting the `TimeFormat` value as "hh:mm". By default, TimeFormat value is `"hh a"`. You can refer [here](https://help.syncfusion.com/xamarin/sfschedule/weekview#time-label-formatting) for changing TimeFormat value.

## Change Time Interval Height
You can customize the interval height of timeslots in `WeekView` by setting [TimeIntervalHeight](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~TimeIntervalHeight.html)  property of `SfSchedule`.

{% tabs %}
{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WeekView;
    schedule.TimeIntervalHeight = 180;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule  x:Name="schedule"  ScheduleView="WeekView" TimeIntervalHeight="180"/>
{% endhighlight %}
{% endtabs %}

![](daymodule_images/weekview_height.png)

## Change Working hours

Working hours in `WeekView` of Schedule control will be differentiated with non-working hours by separate color. By default, working hours will be between 09 to 18. You can customize the working hours by setting [WorkStartHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~WorkStartHour.html) and [WorkEndHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~WorkEndHour.html) properties of   [WeekViewSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~WeekViewSettings.html).

{% tabs %}

{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WeekView;
			//Create new instance of WeekViewSettings
			WeekViewSettings weekViewSettings = new WeekViewSettings();
			weekViewSettings.WorkStartHour = 10;
			weekViewSettings.WorkEndHour = 18;
			schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
         <schedule:SfSchedule.WeekViewSettings>
                <!--setting working hours properties -->
                <schedule:WeekViewSettings 
                     WorkStartHour="10" 
                     WorkEndHour="18">
                </schedule:WeekViewSettings>
          </schedule:SfSchedule.WeekViewSettings>
    </schedule:SfSchedule> 
{% endhighlight %}
{% endtabs %}

![](daymodule_images/changeworkinghours_week.png)

>**Note**:
	`WorkStartHour` and `WorkEndHour` should be in integer value to represent hours.

## Changing StartHour and EndHour

Default value for [StartHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~StartHour.html) and [EndHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~EndHour.html) value is 0 to 24 to show all the time slots in `WeekView`. You need to set [StartHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~StartHour.html) and [EndHour](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~EndHour.html) property of `WeekView`, to show only the required time duration for end users.

{% tabs %}

{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WeekView;
			//Create new instance of WeekViewSettings
			WeekViewSettings weekViewSettings = new WeekViewSettings();
			weekViewSettings.StartHour = 08;
			weekViewSettings.EndHour = 15;
			schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
         <schedule:SfSchedule.WeekViewSettings>
                <!--setting working hours properties -->
                <schedule:WeekViewSettings 
				StartHour="08" 
				EndHour="15">
                </schedule:WeekViewSettings>
          </schedule:SfSchedule.WeekViewSettings>
    </schedule:SfSchedule> 
{% endhighlight %}
{% endtabs %}

![](daymodule_images/changestartendhour_week.png)


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

You can customize the appearance of the working hour timeslots by its color using[TimeSlotColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~TimeSlotColor.html) ,[TimeSlotBorderColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~TimeSlotBorderColor.html), [VerticalLineStrokeWidth](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~VerticalLineStrokeWidth.html), [VerticalLineColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~VerticalLineColor.html) and [TimeSlotBorderStrokeWidth](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~TimeSlotBorderStrokeWidth.html) properties of`WeekViewSettings`.

{% tabs %}

{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WeekView;
			//Create new instance of WeekViewSettings
			WeekViewSettings weekViewSettings = new WeekViewSettings();
			weekViewSettings.TimeSlotBorderColor = Color.Aqua;
			weekViewSettings.VerticalLineColor = Color.Blue;
			weekViewSettings.TimeSlotColor = Color.Yellow;
			weekViewSettings.TimeSlotBorderStrokeWidth = 5;
			weekViewSettings.VerticalLineStrokeWidth = 5;
			schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}
{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
      <schedule:SfSchedule.WeekViewSettings>
        <!--setting week view settings properties -->
         <schedule:WeekViewSettings
             TimeSlotColor="Yellow"
             TimeSlotBorderColor="Aqua" 
             TimeSlotBorderStrokeWidth="5"
             VerticalLineStrokeWidth="5" 
             VerticalLineColor="Blue">
         </schedule:WeekViewSettings>
       </schedule:SfSchedule.WeekViewSettings>
    </schedule:SfSchedule> 
{% endhighlight %}
{% endtabs %}
![](daymodule_images/timeslotappearance_week.png)

### Timeslot customization in Non Working hours

You can customize the appearance of the non-working hour timeslots by its color using [NonWorkingHoursTimeSlotBorderColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~NonWorkingHoursTimeSlotBorderColor.html), [NonWorkingHoursTimeSlotColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~NonWorkingHoursTimeSlotColor.html), `VerticalLineStrokeWidth`, `VerticalLineColor` and `TimeSlotBorderStrokeWidth` properties of `WeekViewSettings`.

{% tabs %}

{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WeekView;
	//Create new instance of WeekViewSettings
	WeekViewSettings weekViewSettings = new WeekViewSettings();
	weekViewSettings.NonWorkingHoursTimeSlotBorderColor = Color.Aqua;
	weekViewSettings.VerticalLineColor = Color.Blue;
	weekViewSettings.NonWorkingHoursTimeSlotColor = Color.Yellow;
	weekViewSettings.TimeSlotBorderStrokeWidth = 5;
	weekViewSettings.VerticalLineStrokeWidth = 5;
	schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
     <schedule:SfSchedule.WeekViewSettings>
      <!--setting week view settings properties -->
        <schedule:WeekViewSettings
            NonWorkingHoursTimeSlotColor="Yellow"
            NonWorkingHoursTimeSlotBorderColor="Aqua" 
            TimeSlotBorderStrokeWidth="5"
            VerticalLineStrokeWidth="5" 
            VerticalLineColor="Blue">
        </schedule:WeekViewSettings>
     </schedule:SfSchedule.WeekViewSettings>
    </schedule:SfSchedule> 
{% endhighlight %}
{% endtabs %}
![](daymodule_images/non-working hours_week.png)

>**Note**:
` TimeSlotBorderStrokeWidth`and ` VerticalLineStrokeWidth` properties are common to both Working hours and Non-Working hour time slot customization.

## Non-Accessible timeslots

You can restrict or allocate certain timeslot as Non-accessible blocks by using[NonAccessibleBlocks](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~NonAccessibleBlocks.html) of `WeekViewSettings` so that you can allocate those timeslots for predefined events/activities like Lunch hour.

{% tabs %}

{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WeekView;
	//Create new instance of NonAccessibleBlock
	NonAccessibleBlock nonAccessibleBlock = new NonAccessibleBlock();
	//Create new instance of NonAccessibleBlocksCollection
	NonAccessibleBlocksCollection nonAccessibleBlocksCollection = new NonAccessibleBlocksCollection();
	WeekViewSettings weekViewSettings = new WeekViewSettings();
	nonAccessibleBlock.StartTime = 13;
	nonAccessibleBlock.EndTime = 14;
	nonAccessibleBlock.Text = "LUNCH";
	nonAccessibleBlock.Color = Color.Black;
	nonAccessibleBlocksCollection.Add(nonAccessibleBlock);
	weekViewSettings.NonAccessibleBlocks = nonAccessibleBlocksCollection;
	schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}

{% highlight XAML %}

        <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
            <!--setting non-accessing blocks-->
            <schedule:SfSchedule.WeekViewSettings>
                <schedule:WeekViewSettings>
                    <schedule:WeekViewSettings.NonAccessibleBlocks>
                        <schedule:NonAccessibleBlock 
                             StartTime="13"
                             EndTime="14"  
                             Text="LUNCH"
                             Color="Black" />
                    </schedule:WeekViewSettings.NonAccessibleBlocks>
                </schedule:WeekViewSettings>
            </schedule:SfSchedule.WeekViewSettings>
        </schedule:SfSchedule>  
{% endhighlight %}
{% endtabs %}
![](daymodule_images/non-accessibleblock_week.png)

>**Note**:
Selection and related events will not be working in this blocks.

## Change first day of week
By default, schedule control will be rendered with Sunday as the first day of the week, it can be customized to any day of the week by using[FirstDayOfWeek](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~FirstDayOfWeek.html) property of `SfSchedule`.

{% tabs %}

{% highlight C# %}

    schedule.ScheduleView = ScheduleView.WeekView;
	schedule.FirstDayOfWeek = 3;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView"        FirstDayOfWeek="3"/>
{% endhighlight %}
{% endtabs %}
![](daymodule_images/firstdayofweek_week.png)

## Time Label Formatting

You can customize the format for the labels which are mentioning the time, by setting [TimeFormat](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekLabelSettings~TimeFormat.html) property of [WeekLabelSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekViewSettings~WeekLabelSettings.html) in `WeekViewSettings`.

{% tabs %}
{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WeekView;
			WeekViewSettings weekViewSettings = new WeekViewSettings();
			WeekLabelSettings weekLabelSettings = new WeekLabelSettings();
			weekLabelSettings.TimeFormat = "hh mm";
			weekViewSettings.WeekLabelSettings = weekLabelSettings;
			schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}
{% endtabs %}
![](daymodule_images/timelabelformat_week.png)

## Time Label Appearance

You can customize the color for the labels which are mentioning the time, by setting [TimeLabelColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekLabelSettings~TimeLabelColor.html) property of `WeekLabelSettings` in `WeekViewSettings`.

{% tabs %}

{% highlight C# %}

           schedule.ScheduleView = ScheduleView.WeekView;
			//Create new instance of WeekViewSettings
			WeekViewSettings weekViewSettings = new WeekViewSettings();
			//Create new instance of WeekLabelSettings
			WeekLabelSettings weekLabelSettings = new WeekLabelSettings();
			weekLabelSettings.TimeLabelColor = Color.Blue;
			weekViewSettings.WeekLabelSettings = weekLabelSettings;
			schedule.WeekViewSettings = weekViewSettings;
{% endhighlight %}
{% endtabs %}
![](daymodule_images/timelabelappearance_week.png)

## Selection
You can customize the default appearance of selection UI in the timeslots.

* [Selection customization using style](#selection-customization-using-style)
* [Selection customization using custom View](#selection-customization-using-custom-view)
* [Programmatic selection](#programmatic-selection)

### Selection customization using style
You can customize the timeslot selection by using [SelectionStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectionStyle.html) property of `SfSchedule`.

{% tabs %}

{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WeekView;
			//Create new instance of SelectionStyle 
			SelectionStyle selectionStyle = new SelectionStyle();
			selectionStyle.BackgroundColor = Color.Blue;
			selectionStyle.BorderColor = Color.Black;
			selectionStyle.BorderThickness = 5;
			selectionStyle.BorderCornerRadius = 5;
			schedule.SelectionStyle = selectionStyle;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
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
![](daymodule_images/selectionstyle_week.png)

### Selection customization using custom View
You can replace the default selection UI with your custom view by setting [SelectionView](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectionView.html) property of `SfSchedule`.

{% tabs %}

{% highlight C# %}

            schedule.ScheduleView = ScheduleView.WeekView;
			//Add the CustomView 
			Button customView = new Button();
			customView.Text = "+NewEvent";
			customView.BackgroundColor = Color.FromHex("#FF9800");
			customView.TextColor = Color.White;
			schedule.SelectionView = customView;
{% endhighlight %}

{% highlight XAML %}

    <schedule:SfSchedule x:Name="schedule" ScheduleView="WeekView">
      <schedule:SfSchedule.SelectionView>
           <Button 
               BackgroundColor="#FF9800" 
               Text="+NewEvent" 
               TextColor="White"/>
      </schedule:SfSchedule.SelectionView>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %}
![](daymodule_images/selectioncustomview_week.png)

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

![](daymodule_images/selection_Week.png)

## Custom Font

For Configuring custom font, please refer [here](https://help.syncfusion.com/xamarin/sfschedule/dayview#custom font)
