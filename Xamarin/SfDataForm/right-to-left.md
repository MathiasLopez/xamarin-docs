---
layout: post
title: Right to left(RTL) | SfDataForm | Xamarin.Forms | Syncfusion
description: Describes how dataform works on right-to-left localization.
platform: xamarin
control: SfDataForm
documentation: UG
---

# Right to left(RTL)

The data form supports linear and grid layouts. The DataFormLayoutManager creates the [DataFormItemView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormItemView.html), [DataFormGroupItemView](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.SfDataForm.XForms~Syncfusion.XForms.DataForm.DataFormGroupItemView.html), and manages layout of label, editor, and validation label.

{% tabs %}
{% highlight xaml %}
<dataForm:SfDataForm FlowDirection="RightToLeft">
</dataForm:SfDataForm>
{% endhighlight %}
{% highlight c# %}
dataForm.FlowDirection = FlowDirection.RightToLeft;
{% endhighlight %}
{% endtabs %}

>**Note**
For implementing the `FlowDirection` in the control, Xamarin.Forms package version must be 3.0 and above. Please refer [RightToLeft](https://blog.xamarin.com/right-to-left-localization-xamarin-forms) to get more details about `RightToLeft` flow direction in Xamarin.Forms.

### Android
For Android, add `android:supportsRtl="true"` in your application tag of `AndroidManifest.xml` file, and make sure your `MinSDKVersion` is 17+. By changing the device language / enabling the device's `Force RTL layout` can achieve the `RightToLeft` layout direction in DataForm.

{% tabs %}
{% highlight xml %}
<manifest ... >
<uses-sdk android:minSdkVersion="17" ... />
<application ... android:supportsRtl="true">
</application>
</manifest>
{% endhighlight %}
{% endtabs %}

### iOS
For iOS, add the `RightToLeft` language in the `CFBundleLocalizations` section of your `Info.plist` file, and make sure you’re targeting iOS 9+.

{% tabs %}
{% highlight xml %}
<resources>
<key>CFBundleDevelopmentRegion</key>
<string>en</string>
<key>CFBundleLocalizations</key>
<array>
<string>en</string>
<string>ar</string>
</array>
</resources>
{% endhighlight %}
{% endtabs %}

![info plist](SfDataForm_images/DataForm_iosplist.png)

### UWP
For UWP, you need to set `FlowDirection` to `RightToLeft` in the `MainPage.cs` file of the `UWP` project.

{% tabs %}
{% highlight c# %}
public MainPage()
{
…
this.FlowDirection = FlowDirection.RightToLeft;
LoadApplication (new App ());
…
}
{% endhighlight %}
{% endtabs %}

![RTL in Xamarin.Forms DataForm](SfDataForm_images/DataForm_RTL.png)