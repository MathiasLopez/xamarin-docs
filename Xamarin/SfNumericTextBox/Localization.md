---
layout: post
title: Localization in Syncfusion NumericTextBox control for Xamarin.Forms
description: Learn how to localize the  NumericTextBox
platform: Xamarin
control: NumericTextBox
documentation: ug
---
# Localization

The SfNumericTextBox value can be localized to any specific culture. It can be specified by setting the `Culture` property with `System.Globalization.CultureInfo` object instance.

{% tabs %}

{% highlight c# %}
 
SfNumericTextBox numericTextBox=new SfNumericTextBox();
numericTextBox.Value=123.45;
numericTextBox.Culture = new System.Globalization.CultureInfo("fr-FR");
this.Content = numericTextBox;

{% endhighlight %}

{% endtabs %}

![](images/Culture.png)

## Change Localization of Return key text

The SfNumericTextBox provides the Localization support for the Return Key in soft keypad of iOS. We have provided the knowledge base document for the same. Please refer this link for more details.


