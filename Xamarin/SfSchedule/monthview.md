---   
layout: post   
title: MonthView   
description: Overview of MonthView related features
platform: xamarin   
control: SfSchedule   
documentation: ug   
---   
    
# Month View
`MonthView` of `SfSchedule` used to display entire dates of the specific month, current month will be displayed by default initially. Current date color is differentiated with other dates of the current month, also the color differentiation for dates will be applicable for previous and next month dates.

{% tabs %}
{% highlight xaml %}
    <schedule:SfSchedule 
			x:Name="schedule" 
			ScheduleView="MonthView">
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
		//setting schedule view
		schedule.ScheduleView = ScheduleView.MonthView;
{% endhighlight %}
{% endtabs %}

![](monthview_images/monthview.png)

## Month Appointment indicator
In `MonthView`, appointments are not viewed in the month cell instead appointment indicators are drawn. You can customize the number of appointment indicators displayed in month cell using  [AppointmentIndicatorCount](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~AppointmentIndicatorCount.html) property of [MonthViewSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings.html) in `SfSchedule`, by default Appointment indicator count is 3.

{% tabs %}
{% highlight xaml %}
        <schedule:SfSchedule 
                x:Name="schedule"
                ScheduleView="MonthView">
        <schedule:SfSchedule.MonthViewSettings>
            <schedule:MonthViewSettings 
					AppointmentIndicatorCount = "2" >
            </schedule:MonthViewSettings>
        </schedule:SfSchedule.MonthViewSettings>
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
			//creating new instance for MonthViewSettings
			MonthViewSettings monthViewSettings = new MonthViewSettings();
			monthViewSettings.AppointmentIndicatorCount = 2;
			schedule.MonthViewSettings = monthViewSettings;
{% endhighlight %}
{% endtabs %}

>**Notes**: If appointments count are lesser than the AppointmentIndicatorCount value in the particular day, then according to number of appointments available, indicator will be displayed in the month cell.Maximum number of appointment indicators drawn in the month cell is 6 in android and ios platforms. 

![](monthview_images/appointmentindicator.png)

## Month InlineView
You can use [ShowAppointmentsInline](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ShowAppointmentsInline.html) bool property in `SfSchedule` to enable / disable the month inline view, by setting `ShowAppointmentsInline` property as `true` you can view the Appointments in the specific date. 

{% tabs %}
{% highlight xaml %}
        <schedule:SfSchedule 
				x:Name="schedule" 
				ScheduleView="MonthView"
				ShowAppointmentsInline="true">
		</schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
			schedule.ShowAppointmentsInline = true;
{% endhighlight %}
{% endtabs %}

![](monthview_images/appointmentindicator.png)

>**Notes**: If appointments not there in the selected day, Inline view displays the text as "No Events"      

## Month Navigation direction
MonthView of Schedule can be navigated in both horizontal and vertical direction. You can change the direction of navigation through [MonthNavigationDirection](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~MonthNavigationDirection.html) property of [MonthViewSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings.html) in `SfSchedule`, by default Month navigation direction is `Horizontal`.

{% tabs %}
{% highlight xaml %}
    <schedule:SfSchedule 
				x:Name="schedule"
				ScheduleView="MonthView">
        <schedule:SfSchedule.MonthViewSettings>
            <schedule:MonthViewSettings 
						MonthNavigationDirection="Vertical">
            </schedule:MonthViewSettings>
        </schedule:SfSchedule.MonthViewSettings>
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
		//creating new instance for MonthViewSettings
		MonthViewSettings monthViewSettings = new MonthViewSettings();
		//To navigate vertically
		monthViewSettings.MonthNavigationDirection = MonthNavigationDirections.Vertical;
		schedule.MonthViewSettings = monthViewSettings;
{% endhighlight %}
{% endtabs %}

## Restricted days in Month
You can disable the interaction for certain date in Month view by using [BlackoutDates](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~BlackoutDates.html) of [MonthViewSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings.html), using this you can allocate / restrict the specific date for predefined events.

