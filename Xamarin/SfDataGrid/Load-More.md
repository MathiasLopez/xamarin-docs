---
layout: post
title: Load More | SfDataGrid | Xamarin | Syncfusion
description: How to perform load more and it's properties and customizations in a SfDataGrid.
platform: xamarin
control: SfDataGrid
documentation: UG
---
# Load More

The SfDataGrid allows enabling `LoadMore` option by setting the [SfDataGrid.AllowLoadMore](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~AllowLoadMore.html) property to `true`, and by setting the [SfDataGrid.LoadMoreCommand](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~LoadMoreCommand.html) property. When `LoadMore` is enabled, the control provides an option to load a subset of data to its data source at runtime using the [LoadMoreView](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.LoadMoreView.html). 

When the grid reaches maximum offset while scrolling down, an interactive load more view is displayed in view. On tapping the load more view, it triggers a command to add more data to the data source of the grid at runtime.

## LoadMoreCommand

The SfDataGrid allows loading records to its data source at runtime by triggering an `ICommand` binded to the `SfDataGrid.LoadMoreCommand` property. When tapping the load more view, if the `CanExecute` of the `ICommand` returns `true`, this command triggered to load the records at runtime.
 
Set the [SfDataGrid.IsBusy](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~IsBusy.html) property to `true` before loading the items to notify the grid, that more items are loaded to it. Set the property to `false` after loading the items to the grid. When loading the items, alter the time for the `LoadMore` animation from the sample by setting a delay based on the requirement.

To enable and load items at runtime, follow the code example:

{% highlight c# %}
//Enable load more in SfDataGrid
dataGrid.AllowLoadMore = true;
dataGrid.LoadMoreCommand = new Command(ExecuteLoadMoreCommand);
 
private async void ExecuteLoadMoreCommand()
{
    this.dataGrid.IsBusy = true;
    await Task.Delay(new TimeSpan(0, 0, 5));
    viewModel.LoadMoreItems ();
    this.dataGrid.IsBusy = false;
} 

//ViewModel.cs
private OrderInfoRepository order;
public ViewModel()
{
    SetRowsToGenerate(50);
}

//ItemsSource
private ObservableCollection<OrderInfo> ordersInfo;

public ObservableCollection<OrderInfo> OrdersInfo
{
    get { return ordersInfo; }
    set { this.ordersInfo = value; }
}

//ItemsSource Generator
public void SetRowsToGenerate(int count)
{
    order = new OrderInfoRepository();
    ordersInfo = order.GetOrderDetails(count);
}

public void LoadMoreItems()
{
    for (int i = 0; i < 20; i++)
        this.OrdersInfo.Add(order.GenerateOrder(OrdersInfo.Count + 1));
}

//OrderInfoRepository.cs
public ObservableCollection<OrderInfo> GetOrderDetails (int count)
{
    ObservableCollection<OrderInfo> orderDetails = new ObservableCollection<OrderInfo> ();

    for (int i = 10001; i <= count + 10000; i++) {
        var order = new OrderInfo () {
            OrderID = i,
            CustomerID = CustomerID [random.Next (7)],
            EmployeeID = random.Next (1700, 1800).ToString (),
            FirstName = FirstNames [random.Next (7)],
            LastName = LastNames [random.Next (7)]
        };
        orderDetails.Add (order);
    }
    return orderDetails;
} 

public OrderInfo GenerateOrder(int id)
{
    var order = new OrderInfo(){
        OrderID = (id + 10000),
        CustomerID = CustomerID [random.Next (15)],
        EmployeeID = random.Next (1700, 1800).ToString (),
        FirstName = FirstNames [random.Next (15)],
        LastName = LastNames [random.Next (15)],
    };
    return order;
}

//Main DataSources
string[] FirstNames = new string[] {
    "Kyle"
    "Gina",
    "Irene",
    "Katie",
    "Michael",
    "Oscar",
    "Ralph"
};

string[] LastNames = new string[] {
    "Adams",
    "Crowley",
    "Ellis",
    "Gable",
    "Irvine",
    "Keefe",
    "Mendoza"
};

string[] CustomerID = new string[] {
    "Adams",
    "Frans",
    "Katie",
    "Laura",
    "Wilson",
    "Andrew",
    "Lenny"
};
{% endhighlight %}

## Customize load more display text

Customize the text displayed in the `LoadMoreView` by setting the [SfDataGrid.LoadMoreText](http://help.syncfusion.com/cr/cref_files/xamarin/sfdatagrid/Syncfusion.SfDataGrid.XForms~Syncfusion.SfDataGrid.XForms.SfDataGrid~LoadMoreText.html) property as follows:

{% highlight c# %}
//setting load more text in SfDataGrid
dataGrid.LoadMoreText = "Load More Items"; 
{% endhighlight %}

## Customize LoadMoreView position

Customize the position in which the `LoadMoreView` is displayed to either `top` or `bottom` based on the requirements.
 
{% highlight c# %}
//Enable load more in SfDataGrid
dataGrid.LoadMorePosition = LoadMoreViewPosition.Bottom;  
{% endhighlight %}

## Customize LoadMoreView

The SfDataGrid also allows customizing the `LoadMoreView` based on the requirements. To do this, write custom `LoadMoreView` class inheriting from the `LoadMoreView`, and perform the `LoadMoreOperation` based on the requirement.

To customize the `LoadMoreView`, follow the code example:
 
{% highlight c# %}
public class CustomLoadMoreView : LoadMoreView
{
    private Button loadMoreView;

    public CustomLoadMoreView()
    {
        this.BackgroundColor = Color.Red;
        loadMoreView = new Button ();
        loadMoreView.Text = "LoadItems";
        this.Children.Add(loadMoreView);
        loadMoreView.Clicked += loadMoreView_Tapped;
    }

    void loadMoreView_Tapped (object sender, EventArgs e)
    {
        if (this.LoadMoreCommand != null)
        {
            this.LoadMoreCommand.Execute(null);
        }
    }

    protected override void LayoutChildren(double x, double y, double width, double height)
    {
        loadMoreView.Layout(new Rectangle(x, y, width, height));
    }
}
{% endhighlight %}

Running the application renders the following output.

![](SfDataGrid_images/LoadMore.png)