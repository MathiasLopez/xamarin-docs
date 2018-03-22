---
layout: post
title: Selection in SfListView
description: Describes about the selection behavior in SfListView.
platform: xamarin
control: SfListView
documentation: ug
---

# Selection

This section explains how to perform selection and its related operations in the SfListView.

## UI selection

The SfListView allows selecting items either programmatically or by touch interactions. To enable selection, set the [SelectionMode](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionMode.html) property value to other than `None`. The control has different selection modes to perform selection operations as listed as follows:

 * None: Allows disabling selection.
 * Single: Allows selecting single item only. When clicking on the selected item, selection not cleared. This is the default value for `SelectionMode`.
 * SingleDeselect: Allows selecting single item only. When clicking on the selected item, selection gets cleared.
 * Multiple: Allows selecting more than one item. Selection is not cleared when selecting more than one items. When you click on the selected item, selection gets cleared.

The SfListView allows selecting items on different gestures such as tap, double tap, and hold. This can be achieved by setting the [SelectionGesture](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionGesture.html). The default value for the `SelectionGesture` is [TouchGesture.Tap](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.TouchGesture.html).

{% highlight c# %}
listView.SelectionMode = SelectionMode.Multiple;
listView.SelectionGesture = TouchGesture.Hold;
{% endhighlight %}

The following screenshot shows the output rendered when the selection is performed on the items:

![](SfListView_images/SfListView-Selection-1.png)

## Programmatic selection

When the [SelectionMode](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionMode.html) is other than `None`, the item/items in the SfListView can be selected from the code by setting the [SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html), or adding items to the [SelectedItems](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) property based on the `SelectionMode`.

When the selection mode is `Single`, programmatically select an item by setting the underlying object to the `SelectedItem` property. 

{% highlight c# %}
//Perform selection using selected item
listView.SelectedItem = viewModel.Items[5];
{% endhighlight %}

When the selection mode is `Multiple`, programmatically select more than one item by adding the underlying object to the `SelectedItems` property. 

{% highlight c# %} 
//Perform multiple selection using selected items
listView.SelectedItems.Add (viewModel.Items [4]);
listView.SelectedItems.Add (viewModel.Items[5]);
{% endhighlight %}

All items of the SfListView can be selected using [SelectAll](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectAll.html) method.

{% highlight c# %} 
listView.SelectAll();
{% endhighlight %}

## Selected items

### Get selected items

The SfListView gets all selected items through the [SelectedItems](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) property. Also gets the single item by using [SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html) property.

### Clear selected items

The selected items can be cleared by calling the [SelectedItems.Clear()](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItems.html) method.

{% highlight c# %}
listView.SelectedItems.Clear();
{% endhighlight %}

### CurrentItem vs SelectedItem

The SfListView gets the selected item by using the [SelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItem.html) and [CurrentItem](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~CurrentItem.html) properties. Both `SelectedItem` and `CurrentItem` returns the same data object when single item is selected. When more than one items are selected, then the `SelectedItem` property returns the first selected item, and the `CurrentItem` property returns the last selected item.

W> If you set any item which is not available in `ItemsSource` to `SelectedItem` or `CurrentItem` property, exception will be thrown.

## Selected item customization 

### Show checked circle on selected items 

To customize the appearance of the selected item/items by using the appearance of [SelectedItemTemplate](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectedItemTemplate.html). The following customizations should give an idea to customize the appearance of selected items in the control: 

{% highlight xaml %}
<ContentPage>
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

Now run the application to render the following output. You can download the entire source code of this demo from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/CustomSelection-New-172474858).

![](SfListView_images/SfListView-Selection-2.png)

## Selected item style

### Selection background

To change the selection background color for the selected items by using BackgroundColor property in `SelectionItemTemplate`.

{% highlight xaml %}
<ContentPage>
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

You can download the entire sample from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/CustomSelection-SelectionBackground715901267). The following output rendered when the background color is set to the selected item:

![](SfListView_images/SfListView-Selection-3.png)

### Programmatic animation

The SfListView allows programmatic animation in selection at runtime by using the virtual method [AnimateSelectedItem](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SelectionController~AnimateSelectedItem.html) of `SelectionController` class.

To animate selection by override the AnimateSelectedItem method, follow the code example:

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

The screenshot shows the output of programmatic animation in selection. You can download the sample for above source code from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Programatic_Animation1251260296).

![](SfListView_images/SfListView-SelectionAnimation.gif)

## Events

### SelectionChanging event

The [SelectionChanging](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanging_EV.html) event is raised while selecting an item at the execution time before the item is selected. [ItemSelectionChangingEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangingEventArgs.html) has the following members which provides the information for `SelectionChanging` event:

 * AddedItems: Gets collection of the underlying data objects where the selection is going to process.
 * RemovedItems: Gets collection of the underlying data objects where the selection is going to remove.

You can cancel the selection process within this event by setting `ItemSelectionChangingEventArgs.Cancel` property to true.

To hook the `SelectionChanging` event, and cancel selection of an item, follow the code example:

{% highlight c# %}
listView.SelectionChanging += ListView_SelectionChanging;  

private void ListView_SelectionChanging(object sender, ItemSelectionChangingEventArgs e)
{
  if (e.AddedItems.Count > 0 && e.AddedItems[0] == ViewModel.Items[0])
      e.Cancel = true;
}
{% endhighlight %}

### SelectionChanged event

The [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanged_EV.html) event will occur once selection process has been completed for the selected item in the SfListView. [ItemSelectionChangedEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.ItemSelectionChangedEventArgs.html) has the following members which provides information for `SelectionChanged` event:

 * AddedItems: Gets collection of the underlying data objects where the selection has been processed.
 * RemovedItems: Gets collection of the underlying data objects where the selection has been removed.

{% highlight c# %}
listView.SelectionChanged += ListView_OnSelectionChanged;  

private void ListView_OnSelectionChanged(object sender, ItemSelectionChangedEventArgs e)
{
   listView.SelectedItems.Clear();
}
{% endhighlight %}

N> [SelectionChanging](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanging_EV.html) and [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/sflistview/Syncfusion.SfListView.XForms~Syncfusion.ListView.XForms.SfListView~SelectionChanged_EV.html) events will be triggered only on UI interactions.


## How to

### Disable selection on particular item 

To disable selection for a particular set of items based on the provided conditions in SelectionChanging event of SfListView. Get the tapped item data from the IList AddedItem of ItemSelectionChangingEventArgs using which you can check whether it satisfies the condition and disable the selection through Cancel property as like below code example.

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

You can download the entire sample from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/SfListViewSample1729548537).

### Automatically scroll to bring a selected item into the view

To bring the selected item automatically into the view when it changed at runtime by calling the ScrollToRowIndex method.  

In linear layout, you can get the row index of SelectedItem using the DisplayItems.IndexOf method and adjust the index based on header and group header like below code snippets.

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

You can download the entire sample from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/SfListViewSample-1451946805).