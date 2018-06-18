---

layout: post
title: Labels in Syncfusion SfCircularGauge control for Xamarin.Forms
description:  Learn how to set labels in Syncfusion SfCircularGauge control
platform: xamarin
control: SfCircularGauge
documentation: ug

---

# Labels

The [`Scale`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale.html) labels associate a numeric value with major scale tick marks.

## Label color customization

The label color can be changed using the [`LabelColor`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~LabelColor.html) property.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>

         <gauge:SfCircularGauge.Scales>

             <gauge:Scale LabelColor= "Blue"/ >

         </gauge:SfCircularGauge.Scales>	
     
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.LabelColor = Color.Blue;
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/label-color-customization.png)

## Label font customization

The label font can be customized by using the [`LabelFontSize`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~LabelFontSize.html), [`FontAttribute`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~FontAttributes.html), and [`FontFamily`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~FontFamily.html) properties. 

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>

         <gauge:SfCircularGauge.Scales>

             <gauge:Scale FontAttributes = "Bold" LabelFontSize = "20" >
                    <gauge:Scale.FontFamily>
                        <OnPlatform x:TypeArguments = "x:String" iOS = "Chalkduster" Android = "algerian.ttf" WinPhone="Chiller" />
                    </gauge:Scale.FontFamily>
             </gauge:Scale>

         </gauge:SfCircularGauge.Scales>	
     
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.FontAttributes = FontAttributes.Bold;
    scale.FontFamily = Device.RuntimePlatform == Device.iOS ? "Chalkduster" :     Device.RuntimePlatform == Device.Android ? "algerian.ttf" : "Chiller";
    scale.LabelFontSize = 20;
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/label-font-customization.png)

## Setting position for labels

The labels can be positioned far away from the ticks by using the [`LabelOffset`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~LabelOffset.html) property.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>
         <gauge:SfCircularGauge.Scales>

            <gauge:Scale LabelOffset = "0.4"/>

         </gauge:SfCircularGauge.Scales>	
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.LabelOffset = 0.4;
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/label-offset.png)

## Setting number of decimal digits for labels

The [`NumberOfDecimalDigits`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~NumberOfDecimalDigits.html) property is used to set the number of decimal digits to be displayed in the scale labels.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>
         <gauge:SfCircularGauge.Scales>

            <gauge:Scale NumberOfDecimalDigits = "3"/>

         </gauge:SfCircularGauge.Scales>	
     
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.NumberOfDecimalDigits = 3; 
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/number-of-decimal-digits.png)

## Setting postfix and prefix for labels

You can postfix/prefix values to the scale labels by using the [`LabelPostfix`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~LabelPostfix.html) and [`LabelPrefix`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~LabelPrefix.html) properties, respectively.

### Label postfix

`LabelPostfix` property allows you to postfix the values to the scale labels.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>
         <gauge:SfCircularGauge.Scales>

            <gauge:Scale LabelPostfix = "$" />

         </gauge:SfCircularGauge.Scales>	
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.LabelPostfix = "$"; 
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/label-postfix.png)

### Label prefix

`LabelPrefix` property allows you to prefix the values to the scale labels.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>
         <gauge:SfCircularGauge.Scales>

            <gauge:Scale LabelPrefix = "$" />

         </gauge:SfCircularGauge.Scales>	
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.LabelPrefix = "$"; 
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/label-prefix.png)

## Edge label customization

You can customize the edge label by using the [`ShowFirstLabel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~ShowFirstLabel.html) and [`ShowLastLabel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~ShowLastLabel.html) properties, which are Boolean properties. The [`ShowFirstLabel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~ShowFirstLabel.html) property is used to enable or disable first label, and the [`ShowLastLabel`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~ShowLastLabel.html) property is used to enable or disable the last label in circular gauge.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>
         <gauge:SfCircularGauge.Scales>

           <gauge:Scale ShowFirstLabel = "False" StartValue = "0" EndValue = "12" Interval ="1" MinorTicksPerInterval = "5" StartAngle = "270" SweepAngle = "360" />
		   
         </gauge:SfCircularGauge.Scales>	
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.StartValue = 0;	
    scale.Interval = 1;			
    scale.MinorTicksPerInterval = 5;			
    scale.EndValue = 12;			
    scale.StartAngle = 270;			
    scale.SweepAngle = 360;			
    scale.ShowFirstLabel = false;
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/label-edge-customization.png)

## Show labels

The [`ShowLabels`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~ShowLabels.html) property is a Boolean property, which is used to enable or disable the labels in circular gauge.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>
         <gauge:SfCircularGauge.Scales>

          <gauge:Scale ShowLabels = "False"/>
		   
         </gauge:SfCircularGauge.Scales>	
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.ShowLabels = false;
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/show-labels.png)

## Setting auto angle for label

Scale labels can be rotated automatically based on the current angle. To enable or disable the auto angle, use the [`EnableAutoAngle`](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfGauge.XForms~Syncfusion.SfGauge.XForms.Scale~EnableAutoAngle.html) property.

{% tabs %}

{% highlight xaml %}

     <gauge:SfCircularGauge>

         <gauge:SfCircularGauge.Scales>

          <gauge:Scale EnableAutoAngle = "True"/>
		   
         </gauge:SfCircularGauge.Scales>	
     </gauge:SfCircularGauge>
              

{% endhighlight %}

{% highlight c# %}

    SfCircularGauge circularGauge = new SfCircularGauge();
    ObservableCollection<Scale> scales = new ObservableCollection<Scale>();
    Scale scale = new Scale();
    scale.EnableAutoAngle = true;
    scales.Add(scale);
    circularGauge.Scales = scales;  
    
{% endhighlight %}

{% endtabs %}

![](labels_images/auto-angle.png)


