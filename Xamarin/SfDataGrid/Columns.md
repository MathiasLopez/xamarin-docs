---
layout: post
title: Columns | SfDataGrid | Xamarin | Syncfusion
description: How to create and add columns, different ways to create columns and its customizations in a SfDataGrid.
platform: xamarin
control: SfDataGrid
documentation: UG
---

# Columns 

SfDatagrid allows you to create and add Columns in two ways:

* Automatic Columns generation based on the underlying collection.
* Manually defining columns in XAML or C#.

## Automatic Columns Generation

The SfDataGrid creates columns automatically based on the property [SfDataGrid.AutoGenerateColumns](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AutoGenerateColumns.html). It is a bindable property and it decides columns generation for SfDataGrid based on the [SfDataGrid.AutoGenerateColumnsMode](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AutoGenerateColumnsMode.html) property. 

`SfDataGrid.AutoGenerateColumnsMode` decides a way to create columns when `SfDataGrid.AutoGenerateColumns` is set to `true`. It also decides whether to retain the grouping and sorting when [ItemsSource](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ItemsSource.html) is changed. 

The `SfDataGrid.AutoGenerateColumnsMode` is of type [AutoGenerateColumnsMode](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AutoGenerateColumnsMode.html) which has the following five options.

<table>
<tr>
<th> Modes </th>
<th> Description </th>
</tr>
<tr>
<td> {{'[None](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.AutoGenerateColumnsMode.html)'| markdownify }} </td>
<td> Stores only the columns that are defined in SfDataGrid.Columns collection.<br/> When changing the ItemsSource, the grouping and sorting for explicitly defined SfDataGrid.Columns alone will be retained. </td>
</tr>
<tr>
<td> {{'[Reset](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.AutoGenerateColumnsMode.html)'| markdownify }} </td>
<td> Retains the columns defined explicitly in the application level and creates columns newly for all the other properties in a data source.<br/> When changing the ItemsSource, the grouping and sorting for explicitly defined SfDataGrid.Columns alone will be retained. </td>
</tr>
<tr>
<td> {{'[ResetAll](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.AutoGenerateColumnsMode.html)'| markdownify }}  </td>
<td> When changing the ItemsSource, the columns for the previous data source are cleared and the columns will be created newly for the new data source. Even when columns are explicitly defined it does not consider the defined columns and creates the column based on the underlying collection.<br/> Further, when changing the ItemsSource, the grouping and sorting for all the columns will be cleared. </td>
</tr>
<tr>
<td>  {{'[RetainOld](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.AutoGenerateColumnsMode.html)'| markdownify }}  </td>
<td> When changing the ItemsSource, creates columns for all fields in a data source when the Grid does not have any explicit definition for columns. When columns are defined explicitly, then the defined columns alone are retained and new columns are not created.<br/>Similarly, when changing the ItemsSource and when the Grid have any explicit definition for columns, the grouping and sorting are retained as it is </td>
</tr>
<tr>
<td>  {{'[SmartReset](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.AutoGenerateColumnsMode.html)'| markdownify }}  </td>
<td> Retains the columns defined explicitly in application level and the columns with MappingName identical to the properties in the new data source. Creates columns newly for all the other properties in the data source.<br/> Similarly, it retains the grouping and sorting of the columns that are defined explicitly in application level and the columns with MappingName identical to the properties in new data source </td>
</tr>
</table>

The default value of `SfDatagrid.AutoGenerateColumns` property is `true` and `SfDatagrid.AutoGenerateColumnsMode` is `Reset`. Hence by default SfDatagrid creates columns automatically for every non-explicitly defined public property in the underlying collection bound to its `ItemsSource` property.

N> When you change items source for SfDatagrid during run time, then the columns are generated on the basis of option set for `SfDataGrid.AutoGenerateColumnsMode`.

### Customize Automatically Generated Columns

When `SfDatagrid.AutoGenerateColumns` is `true`, then [SfDataGrid.AutoGeneratingColumn](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AutoGeneratingColumn_EV.html) event is raised for each GridColumn. This event receives two arguments namely sender which is the SfDatagrid and [AutoGeneratingColumnArgs](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.AutoGeneratingColumnArgs.html).
The `AutoGeneratingColumnArgs` object contains the following property:

