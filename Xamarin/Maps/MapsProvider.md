---
layout: post
title: Maps provider of Syncfusion Maps control for Xamarin.Forms 
description: Describes the maps provider support in SfMaps control
platform: xamarin
control: SfMaps 
documentation: ug
---

# Map Providers

The maps control supports map providers such as OpenStreetMap and Bing Maps that can be added to an imagery layer in maps.

## OpenStreetMap

The OpenStreetMap (OSM) is a world map; it was built by a community of mappers. It is free to use under an open license. This allows you view geographical data in a collaborative way from anywhere on the earth. The OSM provides small tile images based on your requests and combines them into a single image to display the map area in the maps control. 

### Adding OSM in maps

The maps control uses `imagery layer` to display the tile images from the OSM service. To use `OSM`, add an imagery layer in maps’ layers collection.

{% tabs %}

{% highlight xml %}

        <maps:SfMaps.Layers>
            <maps:ImageryLayer/>
        </maps:SfMaps.Layers>

{% endhighlight %}

{% highlight c# %}

        SfMaps maps = new SfMaps();
        ImageryLayer layer = new ImageryLayer();
        maps.Layers.Add(layer);

{% endhighlight %}

{% endtabs %}

![Xamarin OSM image](Images/OSM.png)

N> Both the [`ShapeFileLayer`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ShapeFileLayer.html) and `ImageryLayer` have been derived commonly from MapsLayer.

## Bing Maps

The Bing Maps is a world map owned by Microsoft. As OSM, Bing Maps also provides map tile images based on your requests and combines them into a single image to display the map area. To use `Bing maps`, set the `LayerType` property of ImageryLayer to “Bing”. Then, set the Bing Maps key, which is obtained from [Bing Maps Key](https://www.microsoft.com/en-us/maps/create-a-bing-maps-key).

{% tabs %}

{% highlight xml %}

    <maps:SfMaps.Layers>
        <maps:ImageryLayer LayerType="Bing" BingMapKey="Your bing map key"/>
    </maps:SfMaps.Layers>

{% endhighlight %}

{% highlight c# %}

    SfMaps maps = new SfMaps();
    ImageryLayer layer = new ImageryLayer();
    layer.LayerType = LayerType.Bing;
    layer.BingMapKey = "Your bing map key";
    maps.Layers.Add(layer);

{% endhighlight %}

{% endtabs %}

![Xamarin Bing road image](Images/Road.png)

N> The `LayerType` property of `ImageryLayer` provides support to `OSM` and `Bing Maps`. The default value of the `LayerType` property is OSM.

## Set different bing map style

The ImageryLayer provides support to the following types of Bing Maps:

* `Road`
* `Aerial`
* `AerialWithLabels`

The desired style for the Bing Maps can be set using the `BingMapStyle` property of ImageryLayer. The default value of `BingMapStyle` is "Road".

### Road

The Road view displays the default map view of roads, buildings, and geography. The default value of the `BingMapStyle` property of imagery layer is "Road".

### Aerial

The Aerial view displays the satellite images to highlight the roads and major landmarks for easy identification. The aerial view can be applied to maps by setting the `BingMapStyle` to "Aerial".

{% tabs %}

{% highlight xml %}

        <maps:SfMaps.Layers>
            <maps:ImageryLayer LayerType="Bing" 
                            BingMapStyle="Aerial"
                            BingMapKey=" Your bing map key "/>
        </maps:SfMaps.Layers>

{% endhighlight %}

{% highlight c# %}

        SfMaps maps = new SfMaps();
        ImageryLayer layer = new ImageryLayer();
        layer.LayerType = LayerType.Bing;
        layer.BingMapStyle = BingMapStyle.Aerial;
        layer.BingMapKey = "Your bing map key ";
        maps.Layers.Add(layer);

{% endhighlight %}

{% endtabs %}

![Xamarin Bing aerial image](Images/aerial.jpg)

## AerialWithLabel

The AerialWithLabel view displays the Aerial map with labels for continent, country, ocean, etc. This view can be applied to maps by setting the `BingMapStyle` to "AerialWithLabel".

{% tabs %}

{% highlight xml %}

        <maps:SfMaps.Layers>
            <maps:ImageryLayer LayerType="Bing" 
                            BingMapStyle="AerialWithLabels"
                            BingMapKey=" Your bing map key "/>
        </maps:SfMaps.Layers>

{% endhighlight %}

{% highlight c# %}

        SfMaps maps = new SfMaps();
        ImageryLayer layer = new ImageryLayer();
        layer.LayerType = LayerType.Bing;
        layer.BingMapStyle = BingMapStyle.AerialWithLabels;
        layer.BingMapKey = "Your bing map key ";
        maps.Layers.Add(layer);

{% endhighlight %}

{% endtabs %}

![Xamarin Bing aerialwithlabel image](Images/aerialWithLabel.jpg)

## Zooming and panning

The maps control provides interactive zooming and panning supports to OSM and Bing Maps.

Zooming helps you get a closer look of an area on maps for in-depth analysis. Panning helps you move a map around to focus the targeted area. You can perform zooming and panning with the pinching gesture in a map area.

![Xamarin Zooming image](Images/zooming.jpg)

## Reset zooming

The ImageryLayer provides support to reset the maps to the default view when you double tap the imagery layer by setting the `ResetOnDoubleTap` property to true. The default value of this property is true. This behavior can be restricted by setting the `ResetOnDoubleTap` property to false.

{% tabs %}

{% highlight xml %}

        <maps:SfMaps>
        <maps:SfMaps.Layers>
                <maps:ImageryLayer ResetOnDoubleTap="True"/>
            </maps:SfMaps.Layers>
        </maps:SfMaps>

{% endhighlight %}

{% highlight c# %}

        SfMaps maps = new SfMaps();
        ImageryLayer layer = new ImageryLayer();
        layer.ResetOnDoubleTap = true;
        maps.Layers.Add(layer);

{% endhighlight %}

{% endtabs %}

## Set Geo coordinates points(center position)

The `GeoCoordinates` property allows you view the desired area at the center on loading. By default, the `GeoCoordinates` value is (0,0). So, the latitude value "0" and longitude value "0" are shown at the center.

{% tabs %}

{% highlight xml %}

        <maps:SfMaps ZoomLevel="2">
                <maps:SfMaps.Layers>
                    <maps:ImageryLayer GeoCoordinates="69.07,-37.08"/>
                </maps:SfMaps.Layers>
            </maps:SfMaps>

{% endhighlight %}

{% highlight c# %}

  SfMaps maps = new SfMaps();
  maps.ZoomLevel = 2;
  ImageryLayer layer = new ImageryLayer();
  layer.GeoCoordinates = new Point(69.07, -37.08);
  maps.Layers.Add(layer);


{% endhighlight %}

{% endtabs %}

![Xamarin Coordinate image](Images/Coordinate.png)

{% tabs %}

{% highlight xml %}

        <maps:SfMaps ZoomLevel="2">
            <maps:SfMaps.Layers>
                <maps:ImageryLayer GeoCoordinates="0,0"/>
            </maps:SfMaps.Layers>
        </maps:SfMaps>

{% endhighlight %}

{% highlight c# %}

  SfMaps maps = new SfMaps();
  maps.ZoomLevel = 2;
  ImageryLayer layer = new ImageryLayer();
  layer.GeoCoordinates = new Point(0,0);
  maps.Layers.Add(layer);

{% endhighlight %}

{% endtabs %}

![Xamarin center image](Images/Center.png)

## Set markers in imagery layer

As [`ShapeFileLayer`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ShapeFileLayer.html), markers also can be added to imagery layer. Markers can be customized using the `MarkerSettings` property in imagery layer.
The detailed explanation of marker and its customization have been provided in Markers section.

{% tabs %}

{% highlight xml %}

        <maps:ImageryLayer  >
            <maps:ImageryLayer.MarkerSettings>
                <maps:MapMarkerSetting IconColor="Red" 
                                    IconSize="13" MarkerIcon="Diamond"/>
            </maps:ImageryLayer.MarkerSettings>
                        <maps:ImageryLayer.Markers>
                            <maps:MapMarker  Label="United States" Latitude="40"
                                            Longitude= "-101"/>
                            <maps:MapMarker Label="Brazil" Latitude="-15.7833" 
                                            Longitude= "-52" />
                            <maps:MapMarker Label="Congo" Latitude="-1.6" 
                                            Longitude= "24.4" />
                            <maps:MapMarker Label="Kazakhstan" Latitude="49.9" 
                                            Longitude= "72.23" />
                            <maps:MapMarker Label="Australia" Latitude="-20.54"
                                            Longitude= "134.10" />
                    </maps:ImageryLayer.Markers>
                </maps:ImageryLayer>

{% endhighlight %}

{% highlight c# %}

            ImageryLayer layer = new ImageryLayer();
            layer.MarkerSettings = new MapMarkerSetting();
            layer.MarkerSettings.IconColor = Color.Red;
            layer.MarkerSettings.MarkerIcon = MapMarkerIcon.Diamond;
            layer.MarkerSettings.IconSize = 13;
            MapMarker marker1 = new MapMarker();
            marker1.Label = "United States";
            marker1.Latitude = "40";
            marker1.Longitude = "-101";
            layer.Markers.Add(marker1);
            MapMarker marker2 = new MapMarker();
            marker2.Label = "Brazil";
            marker2.Latitude = "-15.7833";
            marker2.Longitude = "-52";
            layer.Markers.Add(marker2);
            MapMarker marker3 = new MapMarker();
            marker3.Label = "Congo";
            marker3.Latitude = "-1.6";
            marker3.Longitude = "24.4";
            layer.Markers.Add(marker3);
            MapMarker marker4 = new MapMarker();
            marker4.Label = "Kazakhstan";
            marker4.Latitude = "49.9";
            marker4.Longitude = "72.23";
            layer.Markers.Add(marker4);
            MapMarker marker5 = new MapMarker();
            marker5.Label = "Australia";
            marker5.Latitude = "-20.54";
            marker5.Longitude = "134.10";
            layer.Markers.Add(marker5);

{% endhighlight %}

{% endtabs %}

![Xamarin Marker image](Images/Marker.png)

## Custom map providers

You can show the other map providers maps using imagery layer. First, initialize the map extension class, override the GetUri method of imagery layer extension class, and then pass the Map providers tile image Uri link like Google uri with corresponding x, y, and zoom level. Finally, add the imagery layer extension class to layers collection of native map control by overriding the OnElementChanged method of each platform’s (Xamarin.Android, Xamarin.iOS, and UWP) custom map renderer. For more information to add custom map provider, refer to this [`KB article`](https://www.syncfusion.com/kb/8913/display-google-map-in-xamarin-forms-sfmaps-control).

{% highlight c# %}

public partial class MainPage : ContentPage
{
	public MainPage()
	{
        InitializeComponent();
        MapExt maps = new MapExt();
        ImageryLayer layer = new ImageryLayer();
        maps.Layers.Add(layer);
        this.Content = maps;
    }
}

public class MapExt : SfMaps
{
}

public class CustomMapRenderer : SfMapsRenderer
{
    protected override void OnElementChanged(ElementChangedEventArgs<SfMaps> e)
    {
        base.OnElementChanged(e);
        if (Control != null)
                AddLayer();
    }

   
    void AddLayer()
    {
        ImageryLayerExt layer = new ImageryLayerExt();
        (Control as NativeMap.SfMaps).Layers.Clear();
        (Control as NativeMap.SfMaps).Layers.Add(layer as NativeMap.ImageryLayer);
    }
}

public class ImageryLayerExt : NativeMap.ImageryLayer
{
 
    protected override string GetUri(int X, int Y, int Scale)
    {
        var link = "http://mt1.google.com/vt/lyrs=y&x=" + X.ToString()
        + "&y=" + Y.ToString() + "&z=" + Scale.ToString();
        return link;
    }
}

{% endhighlight %}

![Xamarin custom map provider image](Images/custom_map_provider.jpg)

You can download the demo sample in this [`link`](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Google_Sample992378333).

## Cache tile images in application memory

The [`CanCacheTiles`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ImageryLayer~CanCacheTiles.html) property used to decide whether the tile images should be cached in application memory or not.

{% tabs %}

{% highlight c# %}

       ImageryLayer imageryLayer = new ImageryLayer();

       imageryLayer.CanCacheTiles = true;

{% endhighlight %}

{% endtabs %}

## Clear cached tile images from application memory

The [`DeleteTilesFromCache`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ImageryLayer~DeleteTilesFromCache.html) method used to clear the cached tile images from  application cache memory.

{% tabs %}

{% highlight xml %}

        <maps:SfMaps>
            <maps:SfMaps.Layers>            
                <maps:ImageryLayer x:Name="imageryLayer" />
            </maps:SfMaps.Layers>
        </maps:SfMaps>

{% endhighlight %}

{% highlight c# %}

       imageryLayer.DeleteTilesFromCache();

{% endhighlight %}

{% endtabs %}

## Events

The [`ZoomLevelChanging`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ZoomLevelChangingEventArgs.html) event triggers when zoom level changed. Following arguments can be get from the ZoomLevelChanging event .

* [`Cancel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ZoomLevelChangingEventArgs~Cancel.html) : Used to cancel the zooming.

* [`PreviousLevel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ZoomLevelChangingEventArgs~PreviousLevel.html) : Returns the previous level after the zooming.

* [`CurrentLevel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ZoomLevelChangingEventArgs~CurrentLevel.html) : Returns the current level to be zoomed.

{% tabs %}

{% highlight xml %}

        <maps:SfMaps>
            <maps:SfMaps.Layers>            
                <maps:ImageryLayer  ZoomLevelChanging="Layer_ZoomLevelChanging" />
            </maps:SfMaps.Layers>
        </maps:SfMaps>

{% endhighlight %}

{% highlight c# %}

        private void Layer_ZoomLevelChanging(object sender, ZoomLevelChangingEventArgs e)
        {
           if(e.PreviousLevel == 10) // Returns the previous zoom level
           {
               e.Cancel = true; // Cancels the zooming event
               var CurrentLevel = e.CurrentLevel; // Returns the current zoomed level
           }
        }

{% endhighlight %}

{% endtabs %}

The [`GeoCoordinateChanged`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.ImageryLayer~GeoCoordinateChanged_EV.html) event is triggered while zooming and panning the maps.

The following arguments can be gotten from the `ImageryLayer_GeoCoordinateChanged` event: 

* [`Center`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.GeoCoordinateChangedEventArgs~Center.html): Returns the center Geo coordinate point of the visual tiles while zooming and panning.
* [`TopLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.GeoCoordinateChangedEventArgs~TopLeft.html):  Returns the top-left Geo coordinate point of the visual tiles while zooming and panning.
* [`TopRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.GeoCoordinateChangedEventArgs~TopRight.html): Returns the top-right Geo coordinate point of the visual tiles while zooming and panning.
* [`BottomLeft`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.GeoCoordinateChangedEventArgs~BottomLeft.html): Returns the bottom-left Geo coordinate point of the visual tiles while zooming and panning.
* [`BottomRight`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfMaps.XForms~Syncfusion.SfMaps.XForms.GeoCoordinateChangedEventArgs~BottomRight.html): Returns the bottom-right Geo coordinate point of the visual tiles while zooming and panning.

{% tabs %}

{% highlight xml %}

<maps:SfMaps >
    <maps:SfMaps.Layers >
        <maps:ImageryLayer GeoCoordinateChanged="ImageryLayer_GeoCoordinateChanged"/>       
    </maps:SfMaps.Layers>
</maps:SfMaps>

{% endhighlight %}

{% highlight c# %}

private void ImageryLayer_GeoCoordinateChanged(object sender, GeoCoordinateChangedEventArgs e)
{
    var topLeft = e.TopLeft;
    var topRight = e.TopRight;
    var bottomLeft = e.BottomLeft;
    var bottomRight = e.BottomRight;
    var center = e.Center;
}

{% endhighlight %}

{% endtabs %}