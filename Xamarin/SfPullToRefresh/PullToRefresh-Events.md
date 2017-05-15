---
layout: post
title: SfPullToRefresh Events | SfPullToRefresh | Xamarin | Syncfusion
description: How to use different events exposed in SfPullToRefresh.
platform: Xamarin.Forms 
control: SfPullToRefresh 
documentation: ug
---

# Events

There are three built-in events in the PullToRefresh control namely:

1. `Pulling`
2. `Refreshing`
3. `Refreshed`

The `Pulling` event will be notified whenever the swipe gesture is started. This event will notify the listener each and every time until the refresh content height exceeds. When we release the gesture from pullable content, `Refreshing` event will be triggered. Now the refresh operation can be performed. Once the content is refreshed, we should set `SfPullToRefresh.IsRefreshing` to `false` to stop the animation. Once the animation is stopped the `Refreshed` event will be triggered to notify that the refreshing is completed. 

## Pulling

`Pulling` event is triggered whenever you start pulling down on the `PullableContent` with `PullingEventArgs` that contains the following properties

* **Cancel** - You can cancel the pulling action based on the `Progress` value.
* **Progress** - Gets the progress completion value.

{% tabs %}
{% highlight c# %}
  pullToRefresh.Pulling += PullToRefresh_Pulling;

  private void PullToRefresh_Pulling(object sender, PullingEventArgs args)
  {
    args.Cancel = false;
    var progress = args.Progress;
  }
{% endhighlight %}
{%highlight Xaml%}

    <syncfusion:SfPullToRefresh x:Name="pullToRefresh" PullingEvent="PullToRefresh_Pulling" />

{%endhighlight%}

{% endtabs %}

## Refreshing

`Refreshing` event is triggered once pointer is released. This event will occur till the `IsRefreshing` property is set as `false`.

{% tabs %}

{% highlight c# %}

    pullToRefresh.Refreshing += PullToRefresh_Refreshing;
   
    private async void PullToRefresh_Refreshing(object sender, EventArgs args)
    {
        pullToRefresh.IsRefreshing = true;
        await Task.Delay(2000);
        pullToRefresh.IsRefreshing = false;
    }
{% endhighlight %}

{%highlight Xaml%}

    <syncfusion:SfPullToRefresh x:Name="pullToRefresh" RefreshingEvent="PullToRefresh_Refreshing" />

{%endhighlight%}


{% endtabs %}

## Refreshed

`Refreshed` event is triggered once the `Refreshing` event is completed.

{% tabs %}
{% highlight c# %}

    pullToRefresh.Refreshed += PullToRefresh_Refreshed;
    private void PullToRefresh_Refreshed(object sender , EventArgs args)
    {
        
    }

{% endhighlight %}

{%highlight Xaml%}

    <syncfusion:SfPullToRefresh x:Name=" pullToRefresh" RefreshedEvent="PullToRefresh_Refreshed" />

{%endhighlight%}

{% endtabs %}