* Column: This property returns the created column using which you can customize the column.
* Cancel: This property cancels the column creation.

You can skip generating a column by handling the `SfDataGrid.AutoGeneratingColumn` event as shown below.

{% highlight c# %}
dataGrid.AutoGeneratingColumn += GridAutoGeneratingColumns; 

void GridAutoGeneratingColumns(object sender, AutoGeneratingColumnArgs e)
{
    if (e.Column.MappingName == "EmployeeID")
        e.Cancel = true;
}
{% endhighlight %}

You can also apply formatting for auto generated columns as shown below.

{% highlight c# %}
void GridAutoGeneratingColumns(object sender, AutoGeneratingColumnArgs e)
{
    if (e.Column.MappingName == "Freight") {
        e.Column.Format = "C";
        e.Column.CultureInfo = new CultureInfo ("en-US");
    } else if (e.Column.MappingName == "ShippingDate")
        e.Column.Format = "dd/MM/yyyy";
} 
{% endhighlight %}

You can also customize a column’s header text, sorting, alignment, padding, etc. by handling the `SfDataGrid.AutoGeneratingEvent`.


## Manually generate Columns

SfDatagrid also allows you to define the columns manually by adding the GridColumn objects to the [SfDatagrid.Columns](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.Columns.html) collection. In case if you want only the manually defined columns to be in view, then you can achieve it by setting the [SfDatagrid.AutoGenerateColumns](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AutoGeneratingColumn_EV.html) property to `false`. There are different types of columns available in SfDatagrid and you can create any column based on your requirements from both XAML and code.
 
The following code example illustrates about creating columns manually in SfDatagrid

{% tabs %}
{% highlight xaml %}
<syncfusion:SfDataGrid x:Name="dataGrid"
            ColumnSizer="Star"
            AutoGenerateColumns="False"
            ItemsSource="{Binding OrderInfoCollection}">

    <syncfusion:SfDataGrid.Columns x:TypeArguments="syncfusion:Columns">
        <syncfusion:GridTextColumn HeaderText="Order ID" 
                                   MappingName="OrderID" />
        <syncfusion:GridTextColumn HeaderText="Customer ID"
                                   MappingName="CustomerID" />
        <syncfusion:GridTextColumn MappingName="Customer" />
        <syncfusion:GridTextColumn HeaderText="Ship Country"
                                   MappingName="ShipCountry" />
    </syncfusion:SfDataGrid.Columns>
</syncfusion:SfDataGrid>
{% endhighlight %}

{% highlight c# %}
dataGrid.AutoGenerateColumns = false;

GridTextColumn orderIdColumn = new GridTextColumn ();
orderIdColumn.MappingName = "OrderID";
orderIdColumn.HeaderText = "Order ID";

GridTextColumn customerIdColumn = new GridTextColumn ();
customerIdColumn.MappingName = "CustomerID";
customerIdColumn.HeaderText = "Customer ID";

GridTextColumn customerColumn = new GridTextColumn ();
customerColumn.MappingName = "Customer";

GridTextColumn countryColumn = new GridTextColumn ();
countryColumn.MappingName = "ShipCountry";
countryColumn.HeaderText = "Ship Country";

dataGrid.Columns.Add (orderIdColumn);
dataGrid.Columns.Add (customerIdColumn);
dataGrid.Columns.Add (customerColumn);
dataGrid.Columns.Add (countryColumn); 
{% endhighlight %}

{% endtabs %}

## Resizing Columns
SfDataGrid allows to resize the columns by tapping and dragging the right border of the column headers. Resizing can be enabled or disabled by setting [SfDataGrid.AllowResizingColumn](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AllowResizingColumn.html) property. A resizing indicator is displayed while resizing a column.

N> Resizing considers [GridColumn.MinimumWidth](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn~MinimumWidth.html) and [GridColumn.MaximumWidth](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn~MaximumWidth.html) of the column and will not resize past the minimum and maximum width constraints.

{% tabs %}
{% highlight xaml %}
<syncfusion:SfDataGrid  x:Name="dataGrid"
                        AllowResizingColumns="True"
                        AutoGenerateColumns="True"
                        ItemsSource="{Binding Orders}" />
{% endhighlight %}
{% highlight c# %}
dataGrid.AllowResizingColumn = true;
{% endhighlight %}
{% endtabs %}

![](SfDataGrid_images/Resizing_HitTest_Forms.png)
![](SfDataGrid_images/Resizing_Forms.png)

You can change the column width by tapping and dragging the resizing indicator.

N> The resizing indicator appears when you tap the right corner of the column header.

You can interactively hide a column by setting the `GridColumn.MinimumWidth` property to zero and resizing the column to a width less than 0.

### Resizing Modes

SfDataGrid allows two modes of resizing, which can be set using the [SfDataGrid.ResizingMode](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ResizingMode.html) property. The available resizing modes are,

* OnMoved - The resizing indicator is moved based on the touch point and the width of the column is updated as the resizing indicator moves.
* OnTouchUp - The resizing indicator is moved based on the touch point but however the width of the column is updated only on a touch up operation.

N> The default resizing mode is OnMoved.

The below image shows the resizing mode OnMoved
![](SfDataGrid_images/Resizing_OnMoved.png)

The below image shows the resizing mode OnTouchUp
![](SfDataGrid_images/Resizing_OnTouchUp.png)

### Resizing Events

The resizing operation can be handled based on the requirement using [SfDataGrid.ColumnResizing](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnResizing_EV.html) event. The `SfDataGrid.ColumnResizing` event is fired upon starting to resize a column and will be continuously fired till the resizing operation ends.
By handling the `SfDataGrid.ColumnResizing` event you can also cancel the resizing of a particular column.
The `SfDataGrid.ColumnResizing` event provides the following properties through [GridResizingEventArgs](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridResizingEventArgs.html).

* [Index](https://msdn.microsoft.com/en-us/library/office/ff768335.aspx) - Returns the index of the column currently being resized.
* NewValue - Returns the current width of the column being resized.
* ResizingState - Returns the current state of the user-interaction through a value from the ProgressStates enum.
* [Cancel](https://msdn.microsoft.com/query/dev10.query?appId=Dev10IDEF1&l=EN-US&k=k(System.ComponentModel.CancelEventArgs.Cancel)&rd=true) - A Boolean property to cancel the event and the resizing operation. 

### How To

#### Cancel resizing for a column

You can cancel resizing for a particular column using the `SfDataGrid.ColumnResizing` event. You can cancel the resizing operation of a column based on the different arguments provided in the `GridResizingEventArgs`. 

The below code example shows how to cancel resizing for a column using the `SfDataGrid.ColumnResizing` event using the `Index` value. 

{% highlight c# %}
    this.dataGrid.ResizingColumns += dataGrid_ResizingColumns;
    private void DataGrid_ColumnResizing(object sender, GridResizingEventArgs e)
        {
            //Code to end resizing if ColumnIndex is 2
            if (e.Index == 2)
                e.Cancel = true;
        }
{% endhighlight %}

The below code example shows how to cancel resizing for a column using the `SfDataGrid.ColumnResizing` event using the `NewValue` value. 

{% highlight c# %}
    this.dataGrid.ResizingColumns += dataGrid_ResizingColumns;
    private void DataGrid_ColumnResizing(object sender, GridResizingEventArgs e)
        {
            //Code to end resizing if Column's Width is >= 100
            if (e.NewValue >= 100 ||)
                e.Cancel = true;
        }
{% endhighlight %}

The below code example shows how to cancel resizing for a column using the `SfDataGrid.ColumnResizing` event using the `ProgressStates` value. 

{% highlight c# %}
    this.dataGrid.ResizingColumns += dataGrid_ResizingColumns;
    private void DataGrid_ColumnResizing(object sender, GridResizingEventArgs e)
        {
            //Code to end resizing if interaction state is Progressing
            if (e.ResizingState = ProgressStates.Progressing)
                e.Cancel = true;
        }
{% endhighlight %}
