---
layout: post
title: Column Sizer | SfDataGrid | Xamarin | Syncfusion
description: What are all the different ColumnSizer and how it works in a SfDataGrid.
platform: xamarin
control: SfDataGrid
documentation: ug
---

# Column Sizer

SfDataGrid allows you to apply `ColumnSizer` for the [GridColumn](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn.html) by setting the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnSizer.html) property. 

The following code example illustrates how to apply `ColumnSizer` in SfDataGrid.

{% tabs %}
{% highlight xaml %}
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="True"
                   ColumnSizer="None">
{% endhighlight %}
{% highlight c# %}
dataGrid.ColumnSizer = ColumnSizer.None;
{% endhighlight %}
{% endtabs %}

SfDataGrid applies width for all the `GridColumns` in the [SfDataGrid.Columns](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~Columns.html) collection based on the `SfDataGrid.ColumnSizer` property. Following are the lists of options available to set width of the columns.

* None
* LastColumnFill
* Star
* Auto


## ColumnSizer.None

No column sizing is applied when the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnSizer.html) is set to [None](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html). Columns are arranged in view based on the [SfDataGrid.DefaultColumnWidth](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~DefaultColumnWidth.html) property. This is the default value of the `SfDataGrid.ColumnSizer` property.

![](SfDataGrid_images/CoumnSizer_Img1.png)

## ColumnSizer.LastColumnFill

When the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnSizer.html) is [LastColumnFill](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html), the column width of the `GridColumns` are adjusted with respect to `SfDataGrid.DefaultColumnWidth` property. In case if the columns does not fill the entire view space, then the last column’s width fills the unoccupied space in the view.

{% tabs %}
{% highlight xaml %}
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="True"
                   ColumnSizer="LastColumnFill">
{% endhighlight %}
{% highlight c# %}
dataGrid.ColumnSizer = ColumnSizer.LastColumnFill;
{% endhighlight %}
{% endtabs %}

![](SfDataGrid_images/CoumnSizer_Img2.png)

## ColumnSizer.Star

When the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnSizer.html) is [Star](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html), all the `GridColumns` are adjusted an equal column width to fit within the view. Setting `ColumnSizer` to `Star` will disable the `HorizontalScrolling` in SfDataGrid.

{% tabs %}
{% highlight xaml %}
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="True"
                   ColumnSizer="Star">
{% endhighlight %}
{% highlight c# %}
dataGrid.ColumnSizer = ColumnSizer.Star;
{% endhighlight %}
{% endtabs %}

![](SfDataGrid_images/CoumnSizer_Img3.png)

## ColumnSizer.Auto

When the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnSizer.html) is [Auto](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html), the width of the `GridColumns` are adjusted based on the header text or cell contents.

{% tabs %}
{% highlight xaml %}
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="True"
                   ColumnSizer="Auto">
{% endhighlight %}
{% highlight c# %}
dataGrid.ColumnSizer = ColumnSizer.Auto;
{% endhighlight %}
{% endtabs %}

![](SfDataGrid_images/CoumnSizer_Img4.png)

N> If any column is specified a width explicitly using the [GridColumn.Width](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn~Width.html) property then that column is not considered ColumnSizing width and skipped while applying the ColumnSizer for grid columns.

## How to 

### Apply ColumnSizer for a particular column

You can apply column sizing to individual columns by using the [GridColumn.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn~ColumnSizer.html) property. The `GridColumn.ColumnSizer` property is also type of [ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html). If the `GridColumn.ColumnSizer` is not explicitly set to a value, then it takes the value of the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~ColumnSizer.html) and applies the width to the columns accordingly.

The following code example illustrates how to apply `ColumnSizer` for a particular column.

{% tabs %}
{% highlight xaml %}
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="True"
                   ColumnSizer="None">

