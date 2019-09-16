---
layout: post
title: Getting Started with Syncfusion EffectsView
description: How to initialze a effects view.
platform: xamarin
control: SfEffectsView
documentation: ug
---

# Getting Started

This section explains the steps required to configure the effects view.

## Adding SfEffectsView reference

You can add SfEffectsView reference using one of the following methods:

**Method 1: Adding SfEffectsView reference from nuget.org**

Syncfusion Xamarin components are available in [nuget.org](https://www.nuget.org/). To add SfEffectsView to your project, open the NuGet package manager in Visual Studio, search for [Syncfusion.Xamarin.Core](https://www.nuget.org/packages/Syncfusion.Xamarin.Core), and then install it.

![Add Packages](Getting-Started_images/Reference.png)

N> Install the same version of SfEffectsView NuGet in all the projects. SfEffectsView supports only in Android and iOS. 

**Method 2: Adding SfEffectsView reference from toolbox**

Syncfusion also provides Xamarin Toolbox. Using this toolbox, you can drag the SfEffectsView control to the XAML page. It will automatically install the required NuGet packages and add the namespace to the page. To install Syncfusion Xamarin Toolbox, refer to [Toolbox](https://help.syncfusion.com/xamarin/utility#toolbox).

**Method 3: Adding SfEffectsView assemblies manually from the installed location**

If you prefer to manually reference the assemblies instead referencing from NuGet, add the following assemblies in respective projects.

Location : {Installed location}/{version}/Xamarin/lib

<table>
<tr>
<td>PCL</td>
<td>Syncfusion.Core.XForms.dll<br/>Syncfusion.Licensing.dll<br/></td>
</tr>
<tr>
<td>Android</td>
<td>Syncfusion.Core.XForms.dll<br/>Syncfusion.Core.XForms.Android.dll<br/>Syncfusion.Licensing.dll<br/></td>
</tr>
<tr>
<td>iOS</td>
<td>Syncfusion.Core.XForms.dll<br/>Syncfusion.Core.XForms.iOS.dll<br/>Syncfusion.Licensing.dll<br/></td>
</tr>
</table>

N> To know more about obtaining our components, refer to these links for [Mac](https://help.syncfusion.com/xamarin/introduction/download-and-installation/mac/) and [Windows](https://help.syncfusion.com/xamarin/introduction/download-and-installation/windows/).

I> Starting with v16.2.0.x, if you reference Syncfusion assemblies from the trial setup or from the NuGet feed, you also have to include a license key in your projects. Please refer to [Syncfusion license key](https://help.syncfusion.com/common/essential-studio/licensing/license-key/) to know about registering Syncfusion license key in your Xamarin application to use our components.

## Launching an application on each platform with SfEffectsView

To use the effects view inside an application, each platform application requires some additional configurations. The configurations vary from platform to platform and are discussed in the following sections:

N> If you are adding the references from toolbox, below steps are not needed.

### iOS

To launch the effects view in iOS, call the `SfEffectsViewRenderer.Init()` method in the FinishedLaunching overridden method of the AppDelegate class after the Xamarin.Forms framework has been initialized and before the `LoadApplication` method is called as demonstrated in the following code sample.

{% highlight C# %} 

public override bool FinishedLaunching(UIApplication app, NSDictionary options)
{
    global::Xamarin.Forms.Forms.Init();
    SfEffectsViewRenderer.Init();
    LoadApplication(new App());
    return base.FinishedLaunching(app, options);
} 

{% endhighlight %}

### Android

Android platform does not require any additional configuration to render the effects view control.

## Initializing effects view

Import the [`SfEffectsView`]() control namespace in respective page as demonstrated in the following code sample.

{% tabs %} 

{% highlight xaml %} 

xmlns:sfEffectsView="clr-namespace:Syncfusion.XForms.EffectsView;assembly=Syncfusion.Core.XForms"

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.XForms.EffectsView;

{% endhighlight %}

{% endtabs %}

Then initialze effects view as shown below,

{% tabs %} 

{% highlight xaml %} 

<sfEffectsView:SfEffectsView x:Name="EffectsView"  Margin="0,5,0,10" CornerRadius="0,25,0,25" 
                                                 RippleAnimationDuration="800">                        
    <Grid>
        <sfBorder:SfBorder BackgroundColor="#2196F3"  BorderColor="Transparent" BorderWidth="0">  		
        ...                   
        </sfBorder:SfBorder>
    </Grid>
</sfEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

SfEffectsView effectsView = new SfEffectsView();
effectsView.Margin = new Thickness(0, 5, 0, 10);
effectsView.CornerRadius = new Thickness(0, 25, 0, 25);
effectsView.RippleAnimationDuration = 800;

Grid grid = new Grid();

SfBorder border = new SfBorder();
border.BackgroundColor = Color.FromHex("#2196F3");
border.BorderColor = Color.Transparent;
border.BorderWidth = 0;
...
grid.Children.Add(border);

effectsView.Content = grid;

{% endhighlight %}

{% endtabs %}

![EffectsView Initialization](Getting-Started_images/RippleEffect.gif)
