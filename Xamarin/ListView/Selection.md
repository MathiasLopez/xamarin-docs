---
layout: post
title: Selection in Syncfusion SfListView
description: Describes about the selection behavior in SfListView.
platform: xamarin
control: SfListView
documentation: ug
---

# Selection

This section explains how to perform selection and its related operations in the SfListView.

## UI selection

The SfListView allows selecting items either programmatically or touch interactions by setting the [SfListView.SelectionMode](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionMode.html) property value to other than `None`. The control has different selection modes to perform selection operations as listed as follows:

 * None: Allows disabling selection.
 * Single: Allows selecting single item only. When clicking on the selected item, selection not will not be cleared. This is the default value for `SfListView.SelectionMode`.
 * SingleDeselect: Allows selecting single item only. When clicking on the selected item, selection gets cleared.
 * Multiple: Allows selecting more than one item. Selection is not cleared when selecting more than one items. When clicking on the selected item, selection gets cleared.

The SfListView allows selecting items on different gestures such as tap, double tap, and hold by setting the [SfListView.SelectionGesture](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionGesture.html). The default value for the `SfListView.SelectionGesture` is [TouchGesture.Tap](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.TouchGesture.html).

{% tabs %}
{% highlight xaml %}
 <syncfusion:SfListView x:Name="listView"
                        SelectionMode="Multiple"
                        SelectionGesture="Hold"/>
{% endhighlight %}                     
{% highlight c# %}
listView.SelectionMode = SelectionMode.Multiple;
listView.SelectionGesture = TouchGesture.Hold;
{% endhighlight %}
{% endtabs %}

![Single item selection in listview](SfListView_images/SfListView-Selection-1.png)

## Programmatic selection

When the [SfListView.SelectionMode](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionMode.html) is other than `None`, the item or items in the SfListView can be selected from the code by setting the [SfListView.SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html), or adding items to the [SfListView.SelectedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) property based on the `SfListView.SelectionMode`.

When the selection mode is `Single`, programmatically select an item by setting the underlying object to the `SfListView.SelectedItem` property. 

{% tabs %}
{% highlight c# %}
//Perform selection using selected item
listView.SelectedItem = viewModel.Items[5];
{% endhighlight %}
{% endtabs %}

When the selection mode is `Multiple`, programmatically select more than one item by adding the underlying object to the `SfListView.SelectedItems` property. 

{% tabs %}
{% highlight c# %} 
//Perform multiple selection using selected items
listView.SelectedItems.Add (viewModel.Items [4]);
listView.SelectedItems.Add (viewModel.Items[5]);
{% endhighlight %}
{% endtabs %}

All items of the SfListView can be selected using the [SelectAll](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectAll.html) method.

{% tabs %}
{% highlight c# %} 
listView.SelectAll();
{% endhighlight %}
{% endtabs %}

N> When programmatically select an item then the selection related [events](https://help.syncfusion.com/xamarin/sflistview/selection#events) will not be triggered. It triggers only on UI interactions.
However, get the notification from the SelectedItems collection changed event which will be triggered when add an item at runtime.

## Selected items

### Get selected items

The SfListView gets all the selected items through the [SfListView.SelectedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) property  and gets the single item by using the [SfListView.SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html) property.

### Clear selected items

The selected items can be cleared by calling the [SelectedItems.Clear()](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) method.

{% tabs %}
{% highlight c# %}
listView.SelectedItems.Clear();
{% endhighlight %}
{% endtabs %}

### CurrentItem vs SelectedItem

The SfListView gets the selected item by using the [SfListView.SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html) and [SfListView.CurrentItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~CurrentItem.html) properties. Both `SfListView.SelectedItem` and `SfListView.CurrentItem` returns the same data object when selecting single item. When selecting more than one item, the `SfListView.SelectedItem` property returns the first selected item, and the `SfListView.CurrentItem` property returns the last selected item.

W> If you select an item when [SfListView.SelectionMode](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionMode.html) is none or if you select multiple items when `SfListView.SelectionMode` is single, exception will be thrown.

## Selected item customization 

The SfListView supports customizing the selection background color for the selected items by using the [SfListView.SelectedItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItemTemplate.html) if the background color is set to view loaded in the [SfListView.ItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ItemTemplate.html).

{% tabs %}
{% highlight xaml %}
<ContentPage  xmlns:syncfusion="clr-namespace:Syncfusion.ListView.XForms;assembly=Syncfusion.SfListView.XForms">
  <syncfusion:SfListView x:Name="listView">
   <syncfusion:SfListView.SelectedItemTemplate>
    <DataTemplate>
     <Grid x:Name="grid" BackgroundColor="RoyalBlue">
      <Grid.RowDefinitions>
         <RowDefinition Height="*" />
         <RowDefinition Height="*" />
         <RowDefinition Height="1" />
       </Grid.RowDefinitions>
      <Label Text="{Binding SongTitle}" />
      <Label Text="{Binding SongAuther}" Grid.Row="1"/>
      <Frame Grid.Row="2" HasShadow="True" HeightRequest="1"/>
     </Grid>
    </DataTemplate>
   </syncfusion:SfListView.SelectedItemTemplate>
  </syncfusion:SfListView>
</ContentPage>
{% endhighlight %}
{% highlight c# %}
 listView.SelectedItemTemplate = new DataTemplate(() =>
{
  var grid = new Grid();
  grid.RowDefinitions.Add(new RowDefinition { Height = new GridLength(1, GridUnitType.Star) });
  grid.RowDefinitions.Add(new RowDefinition { Height = new GridLength(1, GridUnitType.Star) });
  grid.RowDefinitions.Add(new RowDefinition { Height = new GridLength(1) });
  grid.BackgroundColor = Color.RoyalBlue;
  var songTitle = new Label();
  songTitle.SetBinding(Label.TextProperty, new Binding("SongTitle"));
  var songAuthor = new Label();
  songAuthor.SetBinding(Label.TextProperty, new Binding("songAuthor"));
  var frame = new Frame()
  {
    HeightRequest = 1,
    HasShadow = true,
  };
  grid.Children.Add(songTitle);
  grid.Children.Add(songAuthor, 0, 1);
  grid.Children.Add(frame, 0, 2);
  return grid;
});
{% endhighlight %}
{% endtabs %}

Download the entire sample from GitHub [here](https://github.com/SyncfusionExamples/Customize-selected-item-in-xamarin.forms-listview).

![Custom selection in listview](SfListView_images/SfListView-Selection-3.png)

### Show checked circle on selected items 

To customize the appearance of the selected item or items by using the appearance of [SfListView.SelectedItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItemTemplate.html). The following customizations should give an idea to customize the appearance of selected items in the control.

{% tabs %}
{% highlight xaml %}
<ContentPage xmlns:syncfusion="clr-namespace:Syncfusion.ListView.XForms;assembly=Syncfusion.SfListView.XForms">
  <syncfusion:SfListView x:Name="listView">
   <syncfusion:SfListView.SelectedItemTemplate>
    <DataTemplate>
     <Grid x:Name="grid">
      <Grid.ColumnDefinitions>
       <ColumnDefinition Width="40" />
       <ColumnDefinition Width="*" />    
       <ColumnDefinition Width="Auto" />
      </Grid.ColumnDefinitions>
      <Image Source="{Binding SongThumbnail}"/>
      <Grid Grid.Column="1">
       <Grid.RowDefinitions>
        <RowDefinition Height="*" />
        <RowDefinition Height="*" />
       </Grid.RowDefinitions>
       <Label Text="{Binding SongTitle}" />
       <Grid Grid.Row="1">
        <Grid.ColumnDefinitions>
         <ColumnDefinition Width="*" />
         <ColumnDefinition Width="*" />
        </Grid.ColumnDefinitions>
        <Label Text="{Binding SongAuther}" />
        <Label Grid.Column="1" Text="{Binding SongSize}"/>
       </Grid>
      </Grid>
      <Image Grid.Column="2" x:Name="selectionImage" IsVisible="True" Source="Selected.png"/>
     </Grid>
    </DataTemplate>
   </syncfusion:SfListView.SelectedItemTemplate>
  </syncfusion:SfListView>
</ContentPage>
{% endhighlight %}
{% highlight c# %}
listView.SelectedItemTemplate = new DataTemplate(() =>
{
  var grid1 = new Grid();
  grid1.ColumnDefinitions.Add(new ColumnDefinition { Width = new GridLength(40) });
  grid1.ColumnDefinitions.Add(new ColumnDefinition { Width = new GridLength(1, GridUnitType.Star) });
  grid1.ColumnDefinitions.Add(new ColumnDefinition { Width = new GridLength(1, GridUnitType.Auto) });
  var songThumbnail = new Image();
  songThumbnail.SetBinding(Image.SourceProperty, new Binding("SongThumbnail"));
  var grid2 = new Grid();
  grid2.RowDefinitions.Add(new RowDefinition { Height = new GridLength(1, GridUnitType.Star) });
  grid2.RowDefinitions.Add(new RowDefinition { Height = new GridLength(1, GridUnitType.Star) });
  grid2.Padding = new Thickness(15, 0, 0, 0);
  var songTitle = new Label();
  songTitle.SetBinding(Label.TextProperty, new Binding("SongTitle"));
  var grid3 = new Grid();
  grid3.ColumnDefinitions.Add(new ColumnDefinition { Width = new GridLength(1, GridUnitType.Star) });
  grid3.ColumnDefinitions.Add(new ColumnDefinition { Width = new GridLength(1, GridUnitType.Star) });
  var songAuthor = new Label();
  songAuthor.SetBinding(Label.TextProperty, new Binding("songAuthor"));
  var songSize = new Label();
  songSize.SetBinding(Label.TextProperty, new Binding("SongSize"));
  grid3.Children.Add(songAuthor);
  grid3.Children.Add(songSize, 1, 0);
  grid2.Children.Add(songTitle);
  grid2.Children.Add(grid3, 0, 1);
  var selectionImage = new Image()
  {
    IsVisible = true,
    Source = "Selected.png"
  };
  grid1.Children.Add(songThumbnail);
  grid1.Children.Add(grid2, 1, 0);
  grid1.Children.Add(selectionImage, 2, 0);
  return grid1;
});
{% endhighlight %}
{% endtabs %}

Download the entire source code from GitHub [here](https://github.com/SyncfusionExamples/Show-checked-circle-on-selected-items-in-xamarin.forms-listview).

![Multiple item selection in listview](SfListView_images/SfListView-Selection-2.png)

## Selected item style

### Selection background

The SfListView allows changing the selection background color for the selected items by using the [SfListView.SelectionBackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionBackgroundColor.html) property. You can also change the selection background color at runtime.

{% tabs %}
{% highlight c# %}
 <syncfusion:SfListView x:Name="listView"
                        SelectionBackgroundColor="Khaki"/>
{% endhighlight %}
{% highlight c# %}
listView.SelectionBackgroundColor = Color.Khaki;
{% endhighlight %}
{% endtabs %}

![Selection background color in listview](SfListView_images/SfListView-SelectionBackground.png)

### Programmatic animation

The SfListView allows programmatic animation in selection at runtime by using the virtual method [AnimateSelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SelectionController~AnimateSelectedItem.html) of [SelectionController](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionController.html) class.

{% tabs %}
{% highlight c# %}
listView.SelectionController = new SelectionControllerExt(listView);

public class SelectionControllerExt : SelectionController
{
   public SelectionControllerExt(SfListView listView) : base(listView)
   {
   }
   
   protected override void AnimateSelectedItem(ListViewItem selectedListViewItem)
   {
      base.AnimateSelectedItem(selectedListViewItem);
      selectedListViewItem.Opacity = 0;
      selectedListViewItem.FadeTo(1, 3000, Easing.SinInOut);
   }
}
{% endhighlight %}
{% endtabs %}

Download the entire source code from GitHub [here](https://github.com/SyncfusionExamples/Animate-items-programmatically-on-selection-in-xamarin.forms-listview).

![Selection animation in listview](SfListView_images/SfListView-SelectionAnimation.gif)

## Events

### SelectionChanging event

The [SelectionChanging](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanging_EV.html) event is raised while selecting an item at the execution time. [ItemSelectionChangingEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangingEventArgs.html) has the following members which provides the information for `SelectionChanging` event:

 * [AddedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangingEventArgs~AddedItems.html): Gets collection of the underlying data objects where the selection is going to process.
 * [RemovedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangingEventArgs~RemovedItems.html): Gets collection of the underlying data objects where the selection is going to remove.

You can cancel the selection process within this event by setting the `ItemSelectionChangingEventArgs.Cancel` property to true.

The `SelectionChanging` event is used for the following use case:

 * Disable the selection of the particular item based on the underlying data.

{% tabs %}
{% highlight c# %}
listView.SelectionChanging += ListView_SelectionChanging;  

private void ListView_SelectionChanging(object sender, ItemSelectionChangingEventArgs e)
{
  if (e.AddedItems.Count > 0 && e.AddedItems[0] == ViewModel.Items[0])
      e.Cancel = true;
}
{% endhighlight %}
{% endtabs %}

### SelectionChanged event

The [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanged_EV.html) event will occur once selection process has been completed for the selected item in the SfListView. [ItemSelectionChangedEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangedEventArgs.html) has the following members which provides information for `SelectionChanged` event:

 * [AddedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangedEventArgs~AddedItems.html): Gets collection of the underlying data objects where the selection has been processed.
 * [RemovedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangedEventArgs~RemovedItems.html): Gets collection of the underlying data objects where the selection has been removed.

 The `SelectionChanged` event used for the following use cases:
 
  * Clears all the selected item.
  * Removes the particular selected item.
  * Gets the index of the selected item.

{% tabs %}
{% highlight c# %}
listView.SelectionChanged += ListView_OnSelectionChanged;  

private void ListView_OnSelectionChanged(object sender, ItemSelectionChangedEventArgs e)
{
   listView.SelectedItems.Clear();
}
{% endhighlight %}
{% endtabs %}

N> [SelectionChanging](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanging_EV.html) and [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanged_EV.html) events will be triggered only on UI interactions.

## Key navigation

The [AllowKeyNavigation](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~AllowKeyboardNavigation.html) property enables navigation through keyboard buttons. When the `AllowKeyNavigation` property is `true`, navigation gets enabled. Otherwise, set to `false`. Behavior of key navigation in UWP and macOS are explained as follows :

* When the [SfListView.SelectionMode](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SelectionMode.html) is `Single`, the selected item is highlighted with `FocusBorderColor` around the item while key navigation.
* When the `SelectionMode` is `SingleDeSelect` or `Multiple`, the [FocusBorderColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~FocusBorderColor.html) will set to the `CurrentItem` only on key navigation. 
* If focusable elements i.e. `Entry`, `SearchBar`, etc. are loaded in the page, the `Focus` will not be changed either to other elements in the view or to the next [ListViewItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ListViewItem.html) when `Tab` or `Shift+Tab` key is pressed in the [LinearLayout](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.LinearLayout.html).
* In the [GridLayout](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.GridLayout.html) with span count greater than 1, the `FocusBorderColor` will navigate to the next or previous `ListViewItem` when pressing `Tab` or `Shift+Tab` key.
* In macOS, need to move the focus manually to perform key navigation.

### FocusBorderColor

[FocusBorderColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~FocusBorderColor.html) used to set the border color for the current focused item. For Android and iOS platform, the default color is `Color.Transparent` and for macOS and UWP platform, the default color is `Color.FromRgb(76, 161, 254)`.

### FocusBorderThickness

[FocusBorderThickness](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~FocusBorderThickness.html) used to set the border thickness for the current focused item. For Android and iOS platform, the default thickness is 0 and for macOS and UWP platform, the default thickness is 1.

## MacOS support

### Known issues

* If `SfListView` flings with more `inertia` or the scrollbar reaches either the bottom or top of the view, the listview items will not layout properly. Since, it occurs in simple custom control and `Xamarin.Forms.ListView`. So, a defect report is logged to `Bugzilla` team. Find the bug report: https://github.com/xamarin/Xamarin.Forms/issues/2403
* When `Grouping` is enabled, the listview items and group header items will not layout properly while scrolling the `SfListView`.
* Application will get crash when `Linker` option is set as `Link All`.
* If an `Image` is loaded in the [ItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ItemTemplate.html) property, it is necessary to define a definite size for the `Image`.

### Not yet implemented

The following features are not yet implemented due to some limitations in the `Xamarin.Forms.macOS` platform:

* [ScrollStateChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ScrollStateChanged_EV.html) event
* [Pull-To-Refresh](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfPullToRefresh.XForms~Syncfusion.SfPullToRefresh.XForms.SfPullToRefresh.html)

## How to

### Disable selection on particular item 

The selection of a particular set of items can be disabled based on the [SfListView.SelectedItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) of the underlying collections. 

{% tabs %}
{% highlight c# %}
public partial class MainPage : ContentPage
{
  public MainPage()
  {
    InitializeComponent();
  }

  private void listView_SelectionChanging(object sender, Syncfusion.ListView.XForms.ItemSelectionChangingEventArgs e)
  {
  if (e.AddedItems.Count > 0 && (e.AddedItems[0] as Contacts).Category == "Non-Selectable items")
      e.Cancel = true;
  }
}
{% endhighlight %}
{% endtabs %}

Download the entire sample from GitHub [here](https://github.com/SyncfusionExamples/Disable-selection-animation-on-particular-item-in-xamarin-forms-listview).

### Automatically scroll to bring a selected item into the view

To bring the [SfListView.SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html) automatically into the view when it changed at runtime by calling the [ScrollToRowIndex](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.LayoutBase~ScrollToRowIndex.html) method.  

In linear layout, you can get the row index of `SfListView.SelectedItem` and resolve if header and group header are used. 

{% tabs %}
{% highlight c# %}
public partial class MainPage : ContentPage
{
  public MainPage()
  {
    InitializeComponent();
    listView.PropertyChanged += listView_PropertyChanged;
  }

  private void listView_PropertyChanged(object sender, System.ComponentModel.PropertyChangedEventArgs e)
  {
    if (e.PropertyName == "SelectedItem")
    {
       var selectedItemIndex = listView.DataSource.DisplayItems.IndexOf(listView.SelectedItem);
       selectedItemIndex += (listView.HeaderTemplate != null && !listView.IsStickyHeader || !listView.IsStickyGroupHeader) ? 1 : 0;
       selectedItemIndex -= (listView.GroupHeaderTemplate != null && listView.IsStickyGroupHeader) ? 1 : 0;
       (listView.LayoutManager as LinearLayout).ScrollToRowIndex(selectedItemIndex);
    }
  }
}
{% endhighlight %}
{% endtabs %}

Download the entire sample from GitHub [here](https://github.com/SyncfusionExamples/Scroll-the-xamarin.forms-listview-to-bring-the-particular-item-in-view-).

### Gets the index of selected item

When performing selection, you can get the index of the selected item by using the [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanged_EV.html) event from the [DataSource.DisplayItems](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.DataSource.Portable~Syncfusion.DataSource.DisplayItems.html). 

{% tabs %}
{% highlight c# %}
public partial class MainPage : ContentPage
{
  public MainPage()
  {
    InitializeComponent();
    listView.SelectionChanged += ListView_SelectionChanged;
  }

  private void ListView_SelectionChanged(object sender, ItemSelectionChangedEventArgs e)
  {
    var items = e.AddedItems;
    var index = listView.DataSource.DisplayItems.IndexOf(items[0]);
    entry.Text = index.ToString();
  }
}
{% endhighlight %}
{% endtabs %}

Download the entire sample from GitHub [here](https://github.com/SyncfusionExamples/Get-the-index-of-selected-item-in-xamarin.forms-listview).

### Display selection when ItemTemplate contains image

When [ItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ItemTemplate.html) contains only image, then the selection color will not be visible in the view when select an image. To see selection, add any layout such as Grid or StackLayout above the image, and set margin or padding to it.

{% tabs %}
{% highlight xaml %}
<ContentPage xmlns:syncfusion="clr-namespace:Syncfusion.ListView.XForms;assembly=Syncfusion.SfListView.XForms">
  <syncfusion:SfListView
   ItemsSource="{Binding BookInfo}"
   ItemSize="100">  
    <syncfusion:SfListView.ItemTemplate>  
        <DataTemplate>  
            <Grid Margin="10">  
                <Image Source="{Binding Image}" Aspect="Fill"/>  
            </Grid>  
        </DataTemplate>  
    </syncfusion:SfListView.ItemTemplate>  
</syncfusion:SfListView>  
</ContentPage>
{% endhighlight %}
{% highlight c# %}
public partial class MainPage : ContentPage
{
    SfListView listView;
    public MainPage()
    {
        InitializeComponent();
        listView = new SfListView();
        listView.ItemSize = 100;
        listView.ItemsSource = viewModel.BookInfo;
        listView.ItemTemplate = new DataTemplate(() =>
        {
            var grid = new Grid() { Margin = 10 };
            var image = new Image() { Aspect = Aspect.Fill};
            image.SetBinding(Image.SourceProperty, new Binding("Image"));
            grid.Children.Add(image);
            return grid;
        });
        this.Content = listView;
    }
}
{% endhighlight %}
{% endtabs %}

## Limitation

* When a grid is loaded inside the [ItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~ItemTemplate.html) with background color, the [SelectionBackgroundColor](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionBackgroundColor.html) will not display. Because, it overlaps the `SelectionBackgroundColor`. In this case, set the background color for the ListView instead of `ItemTemplate`.
* When the ListView contains duplicated items in the collection, only the first item whose instance was created initially will be selected or deselected.