<syncfusion:GridTextColumn MappingName="OrderID"
                           ColumnSizer = "Auto" />
{% endhighlight %}
{% highlight c# %}
GridTextColumn textColumn = new GridTextColumn();
textColumn.MappingName = "CustomerID";
textColumn.HeaderText = "Full Name";
textColumn.ColumnSizer = ColumnSizer.Auto;  
{% endhighlight %}
{% endtabs %}

### Fill remaining width for any column

`SfDataGrid` allows to fill the remaining width in view for any column using [GridColumn.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn~ColumnSizer.html) property.

The `GridColumn.ColumnSizer` has higher priority than the [SfDataGrid.ColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html) property. Hence the individual columns having the `GridColumn.ColumnSizer` property set will not be included in the column sizer calculations of the `SfDataGrid`. To fill the column with remaining width in view, set the `GridColumn.ColumnSizer` property as [ColumnSizer.LastColumnFill](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.ColumnSizer.html#). Refer to the following code example to acheive the same:

In the below code snippet, SfDataGrid is applied with `ColumnSizer.Star` and the second column is applied with `ColumnSizer.LastColumnFill`. Hence the second column will take up the remaining space after the other columns are rendered with star size.

{% tabs %}
{% highlight xaml %}
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="False"
                   ItemsSource="{Binding OrdersInfo}">

<sfgrid:SfDataGrid.Columns>
    <sfgrid:GridTextColumn MappingName="OrderID"/>
    <sfgrid:GridTextColumn MappingName="CustomerID" ColumnSizer="LastColumnFill"/>
    <sfgrid:GridTextColumn MappingName="Salary"/>
    <sfgrid:GridTextColumn MappingName="Country"/>
</sfgrid:SfDataGrid.Columns>
</sfgrid:SfDataGrid>
{% endhighlight %}
{% highlight c# %} 
SfDataGrid dataGrid;
ViewModel viewModel;
public MainPage()
{
    InitializeComponent();
    dataGrid = new SfDataGrid();
    viewModel = new ViewModel();
    dataGrid.AutoGenerateColumns = false;
    dataGrid.ItemsSource = viewModel.OrdersInfo;

    GridTextColumn orderIDColumn = new GridTextColumn();
    orderIDColumn.MappingName = "OrderID";

    GridTextColumn customerIDColumn = new GridTextColumn();
    customerIDColumn.MappingName = "CustomerID";
    customerIDColumn.ColumnSizer = ColumnSizer.LastColumnFill;

    GridTextColumn salaryColumn = new GridTextColumn();
    salaryColumn.MappingName = "Salary";

    GridTextColumn countryColumn = new GridTextColumn();
    countryColumn.MappingName = "Country";

    dataGrid.Columns.Add(orderIDColumn);
    dataGrid.Columns.Add(customerIDColumn);
    dataGrid.Columns.Add(salaryColumn);
    dataGrid.Columns.Add(countryColumn);
}
{% endhighlight %}
{% endtabs %}   

![](SfDataGrid_images/FillRemainigColumn_Forms.png)

### Refreshing ColumnSizer at runtime

To refresh the column sizing for `SfDataGrid.Columns` in runtime, use the [SfDataGrid.GridColumnSizer.Refresh](https://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumnSizer~Refresh(Boolean).html)() method.

Consider that `ColumnSizer.Auto` is applied to the SfDataGrid. If the underlying values are changed in run time, refresh the column sizer as shown below:

{% tabs %}
{% highlight xaml %}    
<StackLayout HorizontalOptions="Center" 
             Orientation="Vertical">
    <Button x:Name="button"
            Text="Refresh ColumnSizer"
            HeightRequest="100"
            HorizontalOptions="Center"
            Clicked="ColumnSizerChanged"/>
<sfgrid:SfDataGrid x:Name="dataGrid"
                   AutoGenerateColumns="True"
                   AllowEditing="True"
                   ColumnSizer="Auto"
                   ItemsSource="{Binding OrdersInfo}">
</sfgrid:SfDataGrid>
</StackLayout>
{% endhighlight %}
{% highlight c# %}  
private void ColumnSizerChanged(object sender, EventArgs e)
{
    //Refreshes the column sizer of the SfDataGrid
    dataGrid.GridColumnSizer.Refresh(true);
}    
{% endhighlight %}
{% endtabs %} 

![](SfDataGrid_images/RefreshColumnSizer_Forms.gif) 

### Resetting column width to apply ColumnSizer   

By default, the columns having the [GridColumn.Width](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumn~Width.html) property set will not be included for column sizer calculations of SfDataGrid. To include the width columns and reset the column sizer in runtime, set the `GridColumn.Width` property to double.NaN before calling the [SfDataGrid.GridColumnSizer.Refresh()](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumnSizer~Refresh(Boolean).html) method. Refer to the following code example to achieve the same:

{% tabs %}
{% highlight xaml %}
<StackLayout
    Orientation="Vertical">
    <Button x:Name="button"
        Text=" Reset ColumnWidth"
        TextColor="White"
        HeightRequest="50"
        BackgroundColor="Black"
        HorizontalOptions="Center"
        Clicked="ColumnSizerChanged"/>
    <sfgrid:SfDataGrid x:Name="dataGrid"
                    AllowEditing="True"
                    AutoGenerateColumns="False"
                    ItemsSource="{Binding OrdersInfo}">
        <sfgrid:SfDataGrid.Columns>
            <sfgrid:GridTextColumn MappingName="OrderID" Width="20"/>
            <sfgrid:GridTextColumn MappingName="CustomerID"/>
            <sfgrid:GridTextColumn MappingName="Salary"/>
            <sfgrid:GridTextColumn MappingName="Country"/>
        </sfgrid:SfDataGrid.Columns>
    </sfgrid:SfDataGrid>
</StackLayout>
{% endhighlight %}
{% highlight c# %}
private void ColumnSizerChanged(object sender, EventArgs e)
{
    //Resets the widths for the columns having GridColumn.Width property set
    ResetColumnsWidth(); 
    dataGrid.GridColumnSizer.Refresh(true);
}
private void ResetColumnsWidth()
{
    foreach (var column in dataGrid.Columns)
    {
        // Setting NaN values to columns for which width is applied
        if (!double.IsNaN(column.Width))
        {
            column.Width = double.NaN;
        }
    }
}
{% endhighlight %}

![](SfDataGrid_images/Reset_ColumnWidth_Forms.png)

## Star column sizer ratio support

To customize the `ColumnSizer.Star` width calculation, write a custom GridColumnSizer class derived from [GridColumnSizer](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumnSizer.html) and assign it to the `SfDataGrid.ColumnSizer` property. To implement your own logic to divide the column widths in different ratios, override the [SetStarWidthForColumns](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.GridColumnSizer~SetStarWidthForColumns.html) method in your custom GridColumnSizer class.

To set star sizer ratio for individual column, follow the code example:

{% tabs %}
{% highlight c# %}
<sfgrid:SfDataGrid.Columns >
<sfgrid:GridTextColumn HeaderText="OrderID"  MappingName="OrderID" local:StarSizerRatioHelpers.ColumnRatio="2"/>
<sfgrid:GridTextColumn HeaderText="CustomerID" MappingName="CustomerID" local:StarSizerRatioHelpers.ColumnRatio="3"/>
<sfgrid:GridTextColumn HeaderText="Salary" MappingName="Salary"/>
<sfgrid:GridTextColumn HeaderText="Country" MappingName="Country"/>
</sfgrid:SfDataGrid.Columns>
{% endhighlight %}

The following code example demonstrates how the width is calculated for column using the `SetStarWidthForColumns` method based on the `ColumnRatio` property of the `StarSizerRatioHelpers` class:

{% highlight c# %}   
// Assign custom GridColumnSizer to datagrid GridColumnSizer
dataGrid.GridColumnSizer = new CustomColumnSizer(this.dataGrid);
public class CustomColumnSizer : GridColumnSizer
{
    public CustomColumnSizer(SfDataGrid grid) : base(grid)
    {
    }
    protected override void SetStarWidthForColumns(double columnsWidth, IEnumerable<GridColumn> columns)
    {
        var removedColumn = new List<GridColumn>();
        var column = columns.ToList();
        var totalRemainingStarValue = columnsWidth;
        double removedWidth = 0;
        bool isremoved;
        while (column.Count > 0)
        {
            isremoved = false;
            removedWidth = 0;
            var columnsCount = 0;
            foreach (var data in column)
            {
                columnsCount += StarSizerRatioHelpers.GetColumnRatio(data);
            }
            double starWidth = Math.Floor((totalRemainingStarValue / columnsCount));
            var getColumn = column.First();
            
            //Calculate the ColumnSizer ratio for every column 
            starWidth *= StarSizerRatioHelpers.GetColumnRatio(getColumn);
            var columnSizer = DataGrid.GridColumnSizer;
            var method = columnSizer.GetType().GetRuntimeMethods().FirstOrDefault(x => x.Name == "SetColumnWidth");
            var width = method.Invoke(columnSizer, new object[] { getColumn, starWidth });
            double computeWidth = (double)width;

            if (starWidth != computeWidth && starWidth > 0)
            {
                isremoved = true;
                column.Remove(getColumn);
                foreach (var remColumn in removedColumn)
                {
                    if (!column.Contains(remColumn))
                    {
                        removedWidth += remColumn.ActualWidth;
                        column.Add(remColumn);
                    }
                }
                removedColumn.Clear();
                totalRemainingStarValue += removedWidth;
            }
            totalRemainingStarValue = totalRemainingStarValue - computeWidth;
            if (!isremoved)
            {
                column.Remove(getColumn);
                if (!removedColumn.Contains(getColumn))
                    removedColumn.Add(getColumn);
            }
        }
    }
}
{% endhighlight %}   

The following code example explains the `StarSizerRatioHelpers` class:

{% highlight c# %} 
public static class StarSizerRatioHelpers
{
    public static int GetColumnRatio(BindableObject obj)
    {
        return (int)obj.GetValue(ColumnRatioProperty);
    }
    public static void SetColumnRatio(BindableObject obj, int value)
    {
        obj.SetValue(ColumnRatioProperty, value);
    }

    public static readonly BindableProperty ColumnRatioProperty =
        BindableProperty.Create("ColumnRatio", typeof(int), typeof(StarSizerRatioHelpers), 1, BindingMode.TwoWay);
    public static void OnColumnSizerChanged(BindableObject bindable, object oldValue, object newValue)
    {

    }
}  
{% endhighlight %}   

![](SfDataGrid_images/StarColumnSizerRatio_Forms.png)