---
layout: post
title: Handling Syncfusion ListView Scrolling
description: This section describes about the scrolling behavior of SfListView control and how it can be handled and customized.
platform: xamarin
control: SfListView
documentation: ug
---
# Scrolling

## Programmatic scrolling

### Scrolling to row index

The SfListView allows programmatically scrolling based on the index by using the [ScrollToRowIndex](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.LayoutBase~ScrollToRowIndex.html) method for both linear and grid layouts. It also enables and disables the scrolling animation when changing the view. By default, the scrolling will be animated.

You can set position of item in view while scrolling by passing [ScrollToPosition](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ScrollToPosition.html) to `ScrollToRowIndex` method. Below are four different types of positions:

* MakeVisible: Scrolls a specific item to make visible in the view. If the item is already in view, scrolling will not occur.
* Start: Scrolls a specific item to be positioned at the begin of the view.
* End: Scrolls a specific item to be positioned at the end of the view.
* Center: Scrolls a specific item to be positioned at the center of the view.

You can also scroll to specified data in `SfListView` using the [ScrollTo](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ScrollTo.html) method.

{% tabs %}
{% highlight c# %}

int index = listView.DataSource.DisplayItems.IndexOf(viewModel.Customers[2]); 
// Programmatic scrolling based on the item index.
listView.LayoutManager.ScrollToRowIndex(index, Syncfusion.ListView.XForms.ScrollToPosition.Center, true); 
// Programmatic scrolling based on the item data.
listView.ScrollTo(ViewModel.Customers[index], Syncfusion.ListView.XForms.ScrollToPosition.Center, true);

{% endhighlight %}
{% endtabs %}

N> If grouping is enabled, get the desired row index by passing the underlying data in the [DisplayItems.IndexOf](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.DataSource.Portable~Syncfusion.DataSource.DisplayItems~IndexOf.html) method.

{% tabs %}
{% highlight c# %}

int index = listView.DataSource.DisplayItems.IndexOf(viewModel.Customers[2]); 
listView.LayoutManager.ScrollToRowIndex(index, true); 

{% endhighlight %}
{% endtabs %}

### Limitations

 * When [AutoFitMode](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~AutoFitMode.html) is `Height` or grouping is enabled, the scroll animation will be disabled by default in Android and iOS platforms. 
 * If [ScrollToRowIndex](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.LayoutBase~ScrollToRowIndex.html) method is called when loading the `SfListView`, set `disableAnimation` to `true` to scroll to the appropriate row index, or else view does not scrolled in Android.
 * If the `ScrollToRowIndex` method is applied to a particular item index while the item is in Grouping or AutoFit mode, the particular item will get displayed in view but not in the exact position when the [ScrollToPosition](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ScrollToPosition.html) property is set as `MakeVisible` or `Center` for first time.
* In UWP platform, when you hover and scroll the inner listview, the outer listview will not be scrolled by default. To overcome this, set the `InputTransparent` to `True` for the parent element loaded in the `ItemTemplate`. If you set InputTransparent, then the inner listview scroll will not work. This is the default behavior of the listview.

## Scrollbar visibility

The SfListView provides an option to enable or disable the `Scrollbar` visibility by using the [IsScrollBarVisible](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~IsScrollBarVisible.html) property. By default, the value will be `true`.  

N> Due to some restrictions in native ScrollView renderer in Xamarin.Forms, you cannot change the `IsScrollBarVisible` value at runtime. It can be defined only when initializing the SfListView. 

{% tabs %}
{% highlight xaml %}
<syncfusion:SfListView x:Name="listView" IsScrollBarVisible="False" />
{% endhighlight %}
{% highlight c# %}
listView.IsScrollBarVisible = false; 
{% endhighlight %}
{% endtabs %}

## ListView with full height

The `SfListView` will load all of its items by setting the [IsScrollingEnabled](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~IsScrollingEnabled.html) property to `false`.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfListView x:Name="listView" IsScrollingEnabled="False" />
{% endhighlight %}
{% highlight c# %}
listView.IsScrollingEnabled = false; 
{% endhighlight %}
{% endtabs %}

N> ListView's scrolling will not be enabled when `IsScrollingEnabled` is `false`. To enable scrolling, load ListView inside `ScrollView`.

## Identifying scroll state changes

The SfListView will notify the scrolling state changes by using the [ScrollStateChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ScrollStateChanged_EV.html) event.

Following states will be notified via [ScrollState](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ScrollState.html) property in the event argument.

 * Dragging: Specifies that `SfListView` is currently being dragged in the view.
 * Fling: Specifies that fling action is performed on the `SfListView`.
 * Idle: Specifies that `SfListView` is not currently scrolling.
 * Programmatic: Specifies that scrolling is performed by using [ScrollTo](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ScrollTo.html) or [ScrollToRowIndex](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.LayoutBase~ScrollToRowIndex.html) method.

{% tabs %}
{% highlight c# %}

listView.ScrollStateChanged += ListView_ScrollStateChanged;
private void ListView_ScrollStateChanged(object sender, ScrollStateChangedEventArgs e)
{
   if (e.ScrollState == ScrollState.Idle)
   {
      DisplayAlert("ScrollState", "Scrolling has stopped", "OK");
   }
}

{% endhighlight %}
{% endtabs %}

## Identify when end of the list is reached on scrolling

The SfListView allows notifying when scrolling using [Changed](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.GridCommon.Portable~Syncfusion.GridCommon.ScrollAxis.ScrollAxisBase~Changed_EV.html) event of [ScrollAxisBase](http://help.syncfusion.com/cr/cref_files/wpf/Syncfusion.SfGrid.WPF~Syncfusion.UI.Xaml.ScrollAxis.ScrollAxisBase.html) in [VisualContainer](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.VisualContainer.html) of the SfListView. By using this event, you can find whether reached the last item in the list in the SfListView based on [LastBodyVisibleLineIndex](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.GridCommon.Portable~Syncfusion.GridCommon.ScrollAxis.ScrollAxisBase~LastBodyVisibleLineIndex.html) property and underlying collection count.

{% tabs %}
{% highlight c# %}
using Syncfusion.ListView.XForms.Control.Helpers;
public partial class MainPage : ContentPage
{
    VisualContainer visualContainer;
    bool isAlertShown = false;

    public MainPage()
    {
        InitializeComponent();
        visualContainer = listView.GetVisualContainer();
        visualContainer.ScrollRows.Changed += ScrollRows_Changed;
    }

    ///<summary>
    ///To notify when end reached
    ///</summary>
    private void ScrollRows_Changed(object sender, ScrollChangedEventArgs e)
    {
        var lastIndex = visualContainer.ScrollRows.LastBodyVisibleLineIndex;

        //To include header if used
        var header = (listView.HeaderTemplate != null && !listView.IsStickyHeader) ? 1 : 0;

        //To include footer if used
        var footer = (listView.FooterTemplate != null && !listView.IsStickyFooter) ? 1 : 0;
        var totalItems = listView.DataSource.DisplayItems.Count + header + footer;

        if ((lastIndex == totalItems - 1))
        {
            if (!isAlertShown)
            {
                DisplayAlert("Alert", "End of list reached...", "Ok");
                isAlertShown = true;
            }
        }
        else
            isAlertShown = false;
    }
}

{% endhighlight %}
{% endtabs %}

Download the entire source code from GitHub [here](https://github.com/SyncfusionExamples/Notify-when-end-of-the-xamarin.forms-listview-reached-on-scrolling).

## Maintain the scroll position while updating ItemsSource at runtime

The SfListView have scrolled to top automatically when changing the ItemsSource at runtime. However, you can maintain the same scrolled position by using the `ScrollY` value of ExtendedScrollView from the [VisualContainer](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.VisualContainer.html). After changing the ItemsSource, you can pass the ScrollY value to [ScrollTo](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ScrollTo.html) method of SfListView and scroll back to the same position.

For horizontal orientation, use the `ScrollX` value of ExtendedScrollView.

 By using [Reflection](https://msdn.microsoft.com/en-us/library/system.reflection(v=vs.110).aspx), get the value of `ScrollOwner` from `VisualContainer` and use it.

{% tabs %}
{% highlight c# %}
using Syncfusion.ListView.XForms.Control.Helpers;
public partial class MainPage : ContentPage
{
    ExtendedScrollView scrollView;

    public MainPage()
    {
        InitializeComponent();
        scrollView = listView.GetScrollView();
    }

    private void ChangeItemsSource_Clicked(object sender, EventArgs e)
    {
        var viewModel = new ContactsViewModel();
        listView.ItemsSource = viewModel.EmployeeInfo;
        listView.ScrollTo(scrollView.ScrollY);
    }
}

{% endhighlight %}
{% endtabs %}

Download the entire source code from GitHub [here](https://github.com/SyncfusionExamples/Maintaing-scroll-position-on-changing-itemssource-xamarin.forms-listview).
