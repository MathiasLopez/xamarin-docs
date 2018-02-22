---   
layout: post   
title: Syncfusion SfSchedule control Getting Started for Xamarin.Forms   
description: A quick tour to initial users on Syncfusion SfSchedule control for Xamarin.Forms platform   
platform: xamarin   
control: SfSchedule   
documentation: ug   
---   
    
# Getting Started   
    
This section provides you an overview for working with SfSchedule for Xamarin.Forms and also provides a walk through to configure SfSchedule control in real time scenario.   

## Assembly Configuration   
    
SfSchedule can be included in your Xamarin.Forms project in two ways,  
 
* [Assembly Reference](#assembly-reference)  
* [NuGet Configuration](#nuget-configuration)  

### Assembly Reference  
 
You can download our Xamarin.Forms components directly from our website, refer [here](https://help.syncfusion.com/xamarin/introduction/download-and-installation#download-directly-from-website) for assistance.   
 
Once the assemblies has been downloaded and explored, you can find all the required assemblies in the installation folders.   
   
{Syncfusion Essential Studio Installed location}\Essential Studio\syncfusionessentialstudio-releaseversion\Xamarin\lib   
    
Eg: C:\Program Files (x86)\Syncfusion\Essential Studio\15.1.0.41\Xamarin\lib  
    
>**Notes**: Assemblies can be found in unzipped package location in Mac   
    
The following list of assemblies need to be added as reference from the lib folder to use SfSchedule in your application.   
    
<table>   
<tr>   
<th>Project</th>   
<th>Required assemblies</th>   
</tr>   
<tr>   
<td>PCL</td>   
<td>pcl\Syncfusion.SfSchedule.XForms.dll<br/></td>   
</tr>   
<tr>   
<td>Android Renderer</td>   
<td>pcl\Syncfusion.SfSchedule.XForms.dll<br/>android\Syncfusion.SfSchedule.Android.dll<br/>android\Syncfusion.SfSchedule.XForms.Android.dll<br/></td>   
</tr>   
<tr>   
<td>iOS Renderer</td>   
<td>pcl\Syncfusion.SfSchedule.XForms.dll<br/>ios-unified\Syncfusion.SfSchedule.iOS.dll<br/>ios-unified\Syncfusion.SfSchedule.XForms.iOS.dll<br/></td>   
</tr>   
<tr>   
<td>UWP Renderer</td>   
<td>pcl\Syncfusion.SfSchedule.XForms.dll<br/>uwp\Syncfusion.SfSchedule.XForms.UWP.dll<br/></td>   
</tr>   
</table>   
 

>**Note:**
For compiling the UWP project in Xamarin.Forms, referring the Schedule assemblies (XForms, XForms.UWP) in the XForms (UWP) project is sufficient and its files (properties, themes, etc.) needs to be maintained in the UWP assembly folder to render the control.

### NuGet Configuration  
    
Alternatively you can refer SfSchedule in your application by configuring nuget packages.    
  
* [Configuration in Xamarin Studio](https://help.syncfusion.com/xamarin/introduction/download-and-installation#install-syncfusions-nuget-package-in-xamarin-studio)  
* [Configuration in Visual Studio](https://help.syncfusion.com/xamarin/introduction/download-and-installation#configuring-syncfusion-nuget-packages-in-visual-studio)  
* [Configuration from command line in Linux/MAC](https://help.syncfusion.com/xamarin/introduction/download-and-installation#configuring-syncfusion-nuget-packages-from-command-line-in-linuxmac)  

### Launching SfSchedule on each platform 
 
To use SfSchedule inside an application, each platform application must initialize the SfScheduleRenderer. This initialization step varies from platform to platform and it is discussed in the following sections.   
    
#### Android 
    
Android application launches SfSchedule without any initialization.  
    
#### iOS

To launch SfSchedule in iOS, you need to call `SfScheduleRenderer.Init()` in the FinishedLaunching overridden method of the AppDelegate class after the Xamarin.Forms Framework initialization.   
    
{% highlight c# %}   
    public override bool FinishedLaunching (UIApplication app, NSDictionary options)   
    {    
        ...    
        global::Xamarin.Forms.Forms.Init (); 
        SfScheduleRenderer.Init();    
        LoadApplication (new App ());   
        ...   
    }
{% endhighlight %}   
    
#### Universal Windows Platform (UWP)
 
UWP application launches SfSchedule without any initialization.  

##### ReleaseMode issue in UWP platform

There is a known Framework issue in UWP platform. The custom controls will not render when deployed the application in `Release Mode`.

The above problem can be resolved by initializing the SfSchedule assemblies in `App.xaml.cs` in UWP project as like in below code snippet.

{% highlight c# %}
    // In App.xaml.cs
	protected override void OnLaunched(LaunchActivatedEventArgs e)
    {
        ...
        rootFrame.NavigationFailed += OnNavigationFailed;
        // you'll need to add `using System.Reflection;`
        List<Assembly> assembliesToInclude = new List<Assembly>();
        //Now, add all the assemblies your app uses assembliesToInclude.Add(typeof(SfScheduleRenderer).GetTypeInfo().Assembly);
        // replaces Xamarin.Forms.Forms.Init(e);        
        Xamarin.Forms.Forms.Init(e, assembliesToInclude);
        ...     
    }
{% endhighlight %}

    
## Create a simple application with SfSchedule  
    
This section explains how to create a simple application using SfSchedule control. SfSchedule control can be configured entirely in C# code or by using XAML markup. This is how the final output will look like on iOS, Android and Windows Phone devices.  
    
![](GettingStarted_images/GettingStarted.png)   

You can download the entire source code of this demo for Xamarin.Forms from
here [ScheduleGettingStarted](http://www.syncfusion.com/downloads/support/directtrac/general/ze/ScheduleGettingStarted-815086813.zip)
    
This section provides a walks through to create `MeetingRoomScheduler` using our Schedule control.  
    
* [Creating a new project](#creating-a-new-project)   
* [Adding SfSchedule to the project](#adding-sfschedule-to-the-project)        
* [Changing Schedule Views](#changing-schedule-views)     
* [Binding data to SfSchedule control](#binding-data-to-sfschedule-control)  

## Creating a new project  
    
Create a new Blank App (Xamarin.Forms.Portable) application in Xamarin Studio or Visual Studio.  
    
Add the required assembly references to the pcl and renderer projects as discussed in the [Assembly Configuration](#assembly-configuration) section.   
    
Import SfSchedule control namespace `Syncfusion.SfSchedule.XForms`.   
    
## Adding SfSchedule to the project   
    
Set the SfSchedule control as content to the ContentPage.   
    
{% tabs %}   
{% highlight xaml %}   
    <?xml version="1.0" encoding="utf-8" ?>
    <ContentPage
        x:Class="GettingStarted.Sample"
        xmlns="http://xamarin.com/schemas/2014/forms"
        xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
        xmlns:local="clr-namespace:GettingStarted;assembly=GettingStarted"
        xmlns:syncfusion="clr-namespace:Syncfusion.SfSchedule.XForms;assembly=Syncfusion.SfSchedule.XForms">
        
		<ContentPage.Content>
            <syncfusion:SfSchedule x:Name="schedule" />
        </ContentPage.Content>
    </ContentPage>
{% endhighlight %}   
{% highlight c# %}   
    using Syncfusion.SfSchedule.XForms;   
    using Xamarin.Forms;   
    
    namespace GettingStarted   
    {   
        public class App:Application   
        {   
            SfSchedule schedule; 
            public App()   
            {   
                InitializeComponent();   
                //Creating new instance for SfSchedule   
                schedule = new SfSchedule();   
                MainPage = new ContentPage { Content = schedule };   
            }   
        }   
    } 
{% endhighlight %}   
{% endtabs %}   

You can download the source code for rendering of schedule for Xamarin.Forms from
here [ScheduleProject](http://www.syncfusion.com/downloads/support/directtrac/general/ze/ScheduleSimpleSample-1966430884.zip)

## Changing Schedule Views   
    
SfSchedule control provides four different types of views to display dates and it can be assigned to the control by using [ScheduleView](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleView.html) property. By default the control is assigned with `DayView`. Current date will be displayed initially for all the Schedule views.  

Schedule control will be rendered with `Sunday` as the first day of the week, but you can customize to any day by using [FirstDayOfWeek](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~FirstDayOfWeek.html) property of `SfSchedule`.
    
{% tabs %}  
{% highlight xaml %}
    <syncfusion:SfSchedule x:Name="schedule" FirstDayOfWeek="2"/>   
{% endhighlight %}   
{% highlight c# %}
    //setting first day of the week    
    schedule.FirstDayOfWeek = (int)DayOfWeek.Tuesday;   
{% endhighlight %}  
{% endtabs %}   
    
![](GettingStarted_images/FirstDayOfWeek.png)   

### Day View   
    
DayView is used to display a single day, current day will be visible by default. Appointments on a specific day will be arranged in respective timeslots based on its duration.   
    
{% tabs %}   
{% highlight xaml %}
    <syncfusion:SfSchedule x:Name="schedule" ScheduleView="DayView" />   
{% endhighlight %}   
{% highlight c# %}
    schedule.ScheduleView = ScheduleView.DayView;   
{% endhighlight %}   
{% endtabs %}   
    
![](GettingStarted_images/DayView.png)   

### Week View   
 
`WeekView` is to view all days of a particular week. Appointments will be arranged based on the dates on the week in respective timeslots.  
    
{% tabs %}   
{% highlight xaml %}
    <syncfusion:SfSchedule x:Name="schedule" ScheduleView="WeekView" />   
{% endhighlight %}   
{% highlight c# %}
    schedule.ScheduleView = ScheduleView.WeekView;   
{% endhighlight %}   
{% endtabs %}   
    
![](GettingStarted_images/WeekView.png)  

### Work Week View   
 
`WorkWeekView` is to view only working days of a particular week. By default, Saturday and Sunday are the non-working days. You can be customize it with any days of a Week. Appointments arranged in timeslots based on its duration with respective day of the week.  
    
{% tabs %}   
{% highlight xaml %}
    <syncfusion:SfSchedule x:Name="schedule" ScheduleView="WorkWeekView" />   
{% endhighlight %}   
{% highlight c# %}
    schedule.ScheduleView = ScheduleView.WorkWeekView;   
{% endhighlight %}   
{% endtabs %}   
    
![](GettingStarted_images/WorkWeek.png)   

>**Notes**: Appointments in non-working days will not be displayed.  

### Month View   
    
`MonthView` in Schedule control is to view entire dates of a particular month. Appointments can be viewed in inline by setting [ShowAppointmentsInline](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~ShowAppointmentsInline.html) property of `SfSchedule` as true.    
    
{% tabs %}   
{% highlight xaml %}
    <syncfusion:SfSchedule
        x:Name="schedule"
        ScheduleView="MonthView"
        ShowAppointmentsInline="True"/>
{% endhighlight %}  
{% highlight c# %}
    schedule.ScheduleView = ScheduleView.MonthView;  
    //view appointments in inline  
    schedule.ShowAppointmentsInline = true;  
{% endhighlight %}   
{% endtabs %}   
    
![](GettingStarted_images/MonthView.png)

## Binding data to SfSchedule control   
  
Schedule control has a built-in capability to handle the appointment arrangement internally based on the ScheduleAppointment collections. You need to assign the created collection to the [DataSource](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.SfSchedule~DataSource.html) property of `SfSchedule`.  
  
### Adding Appointments   
  
[ScheduleAppointment](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment.html) is a class, which holds the details about the appointment to be rendered in schedule. It has some basic properties such as [StartTime](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~StartTime.html), [EndTime](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~EndTime.html), [Subject](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~Subject.html) and some additional information about the appointment can be added using [Color](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~Color.html), [Notes](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~Notes.html), [Location](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~Location.html), [IsAllDay](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~IsAllDay.html), [IsRecursive](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointment~IsRecursive.html) properties.    
    
{% highlight c# %}
    ScheduleAppointmentCollection appointmentCollection = new ScheduleAppointmentCollection();   
    //Creating new event   
    ScheduleAppointment clientMeeting = new ScheduleAppointment();   
    DateTime currentDate = DateTime.Now;   
    DateTime startTime = new DateTime (currentDate.Year,currentDate.Month,currentDate.Day, 10, 0, 0);    
    DateTime endTime = new DateTime (currentDate.Year, currentDate.Month,currentDate.Day, 12, 0, 0);   
    clientMeeting.StartTime = startTime;   
    clientMeeting.EndTime = endTime;   
    clientMeeting.Color = Color.Blue;   
    clientMeeting.Subject = "ClientMeeting";   
    appointmentCollection.Add(clientMeeting);   
    schedule.DataSource = appointmentCollection;
{% endhighlight %}   

You can download the source code for rendering of schedule appointment using `ScheduleAppointmentCollection` for Xamarin.Forms from
here [ScheduleAppointment](http://www.syncfusion.com/downloads/support/directtrac/general/ze/ScheduleAppointment-62423344.zip)

### Adding Custom Appointments   
  
You can also map custom appointments data to our schedule.   
  
>**Notes**: CustomAppointment class should contain two DateTime fields and a string field as mandatory.  
 
Here steps to render `MeetingRoomScheduler` using SfSchedule control with respective custom data properties created in a class Meeting.  
  
* [Creating custom class for appointments](#creating-custom-class-for-appointments) 
* [Creating view model](#creating-view-model)
* [Mapping custom class](#mapping-custom-class)  
* [Setting data source for SfSchedule](#setting-data-source-for-sfschedule)  

#### Creating custom class for appointments
 
You can create a custom class `Meeting` with mandatory fields "From", "To" and "EventName". 
 
{% highlight c# %}
    /// <summary>   
    /// Represents custom data properties.   
    /// </summary>   
    public class Meeting   
    {   
        public string EventName { get; set; }   
        public string Organizer { get; set; }   
        public string ContactID { get; set; }   
        public int Capacity { get; set; }   
        public DateTime From { get; set; }   
        public DateTime To { get; set; }   
        public Color color { get; set; }
		public bool AllDay { get; set; }   
    }
{% endhighlight %}   
    
>**Notes**: You can inherit this class from `INotifyPropertyChanged` for dynamic changes in custom data.  

#### Creating view model 

You can schedule meetings for a particular day by setting `From` and `To` of `Meeting` class.Also you can change subject and color of appointment using `EventName` and `color` of Meeting class. In a separate ViewModel class you can describe the collection of custom appointments.  

{% highlight c# %}
    /// <summary>   
    /// Represents collection of appointments.   
    /// </summary> 
    public class ViewModel
    {
		public ObservableCollection<Meeting> Meetings { get; set; }
		List<string> eventNameCollection;
		List<Color> colorCollection;
		public ViewModel()
		{
			Meetings = new ObservableCollection<Meeting>();
			CreateEventNameCollection();
			CreateColorCollection();
			CreateAppointments();
		}

		/// <summary>
		/// Creates meetings and stores in a collection.  
		/// </summary>
		private void CreateAppointments()
		{
			Random randomTime = new Random();
			List<Point> randomTimeCollection = GettingTimeRanges();
			DateTime date;
			DateTime DateFrom = DateTime.Now.AddDays(-10);
			DateTime DateTo = DateTime.Now.AddDays(10);
			DateTime dataRangeStart = DateTime.Now.AddDays(-3);
			DateTime dataRangeEnd = DateTime.Now.AddDays(3);

			for (date = DateFrom; date < DateTo; date = date.AddDays(1))
			{
			if ((DateTime.Compare(date, dataRangeStart) > 0) && (DateTime.Compare(date, dataRangeEnd) < 0))
			{
				for (int AdditionalAppointmentIndex = 0; AdditionalAppointmentIndex < 3; AdditionalAppointmentIndex++)
				{
					Meeting meeting = new Meeting();
					int hour = (randomTime.Next((int)randomTimeCollection[AdditionalAppointmentIndex].X, (int)randomTimeCollection[AdditionalAppointmentIndex].Y));
					meeting.From = new DateTime(date.Year, date.Month, date.Day, hour, 0, 0);
					meeting.To = (meeting.From.AddHours(1));
					meeting.EventName = eventNameCollection[randomTime.Next(9)];
					meeting.color = colorCollection[randomTime.Next(9)];
					if(AdditionalAppointmentIndex%3==0)
					  meeting.AllDay = true;
					Meetings.Add(meeting);
				}
			}
            else
            {
                Meeting meeting = new Meeting();
                meeting.From = new DateTime(date.Year, date.Month, date.Day, randomTime.Next(9, 11), 0, 0);
                meeting.To = (meeting.From.AddHours(1));
                meeting.EventName = eventNameCollection[randomTime.Next(9)];
                meeting.color = colorCollection[randomTime.Next(9)];
                Meetings.Add(meeting);
            }
        }
    }

    /// <summary>  
    /// Creates event names collection.  
    /// </summary>  
    private void CreateEventNameCollection()
    {
        eventNameCollection = new List<string>();
        eventNameCollection.Add("General Meeting");
        eventNameCollection.Add("Plan Execution");
        eventNameCollection.Add("Project Plan");
        eventNameCollection.Add("Consulting");
        eventNameCollection.Add("Performance Check");
        eventNameCollection.Add("Yoga Therapy");
        eventNameCollection.Add("Plan Execution");
        eventNameCollection.Add("Project Plan");
        eventNameCollection.Add("Consulting");
        eventNameCollection.Add("Performance Check");
    }

    /// <summary>  
    /// Creates color collection.  
    /// </summary>  
    private void CreateColorCollection()
    {
        colorCollection = new List<Color>();
        colorCollection.Add(Color.FromHex("#FF339933"));
        colorCollection.Add(Color.FromHex("#FF00ABA9"));
	    colorCollection.Add(Color.FromHex("#FFE671B8"));
        colorCollection.Add(Color.FromHex("#FF1BA1E2"));
        colorCollection.Add(Color.FromHex("#FFD80073"));
        colorCollection.Add(Color.FromHex("#FFA2C139"));
        colorCollection.Add(Color.FromHex("#FFA2C139"));
        colorCollection.Add(Color.FromHex("#FFD80073"));
        colorCollection.Add(Color.FromHex("#FF339933"));
        colorCollection.Add(Color.FromHex("#FFE671B8"));
        colorCollection.Add(Color.FromHex("#FF00ABA9"));
    }

    /// <summary>
    /// Gets the time ranges.
    /// </summary>
    private List<Point> GettingTimeRanges()
    {
        List<Point> randomTimeCollection = new List<Point>();
        randomTimeCollection.Add(new Point(9, 11));
        randomTimeCollection.Add(new Point(12, 14));
        randomTimeCollection.Add(new Point(15, 17));
        return randomTimeCollection;
    }
    }
{% endhighlight %}

#### Mapping custom class  

You can map those properties of `Meeting` class with our schedule control by using [ScheduleAppointmentMapping](http://help.syncfusion.com/cr/cref_files/xamarin/sfschedule/Syncfusion.SfSchedule.XForms~Syncfusion.SfSchedule.XForms.ScheduleAppointmentMapping.html).   

{% tabs %}
{% highlight xaml %}
    <syncfusion:SfSchedule x:Name="schedule">
        <syncfusion:SfSchedule.AppointmentMapping>
            <syncfusion:ScheduleAppointmentMapping
                ColorMapping="color"
                EndTimeMapping="To"
                StartTimeMapping="From"
                SubjectMapping="EventName" 
				IsAllDayMapping="AllDay"/>
        </syncfusion:SfSchedule.AppointmentMapping>
    </syncfusion:SfSchedule>
{% endhighlight %}
{% highlight c# %}  
    ScheduleAppointmentMapping dataMapping = new ScheduleAppointmentMapping(); 
    dataMapping.ColorMapping = "color";  
    dataMapping.EndTimeMapping = "To";
    dataMapping.StartTimeMapping = "From"; 
    dataMapping.SubjectMapping = "EventName";
	dataMapping.IsAllDayMapping = "AllDay";
    schedule.AppointmentMapping = dataMapping;  
{% endhighlight %}
{% endtabs %}

#### Setting data source for SfSchedule  

Create meetings of type `ObservableCollection <Meeting>`  and assign those appointments collection `Meetings` to the `DataSource` property of `SfSchedule`.

{% tabs %}
{% highlight xaml %}
    <syncfusion:SfSchedule x:Name="schedule"
        DataSource = "{Binding Meetings}"
        ScheduleView = "WeekView" >
        <syncfusion:SfSchedule.BindingContext>
            <local:ViewModel/>
        </syncfusion:SfSchedule.BindingContext>
    </syncfusion:SfSchedule>
{% endhighlight %}
{% highlight c# %}
    ViewModel viewModel = new ViewModel();
    schedule.DataSource = viewModel.Meetings;
{% endhighlight %}
{% endtabs %}

![](GettingStarted_images/GettingStarted.png)

You can download the entire source code of this demo for Xamarin.Forms from
here [ScheduleGettingStarted](http://www.syncfusion.com/downloads/support/directtrac/general/ze/ScheduleGettingStarted-815086813.zip)

