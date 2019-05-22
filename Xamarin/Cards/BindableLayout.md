---
layout: post
title: BindableLayout in Syncfusion.Xamarin.Forms SfCardLayout
description: How to bind SfCardView to SfCardLayout using BindableLayout
platform: xamarin
control: Cards
documentation: ug
---

# BindableLayout

From version 3.5, Xamarin.Forms has introduced a new approach, called BindableLayout, which works with all the layouts that are derived from Layout<T>.  By simply setting ItemTemplate and ItemsSource, BindableLayout creates a group of UI (for the given ItemTemplate) for every data in the ItemsSource.

Since [`SfCardLayout`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardLayout.html) is an extended class of Layout<T>, this approach is also possible for [`SfCardLayout`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardLayout.html).

## Initialize view model

Define a simple data model that represents data to be populated for [`SfCardLayout`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardLayout.html).

{% highlight c# %}

public class Model
{
   public IEnumerable<string> Colors { get; set; }
}

{% endhighlight %} 

Next, create a view model class and initialize a model object as demonstrated in the following code sample.

{% highlight c# %}

public class ViewModel 
{
        public Model Model { get; set; }

        public ViewModel()
        {
            Model = new Model
            {
                Colors = new string[]
                {
                    "Cyan", "Yellow", "Orange"
                }
            };
        }
 }

{% endhighlight %} 

Set the ViewModel instance as BindingContext of your page to bind properties of ViewModel to [`SfCardLayout`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardLayout.html). 

N> Add namespace of ViewModel class in your XAML page if you prefer to set BindingContext in XAML. 

{% tabs %} 

{% highlight xaml %}

<ContentPage.BindingContext>

        <local:ViewModel></local:ViewModel>

</ContentPage.BindingContext>

{% endhighlight %}

{% highlight c# %}

this.BindingContext = new ViewModel();      

{% endhighlight %}

{% endtabs %}

## Populate CardLayout with data

[`SfCardLayout`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardLayout.html) can be populated with data by setting the ItemSource property of BindableLayout to a collection of items that can be used in [`SfCardView`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardView.html).

{% tabs %} 

{% highlight xaml %}

<cards:SfCardLayout BindableLayout.ItemsSource="{Binding Model.Colors}">
…
</cards:SfCardLayout>

{% endhighlight %}

{% highlight c# %}

SfCardLayout cardLayout = new SfCardLayout();
BindableLayout.SetItemsSource(cardLayout, viewModel.Model.Colors);

{% endhighlight %}

{% endtabs %}

## Define the appearance of SfCardView

[`SfCardLayout`](https://help.syncfusion.com/cr/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardLayout.html) accepts only [`SfCardView`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardView.html) as its child. The appearance of each [`SfCardView`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Cards.XForms~Syncfusion.XForms.Cards.SfCardView.html) can be defined by setting the BindableLayout.ItemTemplate property.

{% highlight xaml %}

<cards:SfCardLayout BindableLayout.ItemsSource="{Binding Model.Colors}"  SwipeDirection="Left" VerticalOptions="Center"  HeightRequest="300" WidthRequest="300" BackgroundColor="#F0F0F0">
        <BindableLayout.ItemTemplate>
            <DataTemplate>
                <cards:SfCardView BackgroundColor="{Binding}">
                    <Label Text="{Binding}" HorizontalOptions="CenterAndExpand" VerticalTextAlignment="Center"/>
                </cards:SfCardView>
            </DataTemplate>
        </BindableLayout.ItemTemplate>
</cards:SfCardLayout>

{% endhighlight %}