{% tabs %}
{% highlight c# %}
		//creating new instance for MonthViewSettings
		MonthViewSettings monthViewSettings = new MonthViewSettings();
		ObservableCollection<DateTime> blackoutDateCollection = new ObservableCollection<DateTime>();

		DateTime blockedDate1 = DateTime.Now.Date.AddDays(1);
		DateTime blockedDate2 = DateTime.Now.Date.AddDays(2);
		DateTime blockedDate3 = DateTime.Now.Date.AddDays(3);
		DateTime blockedDate4 = DateTime.Now.Date.AddDays(4);
		DateTime blockedDate5 = DateTime.Now.Date.AddDays(5);

		blackoutDateCollection.Add(blockedDate1);
		blackoutDateCollection.Add(blockedDate2);
		blackoutDateCollection.Add(blockedDate3);
		blackoutDateCollection.Add(blockedDate4);
		blackoutDateCollection.Add(blockedDate5);
		monthViewSettings.BlackoutDates = blackoutDateCollection;
		schedule.MonthViewSettings = monthViewSettings;
{% endhighlight %}
{% endtabs %}

![](monthview_images/blackoutdate.png)

## First day of Week in Month
You can set First day of week using [FirstDayOfWeek](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~FirstDayOfWeek.html) property of `SfSchedule`, by default schedule control will rendered with `Sunday` as the first day of the week. 

{% tabs %}
{% highlight xaml %}
    <schedule:SfSchedule 
				x:Name="schedule" 
				FirstDayOfWeek="3"
				ScheduleView="MonthView">
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
		//setting FirstDayOfWeek
		schedule.FirstDayOfWeek = 3; // Tuesday
{% endhighlight %}
{% endtabs %}

![](monthview_images/firstdayofweek.png)

## Week Number of the Year in Month
You can display the Week Number of the year in `MonthView` by setting [ShowWeekNumber](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~ShowWeekNumber.html) property of `MonthViewSettings` as `true`, by default it is `false`.

{% tabs %}
{% highlight xaml %}
    <schedule:SfSchedule 
                x:Name="schedule"
                ScheduleView="MonthView">
        <schedule:SfSchedule.MonthViewSettings>
            <schedule:MonthViewSettings 
						ShowWeekNumber="true">
            </schedule:MonthViewSettings>
        </schedule:SfSchedule.MonthViewSettings>
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
		monthViewSettings.ShowWeekNumber = true;
{% endhighlight %}
{% endtabs %}

![](monthview_images/showweeknumber.png)

## Week Number Appearance
You can customize the Week Number appearance by using [WeekNumberStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~WeekNumberStyle.html) property of `MonthViewSettings`. Week number [BackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekNumberStyle~BackgroundColor.html), [TextColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekNumberStyle~TextColor.html), [TextStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.WeekNumberStyle~TextStyle.html) can be customized using `WeekNumberStyle` properties.

{% tabs %}
{% highlight c# %}
		//creating new instance for WeekNumberStyle
		WeekNumberStyle weekNumberStyle = new WeekNumberStyle();
		weekNumberStyle.TextStyle = Font.OfSize("Arial", 15);
		weekNumberStyle.BackgroundColor = Color.Blue;
		weekNumberStyle.TextColor = Color.White;
		monthViewSettings.WeekNumberStyle = weekNumberStyle;
{% endhighlight %}
{% endtabs %}

![](monthview_images/weeknumberstyle.png)

## Month Label Formatting 
You can change the Format of the Month date and day labels string in the Schedule using [DateFormat](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthLabelSettings~DateFormat.html) and [DayFormat](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthLabelSettings~DayFormat.html) properties of [MonthLabelSettings](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~MonthLabelSettings.html) in `MonthViewSettings`. 

{% tabs %}
{% highlight c# %}
		//creating new instance for MonthLabelSettings
		MonthLabelSettings monthLabelSettings = new MonthLabelSettings();
		monthLabelSettings.DayFormat = "EEEE";
		monthLabelSettings.DateFormat = "dd";
		monthViewSettings.MonthLabelSettings = monthLabelSettings;
{% endhighlight %}
{% endtabs %}

![](monthview_images/monthlabelformat.png)

## View Header Appearance  
You can customize the View Header appearance by using [ViewHeaderStyle](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ViewHeaderStyle.html) property in SfSchedule. View Header [BackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderStyle~BackgroundColor.html), [DayTextColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderStyle~DayTextColor.html) and [DayTextStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderStyle~DayTextStyle.html) can be customized using `ViewHeaderStyle` properties.

{% tabs %}
{% highlight xaml %}
    <schedule:SfSchedule 
				x:Name="schedule" 
				ScheduleView="MonthView">
        <schedule:SfSchedule.ViewHeaderStyle>
            <schedule:ViewHeaderStyle 
						BackgroundColor="Blue" 
						DayTextColor="White" 
						DayTextStyle="Arial,15">
            </schedule:ViewHeaderStyle>
        </schedule:SfSchedule.ViewHeaderStyle>
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
		//creating new instance for viewHeaderStyle
		ViewHeaderStyle viewHeaderStyle = new ViewHeaderStyle();
		viewHeaderStyle.BackgroundColor = Color.Blue;
		viewHeaderStyle.DayTextColor = Color.White;
		viewHeaderStyle.DayTextStyle = Font.OfSize("Arial", 15);
		schedule.ViewHeaderStyle = viewHeaderStyle;
{% endhighlight %}
{% endtabs %}

![](monthview_images/viewheaderstyle.png)

>**Note**:  FontAttributes and FontFamily are native to the platform. Custom font and the font which are not available in the specified platform will not be applied.

### ViewHeader Date Format
We can customize the date and day format of `SfSchedule` ViewHeader by using [DateFormat](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.DayLabelSettings~DateFormat.html) and [DayFormat](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.DayLabelSettings~DayFormat.html) properties of `MonthLabelSettings`.

{% tabs %}
{% highlight xaml %}
<schedule:SfSchedule>
    <schedule:SfSchedule.MonthViewSettings>
        <schedule:MonthViewSettings>
            <schedule:MonthViewSettings.MonthLabelSettings>
                <schedule:MonthLabelSettings DateFormat=“dd”>
                    <schedule:MonthLabelSettings.DayFormat>
                        <OnPlatform x:TypeArguments="x:String" iOS="EEEE" Android="EEEE" WinPhone="dddd" />
                    </schedule:MonthLabelSettings.DayFormat>
                </schedule:MonthLabelSettings>
            </schedule:MonthViewSettings.MonthLabelSettings>
        </schedule:MonthViewSettings>
    </schedule:SfSchedule.MonthViewSettings>
</schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
schedule.ScheduleView = ScheduleView.MonthView;
//Creating new instance of MonthViewSettings
MonthViewSettings monthViewSettings = new MonthViewSettings();
//Creating new instance of MonthLabelSettings
MonthLabelSettings monthLabelSettings = new MonthLabelSettings();
//Customizing date format
monthLabelSettings.DateFormat = "dd";
monthLabelSettings.DayFormat = Device.OnPlatform("EEEE", "EEEE", "dddd");
monthViewSettings.MonthLabelSettings = monthLabelSettings;
schedule.MonthViewSettings = monthViewSettings;
{% endhighlight %}
{% endtabs %}

![](monthview_images/DateFormat_Month.png)

### ViewHeader Tapped Event
We can handle single tap action of `ViewHeader` by using [ViewHeaderTapped](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ViewHeaderTapped_EV.html) event of `SfSchedule`. This event will be triggered when ViewHeader is Tapped. This event contains [ViewHeaderTappedEventArgs](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ViewHeaderTappedEventArgs.html) argument which holds [DateTime](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.CellTappedEventArgs~Datetime.html) details in it.

{% tabs %}
{% highlight xaml %}
<schedule:SfSchedule x:Name="schedule"
                                     ScheduleView="MonthView"
                                     ViewHeaderTapped="Handle_ViewHeaderTapped" >
</schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
//Creating  new instance of Schedule
SfSchedule schedule = new SfSchedule();
schedule.ScheduleView = ScheduleView.MonthView;
schedule.ViewHeaderTapped += Handle_ViewHeaderTapped;
{% endhighlight %}
{% endtabs %}

{% highlight c# %}
void Handle_ViewHeaderTapped(object sender, ViewHeaderTappedEventArgs e)
{
var dateTime = e.DateTime;
}
{% endhighlight %}

## MonthCell Appearance 
You can customize the Month view cell in three ways,

* [Customize month cell using style](#customize-month-cell-using-style)
* [Customize month cell using event](#customize-month-cell-using-event)
* [Customize month cell with custom UI](#customize-month-cell-with-custom-ui)

### Customize month cell using style
By using [MonthViewCellStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle.html) of `SfSchedule` you can customize the month cell properties such as [BackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~BackgroundColor.html), [NextMonthBackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~NextMonthBackgroundColor.html), [NextMonthTextColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~NextMonthTextColor.html), [PreviousMonthBackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~PreviousMonthBackgroundColor.html), [PreviousMonthTextColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~PreviousMonthTextColor.html), [TextColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~TextColor.html), [TextStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~TextStyle.html), [TodayBackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~TodayBackgroundColor.html), [TodayTextColor](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewCellStyle~TodayTextColor.html).
   
{% tabs %}
{% highlight xaml %}
        <schedule:SfSchedule.MonthCellStyle>
            <schedule:MonthViewCellStyle 
                        BackgroundColor="Blue" 
                        TextColor="Red" 
                        TextStyle="Arial,20" 
                        NextMonthBackgroundColor="Gray" 
                        NextMonthTextColor="Gray" 
                        PreviousMonthBackgroundColor="White" 
                        PreviousMonthTextColor="Gray" 
                        TodayBackgroundColor="Red" 
                        TodayTextColor="White">
            </schedule:MonthViewCellStyle>
        </schedule:SfSchedule.MonthCellStyle>
    </schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
		//MonthCell Appearance
		MonthViewCellStyle monthCellStyle = new MonthViewCellStyle();
		monthCellStyle.BackgroundColor = Color.Blue;
		monthCellStyle.NextMonthBackgroundColor = Color.White;
		monthCellStyle.NextMonthTextColor = Color.Gray;
		monthCellStyle.PreviousMonthBackgroundColor = Color.White;
		monthCellStyle.PreviousMonthTextColor = Color.Gray;
		monthCellStyle.TextColor = Color.Red;
		monthCellStyle.TextStyle = Font.OfSize("Arial", 20);
		monthCellStyle.TodayBackgroundColor = Color.Red;
		monthCellStyle.TodayTextColor = Color.White;
		schedule.MonthCellStyle = monthCellStyle;
{% endhighlight %}
{% endtabs %}

![](monthview_images/monthcellstyle.png)
    
### Customize month cell using event
By using [OnMonthCellLoadedEvent](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~OnMonthCellLoadedEvent_EV.html) in `SfSchedule`, you can customize the month cell properties in the run time. In `OnMonthCellLoadedEvent`, arguments such as [cellStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~cellStyle.html), [appointments](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~appointments.html), [date](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~date.html), [view](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~view.html) and boolean properties such as [isToday](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~isToday.html), [isNextMonthDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~isNextMonthDate.html), [isPreviousMonthDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~isPreviousMonthDate.html) and [isBlackOutDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~isBlackOutDate.html) are in the [MonthCellLoadedEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs.html). 

{% tabs %}
{% highlight c# %}
		schedule.OnMonthCellLoadedEvent += Schedule_OnMonthCellLoadedEvent;
			...
        private void Schedule_OnMonthCellLoadedEvent(object sender, MonthCellLoadedEventArgs args)
        {
            args.cellStyle = new CellStyle();
            if (args.isToday)
            {
                args.cellStyle.BackgroundColor = Color.Red;
                args.cellStyle.TextColor = Color.White;
                args.cellStyle.TextStyle = Font.OfSize("Arial", 25);
            }
            else if (args.isNextMonthDate)
            {
                args.cellStyle.BackgroundColor = Color.White;
                args.cellStyle.TextColor = Color.Gray;
                args.cellStyle.TextStyle = Font.OfSize("Arial", 10);
            }
            else if (args.isPreviousMonthDate)
            {
                args.cellStyle.BackgroundColor = Color.White;
                args.cellStyle.TextColor = Color.Gray;
                args.cellStyle.TextStyle = Font.OfSize("Arial", 10);
            }
            else if (args.isBlackOutDate)
            {
                args.cellStyle.BackgroundColor = Color.Black;
                args.cellStyle.TextColor = Color.White;
                args.cellStyle.TextStyle = Font.OfSize("Arial", 20);
            }
            else
            {
                args.cellStyle.BackgroundColor = Color.Blue;
                args.cellStyle.TextColor = Color.White;
                args.cellStyle.TextStyle = Font.OfSize("Arial", 20);
            }
        }
{% endhighlight %}
{% endtabs %}

![](monthview_images/monthcellstyle_event.png)

>**Note**:  FontAttributes and FontFamily are native to the  platform. Custom font and the font which are not available in the specified platform will not be applied.

#### Customize month cell with custom UI 
You can set the Custom UI for the month cell using [view](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthCellLoadedEventArgs~view.html) property of `MonthCellLoadedEventArgs` in the `OnMonthCellLoadedEvent`.

{% tabs %}
{% highlight c# %}
		schedule.OnMonthCellLoadedEvent += Schedule_OnMonthCellLoadedEvent;
			...
        private void Schedule_OnMonthCellLoadedEvent(object sender, MonthCellLoadedEventArgs args)
        {
            Button button = new Button();
            button.Text = args.date.Day.ToString();
            button.BackgroundColor = Color.Blue;
            button.TextColor = Color.White;
            args.view = button;
            if (args.isToday)
            {
                button.BackgroundColor = Color.Red;
                button.TextColor = Color.White;
            }
        }
{% endhighlight %}
{% endtabs %}

![](monthview_images/monthcellcustomview.png)

## Getting Inline Appointment details
Using [Appointment](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineAppointmentTappedEventArgs~Appointment.html) argument in the [MonthInlineAppointmentTappedEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineAppointmentTappedEventArgs.html) of [MonthInlineAppointmentTapped](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~MonthInlineAppointmentTapped_EV.html) event, you can get the details Month Inline Appointments details while tapping the specific appointment. You can do the required functions while tapping the inline appointment using this event. 

{% tabs %}
{% highlight c# %}
		schedule.MonthInlineAppointmentTapped += Schedule_MonthInlineAppointmentTapped;
			...
        private void Schedule_MonthInlineAppointmentTapped(object sender, MonthInlineAppointmentTappedEventArgs args)
        {
            var appointment = (args.Appointment as ScheduleAppointment);
            DisplayAlert(appointment.Subject, appointment.StartTime.ToString(), "ok");
        }
{% endhighlight %}
{% endtabs %}

![](monthview_images/inlineappointmentdetails.png)

## InlineView Appearance  
By using [OnMonthInlineLoadedEvent](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~OnMonthInlineLoadedEvent_EV.html) in `SfSchedule`, you can customize the month inline view properties in the run time. In `OnMonthInlineLoadedEvent`, arguments such as [monthInlineViewStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineLoadedEventArgs~monthInlineViewStyle.html), [appointments](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineLoadedEventArgs~appointments.html), [selectedDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineLoadedEventArgs~selectedDate.html) are in the MonthInlineLoadedEventArgs.

{% tabs %}
{% highlight c# %}
		schedule.OnMonthInlineLoadedEvent += Schedule_OnMonthInlineLoadedEvent;
			...
        private void Schedule_OnMonthInlineLoadedEvent(object sender, MonthInlineLoadedEventArgs args)
        {
            MonthInlineViewStyle monthInlineViewStyle = new MonthInlineViewStyle();
            monthInlineViewStyle.BackgroundColor = Color.Blue;
            monthInlineViewStyle.TextColor = Color.Green;
            monthInlineViewStyle.TextStyle = Font.OfSize("Times New Roman", 20);
            monthInlineViewStyle.TimeTextColor = Color.Red;
            monthInlineViewStyle.TimeTextSize = 15;
            monthInlineViewStyle.TimeTextFormat = "hh a";
            args.monthInlineViewStyle = monthInlineViewStyle;
        }
{% endhighlight %}
{% endtabs %}

![](monthview_images/inlineviewstyle.png)

>**Note**:  FontAttributes and FontFamily are native to the  platform. Custom font and the font which are not available in the specified platform will not be applied.

## InlineAppointment Appearance 
You can customize the Month inline view Appointment by using [OnMonthInlineAppointmentLoadedEvent](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~OnMonthInlineAppointmentLoadedEvent_EV.html) in `SfSchedule`, using [view](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineAppointmentLoadedEventArgs~view.html) of [MonthInlineAppointmentLoadedEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineAppointmentLoadedEventArgs.html) argument. You can get the details of Appointment in the [appointment](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthInlineAppointmentLoadedEventArgs~appointment.html) argument.

{% tabs %}
{% highlight c# %}
		schedule.OnMonthInlineAppointmentLoadedEvent += Schedule_OnMonthInlineAppointmentLoadedEvent;
			...
        private void Schedule_OnMonthInlineAppointmentLoadedEvent(object sender, MonthInlineAppointmentLoadedEventArgs args)
        {
            var appointment = (args.appointment as ScheduleAppointment);
            Button button = new Button();
            button.Text = appointment.Subject;
            button.BackgroundColor = Color.Blue;
            button.TextColor = Color.White;
            args.view = button;
        }
{% endhighlight %}
{% endtabs %}

>**Note**:  Inline view customization - No support for inline view appointments customization using custom view in XForms UWP.

![](monthview_images/inlinecustomview.png)

## Selection
You can customize the default appearance of selection UI in the month cells.

* [Selection customization using style](#selection-customization-using-style)
* [Selection customization using custom View](#selection-customization-using-custom-view)
* [Programmatic selection](#programmatic-selection)

### Selection customization using style
You can customize the month cell selection by using [SelectionStyle](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectionStyle.html) property of `SfSchedule`.

{% tabs %}
{% highlight C# %}
    schedule.ScheduleView = ScheduleView.MonthView;
    //Create new instance of SelectionStyle
    SelectionStyle selectionStyle = new SelectionStyle();
    selectionStyle.BackgroundColor = Color.Blue;
    selectionStyle.BorderColor = Color.Black;
    selectionStyle.BorderThickness = 5;
    selectionStyle.BorderCornerRadius = 5;
    schedule.SelectionStyle = selectionStyle;
{% endhighlight %}
{% highlight XAML %}
    <schedule:SfSchedule x:Name="schedule" ScheduleView="MonthView">
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

![](monthview_images/SelectionStyle_Month.png)

### Selection customization using custom View
You can replace the default selection UI with your custom view by setting [SelectionView](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectionView.html) property of `SfSchedule`.

{% tabs %}
{% highlight C# %}
    schedule.ScheduleView = ScheduleView.MonthView;
    //Add the CustomView
    Button customView = new Button();
    customView.Text = "+NewEvent";
    customView.BackgroundColor = Color.FromHex("#FF9800");
    customView.TextColor = Color.White;
    schedule.SelectionView = customView;
{% endhighlight %}
{% highlight XAML %}
    <schedule:SfSchedule x:Name="schedule" ScheduleView="MonthView">
        <schedule:SfSchedule.SelectionView>
            <Button
                BackgroundColor="#FF9800"
                Text="+NewEvent"
                TextColor="White"/>
        </schedule:SfSchedule.SelectionView>
    </schedule:SfSchedule>
{% endhighlight %}
{% endtabs %}

![](monthview_images/SelectionView_Month.png)

### Programmatic selection
You can programmatically select the specific cell by setting corresponding date to [SelectedDate](https://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~SelectedDate.html) property of `SfSchedule`. By default, it is null.

{% highlight C# %}
    // Setting a date to select
    schedule.SelectedDate = new DateTime(2017, 10, 04);
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

![](monthview_images/selection_Month.png)

## Today Background Color
We can customize the current date background of  `SfSchedule`  by using [TodayBackground](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.MonthViewSettings~TodayBackground.html) property of `MonthViewSettings`.

{% tabs %}
{% highlight xaml %}
<schedule:SfSchedule ScheduleView=“MonthView”>
    </schedule:SfSchedule.MonthViewSettings>
        <schedule:MonthViewSettings
                                            TodayBackground="Red">
        </schedule:MonthViewSettings>
    </schedule:SfSchedule.MonthViewSettings>
</schedule:SfSchedule>
{% endhighlight %}
{% highlight c# %}
schedule.ScheduleView = ScheduleView.MonthView;
//Creating new instance of MonthViewSettings
MonthViewSettings monthViewSettings = new MonthViewSettings();
//Customizing background color
monthViewSettings.TodayBackground = Color.Red;
schedule.MonthViewSettings = monthViewSettings;
{% endhighlight %}
{% endtabs %}

![](monthview_images/TodayBackground.png)
