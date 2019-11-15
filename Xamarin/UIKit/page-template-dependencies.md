---
layout: post
title:  XAML Templates | Page Template Dependencies of UI Kit | Syncfusion
description: The list of screen-wise resources and NuGet packages required for each Xamarin Essential UI kit page.
platform: xamarin
control: UI kit
documentation: ug
---

# Page Template Dependencies for Syncfusion Xamarin.Forms Essential UI Kit  

## Forms

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
		   1<br/>
		</td>
		<td>
		  Login Page with Gradient<br/>
		</td>
		<td>
		 Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/> 
		</td>
		<td>
		  <b>PCL:</b><br/>  Views\Forms\LoginPage.xaml<br/>  Views\Forms\LoginPage.xaml.cs<br/>  Views\Forms\EmailEntry.xaml<br/>  Views\Forms\EmailEntry.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs <br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs <br/>  ViewModels\Forms\LoginViewModel.cs<br/>  ViewModels\Forms\LoginPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\LoginBackground.png<br/>  Resources\drawable-hdpi\LoginBackground.png<br/>  Resources\drawable-xhdpi\LoginBackground.png<br/>  Resources\drawable-xxhdpi\LoginBackground.png<br/>  Resources\drawable-xxxhdpi\LoginBackground.png<br/>  Resources\drawable-land\LoginBackground.png<br/>  Resources\drawable-land-hdpi\LoginBackground.png<br/>  Resources\drawable-land-xhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxxhdpi\LoginBackground.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\LoginBackground.png<br/>  Resources\LoginBackground@2x.png<br/>  Resources\LoginBackground@2x~ipad.png<br/>  Resources\LoginBackground@3x.png<br/>  Resources\LoginBackground@3x~ipad.png<br/>  Resources\LoginBackground@4x.png<br/>  Resources\LoginBackground~ipad.png<br/>  Resources\LoginBackground-Landscape.png<br/>  Resources\LoginBackground-Landscape@2x.png<br/>  Resources\LoginBackground-Landscape@2x~ipad.png<br/>  Resources\LoginBackground-Landscape@3x.png<br/>  Resources\LoginBackground-Landscape@3x~ipad.png<br/>  Resources\LoginBackground-Landscape@4x.png<br/>  Resources\LoginBackground-Landscape~ipad.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\LoginBackground.scale-100.png<br/>  scale-100\LoginBackground.scale-200.png<br/>  scale-100\LoginBackground.scale-400.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>   
        </td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		    Sign Up Page with Gradient<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\SignupPage.xaml<br/>  Views\Forms\SignupPage.xaml.cs<br/>  Views\Forms\EmailEntry.xaml<br/>  Views\Forms\EmailEntry.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs <br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  ViewModels\Forms\SignupPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\LoginBackground.png<br/>  Resources\drawable-hdpi\LoginBackground.png<br/>  Resources\drawable-xhdpi\LoginBackground.png<br/>  Resources\drawable-xxhdpi\LoginBackground.png<br/>  Resources\drawable-xxxhdpi\LoginBackground.png<br/>  Resources\drawable-land\LoginBackground.png<br/>  Resources\drawable-land-hdpi\LoginBackground.png<br/>  Resources\drawable-land-xhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxxhdpi\LoginBackground.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\LoginBackground.png<br/>  Resources\LoginBackground@2x.png<br/>  Resources\LoginBackground@2x~ipad.png<br/>  Resources\LoginBackground@3x.png<br/>  Resources\LoginBackground@3x~ipad.png<br/>  Resources\LoginBackground@4x.png<br/>  Resources\LoginBackground~ipad.png<br/>  Resources\LoginBackground-Landscape.png<br/>  Resources\LoginBackground-Landscape@2x.png<br/>  Resources\LoginBackground-Landscape@2x~ipad.png<br/>  Resources\LoginBackground-Landscape@3x.png<br/>  Resources\LoginBackground-Landscape@3x~ipad.png<br/>  Resources\LoginBackground-Landscape@4x.png<br/>  Resources\LoginBackground-Landscape~ipad.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\LoginBackground.scale-100.png<br/>  scale-100\LoginBackground.scale-200.png<br/>  scale-100\LoginBackground.scale-400.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Forgot Password Page with Gradient<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs<br/>  Views\Forms\ForgotPasswordPage.xaml <br/>  Views\Forms\ForgotPasswordPage.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Views\Forms\EmailEntry.xaml<br/>  Views\Forms\EmailEntry.xaml.cs<br/>  ViewModels\Forms\ForgotPasswordViewModel.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\LoginBackground.png<br/>  Resources\drawable-hdpi\LoginBackground.png<br/>  Resources\drawable-xhdpi\LoginBackground.png<br/>  Resources\drawable-xxhdpi\LoginBackground.png<br/>  Resources\drawable-xxxhdpi\LoginBackground.png<br/>  Resources\drawable-land\LoginBackground.png<br/>  Resources\drawable-land-hdpi\LoginBackground.png<br/>  Resources\drawable-land-xhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxxhdpi\LoginBackground.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\LoginBackground.png<br/>  Resources\LoginBackground@2x.png<br/>  Resources\LoginBackground@2x~ipad.png<br/>  Resources\LoginBackground@3x.png<br/>  Resources\LoginBackground@3x~ipad.png<br/>  Resources\LoginBackground@4x.png<br/>  Resources\LoginBackground~ipad.png<br/>  Resources\LoginBackground-Landscape.png<br/>  Resources\LoginBackground-Landscape@2x.png<br/>  Resources\LoginBackground-Landscape@2x~ipad.png<br/>  Resources\LoginBackground-Landscape@3x.png<br/>  Resources\LoginBackground-Landscape@3x~ipad.png<br/>  Resources\LoginBackground-Landscape@4x.png<br/>  Resources\LoginBackground-Landscape~ipad.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\LoginBackground.scale-100.png<br/>  scale-100\LoginBackground.scale-200.png<br/>  scale-100\LoginBackground.scale-400.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			4<br/>
		</td>
		<td>
		Reset Password Page with Gradient<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.c<br/>  Views\Forms\ResetPasswordPage.xaml <br/>  Views\Forms\ResetPasswordPage.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Views\Forms\EmailEntry.xaml<br/>  Views\Forms\EmailEntry.xaml.cs<br/>  ViewModels\Forms\ResetPasswordViewModel.cs<br/>  ViewModels\Forms\LoginViewModel.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\LoginBackground.png<br/>  Resources\drawable-hdpi\LoginBackground.png<br/>  Resources\drawable-xhdpi\LoginBackground.png<br/>  Resources\drawable-xxhdpi\LoginBackground.png<br/>  Resources\drawable-xxxhdpi\LoginBackground.png<br/>  Resources\drawable-land\LoginBackground.png<br/>  Resources\drawable-land-hdpi\LoginBackground.png<br/>  Resources\drawable-land-xhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxhdpi\LoginBackground.png<br/>  Resources\drawable-land-xxxhdpi\LoginBackground.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\LoginBackground.png<br/>  Resources\LoginBackground@2x.png<br/>  Resources\LoginBackground@2x~ipad.png<br/>  Resources\LoginBackground@3x.png<br/>  Resources\LoginBackground@3x~ipad.png<br/>  Resources\LoginBackground@4x.png<br/>  Resources\LoginBackground~ipad.png<br/>  Resources\LoginBackground-Landscape.png<br/>  Resources\LoginBackground-Landscape@2x.png<br/>  Resources\LoginBackground-Landscape@2x~ipad.png<br/>  Resources\LoginBackground-Landscape@3x.png<br/>  Resources\LoginBackground-Landscape@3x~ipad.png<br/>  Resources\LoginBackground-Landscape@4x.png<br/>  Resources\LoginBackground-Landscape~ipad.png<br/>   <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\LoginBackground.scale-100.png<br/>  scale-100\LoginBackground.scale-200.png<br/>  scale-100\LoginBackground.scale-400.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			5<br/>
		</td>
		<td>
		Simple Login Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		 <b>PCL:</b><br/>  Views\Forms\SimpleLoginPage.xaml<br/>  Views\Forms\SimpleLoginPage.xaml.cs<br/>  Views\Forms\SimpleEmailEntry.xaml<br/>  Views\Forms\SimpleEmailEntry.xaml.cs <br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  ViewModels\Forms\LoginPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			6<br/>
		</td>
		<td>
		Simple Sign Up Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\SimpleSignUpPage.xaml<br/>  Views\Forms\SimpleSignUpPage.xaml.cs<br/>  Views\Forms\SimpleEmailEntry.xaml<br/>  Views\Forms\SimpleEmailEntry.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  ViewModels\Forms\SignupPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			7<br/>
		</td>
		<td>
		Simple Forgot Password Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\SimpleForgotPasswordPage.xaml<br/>  Views\Forms\SimpleForgotPasswordPage.xaml.cs<br/>  Views\Forms\SimpleEmailEntry.xaml<br/>  Views\Forms\SimpleEmailEntry.xaml.cs <br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs<br/>  ViewModels\Forms\ForgotPasswordViewModel.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			8<br/>
		</td>
		<td>
		Simple Reset Password Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\SimpleResetPasswordPage.xaml<br/>  Views\Forms\SimpleResetPasswordPage.xaml.cs <br/>  Views\Forms\SimpleEmailEntry.xaml<br/>  Views\Forms\SimpleEmailEntry.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs <br/>  Converters\StringToBooleanConverter.cs<br/>  Converters\ErrorValidationColorConverter.cs <br/>  ViewModels\Forms\ResetPasswordViewModel.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs <br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>
		</td>
	</tr><tr valign="top">		
		<td align="center">
			9<br/>
		</td>
		<td>
		Add Contact Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfCalendar<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\AddContactPage.xaml<br/>  Views\Forms\AddContactPage.xaml.cs <br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Controls\CalenderDatePicker.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\CalenderDatePickerRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\CalenderDatePickerRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\CalenderDatePickerRenderer.cs<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			10<br/>
		</td>
		<td>
		Add Card Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfCalendar<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\AddCardPage.xaml<br/>  Views\Forms\AddCardPage.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Controls\CalenderDatePicker.cs<br/>  Converters\BooleanToColorConverter.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Behaviors\PaymentCardNumberEntryBehavior.cs <br/>  Behaviors\BorderlessEntryCVVBehavior.cs<br/>  ViewModels\Forms\AddCardViewModel.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\CalenderDatePickerRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\CalenderDatePickerRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\Card.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\CalenderDatePickerRenderer.cs<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			11<br/>
		</td>
		<td>
		Tabbed login Page <br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfTabView,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\TabbedForm.xaml<br/>  Views\Forms\TabbedForm.xaml.cs<br/>  Views\Forms\SimpleEmailEntry.xaml<br/>  Views\Forms\SimpleEmailEntry.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Converters\BooleanToColorConverter.cs <br/>  Converters\ErrorValidationColorConverter.cs <br/>  Converters\StringToBooleanConverter.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\Forms\LoginPageViewModel.cs<br/>  ViewModels\Forms\SignUpPageViewModel.cs<br/>  ViewModels\Forms\LoginViewModel.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\FrameShadowRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/>
		</td>
	</tr><tr valign="top">		
		<td align="center">
			12<br/>
		</td>
		<td>
		Add Profile page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfBadgeView,<br/>  Syncfusion.Xamarin.SfComboBox<br/> 
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Forms\AddProfilePage.xaml<br/>  Views\Forms\AddProfilePage.xaml.cs<br/>  Views\Forms\Styles.xaml<br/>  Views\Forms\Styles.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\Card.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  Renderers\BorderlessEntryRenderer.cs<br/> 
		</td>
	</tr>
</table>

## Catalog

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Category Tile Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Catalog\CategoryTilePage.xaml<br/>  Views\Catalog\CategoryTilePage.xaml.cs<br/>  Views\Catalog\Styles.xaml<br/>  Views\Catalog\Styles.xaml.cs<br/>  ViewModels\Catalog\CategoryPageViewModel.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Models\Category.cs<br/>  Controls\TitleView.cs<br/>  Behaviors\SfListViewTapBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  DataService\CategoryDataService.cs<br/>  Data\ecommerce.json<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Catalog Tile page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView, <br/>  Syncfusion.Xamarin.Buttons, <br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.SfBadgeView,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Catalog\CatalogTilePage.xaml<br/>  Views\Catalog\CatalogTilePage.xaml.cs<br/>  Views\Catalog\Styles.xaml<br/>  Views\Catalog\Styles.xaml.cs<br/>  ViewModels\Catalog\CatalogPageViewModel.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Converters\IntToThicknessConverter.cs<br/>  Models\Product.cs<br/>  Models\Review.cs<br/>  Models\Category.cs<br/>  Controls\TitleView.cs<br/>  Helpers\RTLHelper.cs<br/>  Behaviors\Catalog\CartBehavior.cs<br/>  Behaviors\SfListViewTapBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  DataService\CatalogDataService.cs<br/>  Data\ecommerce.json<br/>  Views\Templates\ProductTileTemplate.xaml <br/>  Views\Templates\ProductTileTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Catalog List Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.SfBadgeView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Expander,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Catalog\CatalogListPage.xaml<br/>  Views\Catalog\CatalogListPage.xaml.cs<br/>  Views\Catalog\Styles.xaml<br/>  Views\Catalog\Styles.xaml.cs<br/>  ViewModels\Catalog\CatalogPageViewModel.cs<br/>  Models\Product.cs<br/>  Models\Review.cs<br/>  Models\Category.cs<br/>  Data\ecommerce.json<br/>  DataService\CatalogDataService.cs<br/>  Converters\DynamicResourceToColorConverter.cs <br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Converters\IntToThicknessConverter.cs<br/>  Controls\TitleView.cs<br/>  Helpers\RTLHelper.cs<br/>  Behaviors\Catalog\CartBehavior.cs<br/>  Behaviors\SfListViewTapBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Views\Templates\ProductListTemplate.xaml<br/>  Views\Templates\ProductListTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			4<br/>
		</td>
		<td>
		Article List Page <br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Cards,<br/>  Syncfusion.Xamarin.SfRotator,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating<br/> 
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Catalog\ArticleListPage.xaml<br/>  Views\Catalog\ArticleListPage.xaml.cs<br/>  Views\Catalog\Styles.xaml<br/>  Views\Catalog\Styles.xaml.cs<br/>  ViewModels\Catalog\ArticleListViewModel.cs<br/>  Models\Article.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  Converters\BooleanToStringConverter.cs <br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Helpers\RTLHelper.cs<br/>  Views\Templates\ArticleListTemplate.xaml<br/>  Views\Templates\ArticleListTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs <br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>  
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			5<br/>
		</td>
		<td>
		Article Tile Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfRotator,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Catalog\ArticleTilePage.xaml<br/>  Views\Catalog\ArticleTilePage.xaml.cs <br/>  Views\Catalog\Styles.xaml<br/>  Views\Catalog\Styles.xaml.cs<br/>  ViewModels\Catalog\ArticleListViewModel.cs<br/>  Models\Article.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Views\Templates\ArticleTileTemplate.xaml<br/>  Views\Templates\ArticleTileTemplate.xaml.cs <br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			6<br/>
		</td>
		<td>
		Product Home page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  EssentialUIKit\Views\Catalog\ProductHomePage.xaml<br/>  EssentialUIKit\Views\Catalog\ProductHomePage.xaml.cs<br/>  EssentialUIKit\Views\Catalog\Styles.xaml<br/>  EssentialUIKit\Views\Catalog\Styles.xaml.cs<br/>  EssentialUIKit\ViewModels\Catalog\ProductHomePageViewModel.cs<br/>  EssentialUIKit\Converters\DynamicResourceToColorConverter.cs <br/>  EssentialUIKit\Models\Product.cs<br/>  EssentialUIKit\Models\Review.cs<br/>  EssentialUIKit\Controls\TitleView.cs<br/>  EssentialUIKit\Controls\CustomShadowFrame.cs<br/>  EssentialUIKit\Behaviors\SfListViewExtendHeightBehavior.cs<br/>  EssentialUIKit\Themes\LightTheme.xaml<br/>  EssentialUIKit\Themes\LightTheme.xaml.cs<br/>  EssentialUIKit\DataService\ProductHomeDataService.cs<br/>  EssentialUIKit\Data\ecommerce.json<br/>  EssentialUIKit\ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Renderers\FrameShadowRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Detail

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Product Detail page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfRotator,<br/>  Syncfusion.Xamarin.SfBadgeView,<br/>  Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Detail\DetailPage.xaml<br/>  Views\Detail\DetailPage.xaml.cs<br/>  Views\Detail\Styles.xaml<br/>  Views\Detail\Styles.xaml.cs<br/>  Views\Detail\FeedbackView.xaml<br/>  Views\Detail\FeedbackView.xaml.cs<br/>  Views\Templates\ReviewTemplate.xaml<br/>  Views\Templates\ReviewTemplate.xaml.cs<br/>  ViewModels\Detail\DetailPageViewModel.cs T<br/>  Converters\DynamicResourceToColorConverter.csI<br/>  Converters\BooleanToColorConverter.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Converters\IntToThicknessConverter.cs<br/>  Converters\VisibilityConverter.cs<br/>  Models\Product.cs<br/>  Models\Review.cs<br/>  Models\Category.cs<br/>  Controls\TitleView.cs<br/>  Helpers\RTLHelper.cs<br/>  Behaviors\SegmentedControlCommandBehavior.cs<br/>  Behaviors\Detail\CartBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Feedback Detail Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfRating<br/> 
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Detail\FeedbackDetailPage.xaml<br/>  Views\Detail\FeedbackDetailPage.xaml.cs<br/>  Views\Detail\Templates\MobileView.xaml <br/>  Views\Detail\Templates\MobileView.xaml.cs<br/>  Views\Detail\Templates\TabletView.xaml <br/>  Views\Detail\Templates\TabletView.xaml.cs<br/>  Controls\TitleView.cs<br/>  Views\Detail\Styles.xaml<br/>  Views\Detail\Styles.xaml.cs<br/>  ViewModels\Detail\DetailViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Article Detail<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.SfComboBox<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Detail\ArticleDetailPage.xaml<br/>  Views\Detail\ArticleDetailPage.xaml.cs<br/>  Views\Detail\Styles.xaml<br/>  Views\Detail\Styles.xaml.cs<br/>  ViewModels\Detail\ArticleDetailPageViewModel.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Models\Article.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Controls\TitleView.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Views\Templates\ArticleListTemplate.xaml<br/>  Views\Templates\ArticleListTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
</table>

## Chat

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Recent Chat Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfBadgeView<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Chat\RecentChatPage.xaml<br/>  Views\Chat\RecentChatPage.xaml.cs<br/>  Views\Chat\Styles.xaml<br/>  Views\Chat\Styles.xaml.cs<br/>  ViewModels\Chat\RecentChatViewModel.cs<br/>  Models\Chat\ChatDetail.cs<br/>  Controls\BorderlessEntry.cs<br/>  Controls\BorderlessEditor.cs<br/>  Controls\SearchableListView.cs<br/>  Converters\StringToBadgeIconConverter.cs<br/>  Converters\StringToGlyphConverter.cs <br/>  Converters\StringToMessageTypeConverter.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b> <br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Chat Conversation Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Chat\ChatMessagePage.xaml<br/>  Views\Chat\ChatMessagePage.xaml.cs<br/>  Views\Chat\Styles.xaml<br/>  Views\Chat\Styles.xaml.cs<br/>  Views\Chat\Selectors\MessageDataTemplateSelector.cs<br/>  Views\Chat\Templates\IncomingImageTemplate.xaml <br/>  Views\Chat\Templates\IncomingImageTemplate.xaml.cs<br/>  Views\Chat\Templates\OutgoingImageTemplate.xaml <br/>  Views\Chat\Templates\OutgoingImageTemplate.xaml.cs<br/>  Views\Chat\Templates\IncomingTextTemplate.xaml<br/>  Views\Chat\Templates\IncomingTextTemplate.xaml.cs<br/>  Views\Chat\Templates\OutgoingTextTemplate.xaml<br/>  Views\Chat\Templates\OutgoingTextTemplate.xaml.cs<br/>  ViewModels\Chat\ChatMessageViewModel.cs<br/>  Models\Chat\ChatMessage.cs<br/>  Helpers\RTLHelper.cs<br/>  Controls\BorderlessEditor.cs<br/>  Controls\BorderlessEntry.cs<br/>  Converters\DateTimeToStringConverter.cs<br/>  Behaviors\Chat\ChatMessageListViewBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b> <br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Renderers\BorderlessEntryRenderer.cs<br/>   <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b> <br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Article

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Article with Comments page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Article\ArticleWithCommentsPage.xaml<br/>  Views\Article\ArticleWithCommentsPage.xaml.cs<br/>  Views\Article\Styles.xaml<br/>  Views\Article\Styles.xaml.cs<br/>  Models\Article.cs<br/>  Models\Review.cs<br/>  ViewModels\Article\ArticleWithCommentsPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Views\Templates\Reviewtemplate.xaml<br/>  Views\Templates\Reviewtemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr><tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Article parallax Header Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Article\ArticleParallaxHeaderPage.xaml<br/>  Views\Article\ArticleParallaxHeaderPage.xaml.cs<br/>  Views\Article\Styles.xaml<br/>  Views\Article\Styles.xaml.cs<br/>  Models\Article.cs<br/>  Models\Review.cs<br/>  ViewModels\Article\ArticleParallaxHeaderPageViewModel.cs<br/>  ViewModels\BaseViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  Controls\ParallaxScrollView.cs<br/>  Behaviors\SfListviewExtendHeightBehavior.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Converters\DynamicResourceToColorConverter.cs <br/>  Views\Templates\ArticleTileTemplate.xaml<br/>  Views\Templates\ArticleTileTemplate.xaml.cs<br/>  Views\Templates\Reviewtemplate.xaml<br/>  Views\Templates\Reviewtemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		My Article Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Article\MyArticlePage.xaml<br/>  Views\Article\MyArticlePage.xaml.cs<br/>  Views\Article\Styles.xaml<br/>  Views\Article\Styles.xaml.cs<br/>  Models\Article.cs<br/>  ViewModels\Article\MyArticlePageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  Behaviors\SfListViewTapBehavior.cs<br/>  Converters\DynamicResourceToColorConverter.cs" <br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Reviews and Ratings

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Feedback Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.SfListView<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Feedback\FeedbackPage.xaml<br/>  Views\Feedback\FeedbackPage.xaml.cs<br/>  Views\Feedback\Styles.xaml<br/>  Views\Feedback\Styles.xaml.cs<br/>  ViewModels\Feedback\FeedbackViewModel.cs<br/>  Models\Feedback\Review.cs<br/>  Behaviors\SfListViewExtendHeightBehavior.cs<br/>  Views\Templates\ReviewTemplate.xaml<br/>  Views\Templates\ReviewTemplate.xaml.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr><tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Review Page<br/>
		</td>
		<td>
		 Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfRating<br/> 
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Feedback\ReviewPage.xaml<br/>  Views\Feedback\ReviewPage.xaml.cs<br/>  Views\Feedback\Styles.xaml<br/>  Views\Feedback\Styles.xaml.cs<br/>  ViewModels\Feedback\ReviewPageViewModel.cs <br/>  Controls\BorderlessEditor.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
</table>

## Contact Us

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Contact us Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfMaps<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ContactUs\ContactUsPage.xaml<br/>  Views\ContactUs\ContactUsPage.xaml.cs<br/>  Views\ContactUs\Styles.xaml<br/>  Views\ContactUs\Styles.xaml.cs<br/>  ViewModels\ContactUs\ContactUsViewModel.cs<br/>  Models\ContactUs\LocationMarker.cs<br/>  Controls\BorderlessEntry.cs<br/>  Controls\BorderlessEditor.cs<br/>  Controls\TitleView.cs<br/>  Converters\StringToBooleanConverter.cs <br/>  Converters\BooleanToColorConverter.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Renderers\BorderlessEditorRenderer.cs<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
</table>

## About Us

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Simple About Us Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\AboutUs\AboutUsSimplePage.xaml<br/>  Views\AboutUs\AboutUsSimplePage.xaml.cs<br/>  Views\AboutUs\Styles.xaml<br/>  Views\AboutUs\Styles.xaml.cs<br/>  ViewModels\About\AboutUsViewModel.cs<br/>  Models\About\AboutUsModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr><tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		About Us Page with cards<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfListView<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\AboutUs\AboutUsWithCardsPage.xaml <br/>  Views\AboutUs\AboutUsWithCardsPage.xaml.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Behaviors\SfListViewExtendHeightBehavior.cs<br/>  Views\AboutUs\Styles.xaml<br/>  Views\AboutUs\Styles.xaml.cs<br/>  ViewModels\About\AboutUsViewModel.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Models\About\AboutUsModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		About Page with parallax Scrolling<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfListView<br/>  Syncfusion.Xamarin.SfParallaxView<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\AboutUs\AboutUswithScrollPage.xaml <br/>  Views\AboutUs\AboutUswithScrollPage.xaml.cs<br/>  Views\AboutUs\Styles.xaml<br/>  Views\AboutUs\Styles.xaml.cs<br/>  ViewModels\About\AboutUsViewModel.cs<br/>  Models\About\AboutUsModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Behaviors\SfListViewExtendHeightBehavior.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\About.png<br/>  Resources\drawable\OurTeam.png<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources \About.png<br/>  Resources \OurTeam.png<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\ About.png<br/>  scale-100\ OurTeam.png<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Navigation

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Bottom Navigation Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.DataSource<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Navigation\BottomNavigationPage.xaml<br/>  Views\Navigation\BottomNavigationPage.xaml.cs<br/>  Views\Navigation\PhotosPage.xaml<br/>  Views\Navigation\PhotosPage.xaml.cs<br/>  Views\Navigation\SettingsPage.xaml<br/>  Views\Navigation\SettingsPage.xaml.cs <br/>  Views\Navigation\AlbumPage.xaml<br/>  Views\Navigation\AlbumPage.xaml.cs<br/>  Views\Navigation\Styles.xaml<br/>  Views\Navigation\Styles.xaml.cs<br/>  ViewModels\Navigation\AlbumViewModel.cs<br/>  ViewModels\Navigation\NavigationViewModel.cs<br/>  ViewModels\Navigation\PhotosViewModel.cs<br/>  ViewModels\Navigation\SettingsViewModel.cs<br/>  Models\Navigation\Album.cs<br/>  Models\Navigation\NavigationModel.cs<br/>  Models\Navigation\Photo.cs<br/>  Data\navigation.json<br/>  DataService\NavigationDataService.cs<br/>  DataService\AlbumDataService.cs<br/>  DataService\PhotosDataService.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr><tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Navigation List Card Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.SfListView<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Navigation\NavigationListCardPage.xaml <br/>  Views\Navigation\NavigationListCardPage.xaml.cs <br/>  Views\Navigation\Styles.xaml Views\Navigation\Styles.xaml.<br/>  Controls\CustomShadowFrame.cs<br/>  Controls\TitleView.cs<br/>  ViewModels\Navigation\NavigationViewModel.cs<br/>  Models\Navigation\NavigationModel.cs<br/>  Themes\LightTheme.xaml <br/>  Themes\LightTheme.xaml.<br/>  Data\navigation.json <br/>  DataService\NavigationDataService.cs<br/>  Views\Templates\NavigationListTemplate.xaml<br/>  Views\Templates\NavigationListTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Navigation Tile Card Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.SfListView<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Navigation\NavigationTileCardPage.xaml<br/>  Views\Navigation\NavigationTileCardPage.xaml.cs<br/>  Views\Navigation\Styles.xaml<br/>  Views\Navigation\Styles.xaml.cs<br/>  ViewModels\Navigation\NavigationViewModel.cs<br/>  Models\Navigation\NavigationModel.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Controls\TitleView.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Data\navigation.json<br/>  DataService\NavigationDataService.cs<br/>  Views\Templates\NavigationTileTemplate.xaml <br/>  Views\Templates\NavigationTileTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Onboarding

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Walkthrough Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfRotator,<br/>  Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\OnBoarding\OnBoardingAnimationPage.xaml <br/>  Views\OnBoarding\OnBoardingAnimationPage.xaml.cs<br/>  Views\OnBoarding\WalkthroughItemPage.xaml<br/>  Views\OnBoarding\WalkthroughItemPage.xaml.cs<br/>  Views\OnBoarding\Styles.xaml<br/>  Views\OnBoarding\Styles.xaml.cs<br/>  ViewModels\OnBoarding\OnBoardingAnimationViewModel.cs<br/>  Models\OnBoarding\Boarding.cs<br/>  Controls\SVGImage.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\ChooseGradient.svg<br/>  Images\ConfirmGradient.svg<br/>  Images\DeliverGradient.svg<br/>  Behaviors\OnBoarding\SfRotatorBehavior.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Error and Empty

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Empty Cart Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\EmptyCartPage.xaml<br/>  Views\ErrorAndEmpty\EmptyCartPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\EmptyCartPageViewModel.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\EmptyCart.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Location Denied Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\LocationDeniedPage.xaml<br/>  Views\ErrorAndEmpty\LocationDeniedPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\LocationDeniedPageViewModel.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\LocationAccessDenied.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		No Credits Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NoCreditsPage.xaml<br/>  Views\ErrorAndEmpty\NoCreditsPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NoCreditsPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NoCredits.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr><tr valign="top">		
		<td align="center">
			4<br/>
		</td>
		<td>
		No Internet Connection Page<br/> 
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NoInternetConnectionPage.xaml<br/>  Views\ErrorAndEmpty\NoInternetConnectionPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NoInternetConnectionPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NoInternet.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			5<br/>
		</td>
		<td>
		No Item Page<br/> 
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NoItemPage.xaml<br/>  Views\ErrorAndEmpty\NoItemPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NoItemPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NoItem.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			6<br/>
		</td>
		<td>
		No Photos Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NoPhotosPage.xaml<br/>  Views\ErrorAndEmpty\NoPhotosPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NoPhotosPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NoPhotos.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr><tr valign="top">		
		<td align="center">
			7<br/>
		</td>
		<td>
		No Tasks Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NoTasksPage.xaml<br/>  Views\ErrorAndEmpty\NoTasksPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NoTasksPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NoTasks.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			8<br/>
		</td>
		<td>
		Not Enough Credit Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NotEnoughCreditPage.xaml<br/>  Views\ErrorAndEmpty\NotEnoughCreditPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NotEnoughCreditPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NotEnoughCredit.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			9<br/>
		</td>
		<td>
		No Videos Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\NoVideosPage.xaml<br/>  Views\ErrorAndEmpty\NoVideosPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\NoVideosPageViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\NoVideos.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr><tr valign="top">		
		<td align="center">
			10<br/>
		</td>
		<td>
		Payment Failed Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\PaymentFailedPage.xaml<br/>  Views\ErrorAndEmpty\PaymentFailedPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\PaymentFailedPageViewModel.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\PaymentFailed.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			11<br/>
		</td>
		<td>
		Something Went Wrong Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms,<br/>  SkiaSharp.Extended<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\ErrorAndEmpty\SomethingWentWrongPage.xaml<br/>  Views\ErrorAndEmpty\SomethingWentWrongPage.xaml.cs<br/>  Views\ErrorAndEmpty\Styles.xaml<br/>  Views\ErrorAndEmpty\Styles.xaml.cs<br/>  ViewModels\ErrorAndEmpty\SomethingWentWrongPageViewModel.cs <br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\SomethingWentWrong.svg<br/>  Controls\SVGImage.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Transaction

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Checkout Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Transaction\CheckoutPage.xaml<br/>  Views\Transaction\CheckoutPage.xaml.cs<br/>  Views\Transaction\DeliveryView.xaml<br/>  Views\Transaction\DeliveryView.xaml.cs<br/>  Views\Transaction\PaymentView.xaml<br/>  Views\Transaction\PaymentView.xaml.cs<br/>  Views\Transaction\PriceDetailView.xaml<br/>  Views\Transaction\PriceDetailView.xaml.cs <br/>  Views\Transaction\Styles.xaml<br/>  Views\Transaction\Styles.xaml.cs <br/>  ViewModels\Transaction\CheckoutPageViewModel.cs <br/>  Models\Transaction\Customer.cs<br/>  Models\Transaction\Payment.cs<br/>  Models\Product.cs<br/>  Models\Review.cs<br/>  Controls\TitleView.cs<br/>  Controls\BorderlessEntry.cs<br/>  Behaviors\BorderlessEntryCVVBehavior.cs<br/>  Helpers\RTLHelper.cs<br/>  Helpers\PaymentTemplateSelector.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Resources\drawable\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  scale-100\Card.png<br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Payment Success Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Extended,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Transaction\PaymentSuccessPage.xaml<br/>  Views\Transaction\PaymentSuccessPage.xaml.cs<br/>  Views\Transaction\Styles.xaml<br/>  Views\Transaction\Styles.xaml.cs<br/>  ViewModels\Transaction\PaymentViewmodel.cs<br/>  Controls\SVGImage.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\PaymentSuccess.svg<br/>  Controls\TitleView.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr><tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Payment Failure Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  SkiaSharp.Extended,<br/>  SkiaSharp.Svg,<br/>  SkiaSharp.Views.Forms<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Transaction\PaymentFailurePage.xaml<br/>  Views\Transaction\PaymentFailurePage.xaml.cs<br/>  Views\Transaction\Styles.xaml<br/>  Views\Transaction\Styles.xaml.cs<br/>  ViewModels\Transaction\PaymentViewmodel.cs <br/>  Controls\SVGImage.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Images\PaymentFailure.svg<br/>  Controls\TitleView.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Bookmark

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Wishlist Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfBadgeView,<br/>  Syncfusion.Xamarin.SfPopupLayout,<br/>  Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Bookmarks\WishlistPage.xaml<br/>  Views\Bookmarks\WishlistPage.xaml.cs<br/>  Views\Bookmarks\Styles.xaml<br/>  Views\Bookmarks\Styles.xaml.cs<br/>  ViewModels\Bookmarks\WishlistViewModel.cs <br/>  Converters\IntToThicknessConverter.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Controls\TitleView.cs<br/>  Controls\SfPopupView.cs<br/>  Helpers\RTLHelper.cs<br/>  Behaviors\SfComboBoxDropDownBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  DataService\WishlistDataService.cs<br/>  Data\ecommerce.json<br/>  Models\Product.cs<br/>  Models\Review.cs<br/>  Views\Templates\WishlistItemTemplate.xaml <br/>  Views\Templates\WishlistItemTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Cart Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfPopupLayout,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Bookmarks\CartPage.xaml<br/>  Views\Bookmarks\CartPage.xaml.cs<br/>  Views\Bookmarks\PriceDetailView.xaml<br/>  Views\Bookmarks\PriceDetailView.xaml.cs<br/>  Views\Bookmarks\Styles.xaml<br/>  Views\Bookmarks\Styles.xaml.cs<br/>  ViewModels\Bookmarks\CartPageViewModel.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Models\Product.cs<br/>  Models\Review.cs<br/>  Data\ecommerce.json<br/>  DataService\CartDataService.cs<br/>  Controls\TitleView.cs<br/>  Controls\SfPopupView.cs<br/>  Helpers\RTLHelper.cs<br/>  Behaviors\SfComboBoxDropDownBehavior.cs<br/>  Behaviors\ItemTemplateButtonBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\BorderlessEntry.cs<br/>  Views\Templates\CartItemListTemplate.xaml<br/>  Views\Templates\CartItemListTemplate.xaml.cs <br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs <br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Renderers\BorderlessEntryRenderer.cs<br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Article Bookmark<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfPopupLayout,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfRating<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Bookmarks\BookmarksPage.xaml<br/>  Views\Bookmarks\BookmarksPage.xaml.cs<br/>  Views\Bookmarks\Styles.xaml<br/>  Views\Bookmarks\Styles.xaml.cs<br/>  ViewModels\Bookmarks\BookmarksViewModel.cs<br/>  Models\Article.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  Controls\SfPopupView.cs<br/>  Converters\BooleanToStringConverter.cs<br/>  Behaviors\ItemTemplateButtonBehavior.cs<br/>  Converters\DynamicResourceToColorConverter.cs<br/>  Views\Templates\ArticleListTemplate.xaml<br/>  Views\Templates\ArticleListTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
</table>

## History

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Transaction History Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\History\TransactionHistoryPage.xaml<br/>  Views\History\TransactionHistoryPage.xaml.cs<br/>  ViewModels\History\TransactionHistoryViewModel.cs<br/>  Converters\BooleanToColorConverter.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Models\History\Transaction.cs<br/>  Helpers\RTLHelper.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		My Orders Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.SfTabView,<br/>  Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.SfComboBox,<br/>  Syncfusion.Xamarin.SfRating<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\History\MyOrdersPage.xaml<br/>  Views\History\MyOrdersPage.xaml.cs<br/>  Views\History\MyOrdersView.xaml<br/>  Views\History\MyOrdersView.xaml.cs<br/>  ViewModels\History\MyOrdersPageViewModel.cs<br/>  Controls\SVGImage.cs<br/>  Converters\StringToColorConverter.cs<br/>  Models\History\Orders.cs<br/>  Data\ecommerce.json<br/>  DataService\MyOrdersDataService.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Views\Templates\OrderHistoryTemplate.xaml<br/>  Views\Templates\OrderHistoryTemplate.xaml.cs<br/>  Views\Templates\Styles.xaml<br/>  Views\Templates\Styles.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Social

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Social Profile with Connections Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Social\SocialProfileWithConnectionsPage.xaml<br/>  Views\Social\SocialProfileWithConnectionsPage.xaml.cs <br/>  Views\Social\Templates\ProfileTemplate.xaml<br/>  Views\Social\Templates\ProfileTemplate.xaml.cs<br/>  Views\Social\Styles.xaml<br/>  Views\Social\Styles.xaml.cs<br/>  ViewModels\Social\SocialProfileViewModel.cs<br/>  Models\Profile.cs<br/>  Behaviors\SfListViewExtendHeightBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\CustomShadowFrame.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Social Profile with Card Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Social\SocialProfileWithCardPage.xaml<br/>  Views\Social\SocialProfileWithCardPage.xaml.cs<br/>  Views\Social\Templates\ProfileTemplate.xaml<br/>  Views\Social\Templates\ProfileTemplate.xaml.cs<br/>  Views\Social\Styles.xaml<br/>  Views\Social\Styles.xaml.cs<br/>  ViewModels\Social\SocialProfileViewModel.cs<br/>  Models\Profile.cs<br/>  Controls\CustomShadowFrame.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Social Profile with Interests Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Core,<br/>  Syncfusion.Xamarin.SfListView,<br/>  Syncfusion.Xamarin.Buttons<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Social\SocialProfileWithInterestsPage.xaml<br/>  Views\Social\SocialProfileWithInterestsPage.xaml.cs<br/>  Views\Social\Templates\ProfileTemplate.xaml<br/>  Views\Social\Templates\ProfileTemplate.xaml.cs<br/>  Views\Social\Styles.xaml<br/>  Views\Social\Styles.xaml.cs<br/>  ViewModels\Social\SocialProfileViewModel.cs<br/>  Models\Profile.cs<br/>  Behaviors\SfListViewExtendHeightBehavior.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\CustomShadowFrame.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/> 
		</td>
	</tr>
</table>

## Profile

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Author Profile Page<br
		</td>
		<td>
		Syncfusion.Xamarin.Buttons<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Profile\ProfilePage.xaml<br/>  Views\Profile\ProfilePage.xaml.cs<br/>  Views\Profile\Styles.xaml<br/>  Views\Profile\Styles.xaml.cs<br/>  ViewModels\Profile\ProfileViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Controls\TitleView.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			2<br/>
		</td>
		<td>
		Contacts Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Profile\ContactProfilePage.xaml <br/>  Views\Profile\ContactProfilePage.xaml.cs<br/>  Views\Profile\Styles.xaml<br/>  Views\Profile\Styles.xaml.cs<br/>  ViewModels\Profile\ContactProfileViewModel.cs<br/>  Models\Profile.cs<br/>  Helpers\RTLHelper.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			3<br/>
		</td>
		<td>
		Chat Profile Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons<br/> 
		</td>
		<td>
		 <b>PCL:</b><br/>  Views\Profile\ChatProfilePage.xaml <br/>  Views\Profile\ChatProfilePage.xaml.cs<br/>  Views\Profile\Styles.xaml<br/>  Views\Profile\Styles.xaml.cs<br/>  ViewModels\Profile\ChatProfileViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
	<tr valign="top">		
		<td align="center">
			4<br/>
		</td>
		<td>
		Master Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.Buttons,<br/>  Syncfusion.Xamarin.Cards<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Profile\MasterPage.xaml<br/>  Views\Profile\MasterPage.xaml.cs<br/>  Views\Profile\Styles.xaml<br/>  Views\Profile\Styles.xaml.cs<br/>  ViewModels\Profile\MasterPageViewModel.cs<br/>  Helpers\RTLHelper.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  ViewModels\BaseViewModel.cs<br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b> <br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
</table>

## Tracking

<table>
	<tr>
		<th>
			S.No<br/>
		</th>
		<th>
			Pages<br/>
		</th>
		<th>
			Packages<br/>
		</th>
		<th>
			Required Files<br/>
		</th>
	</tr>
	<tr valign="top">		
		<td align="center">
			1<br/>
		</td>
		<td>
		Product Delivery Tracking Page<br/>
		</td>
		<td>
		Syncfusion.Xamarin.SfProgressBar,<br/>  Syncfusion.Xamarin.Core<br/>
		</td>
		<td>
		<b>PCL:</b><br/>  Views\Tracking\ProductDeliveryTrackingPage.xaml<br/>  Views\Tracking\ProductDeliveryTrackingPage.xaml.cs <br/>  Views\Tracking\Styles.xaml<br/>  Views\Tracking\Styles.xaml.cs<br/>  Models\Tracking\ProductDeliveryTrackingModel.cs<br/>  ViewModels\Tracking\ProductDeliveryTrackingViewModel.cs<br/>  Themes\LightTheme.xaml<br/>  Themes\LightTheme.xaml.cs<br/>  Converters\DatetimeToColorConverter.cs<br/>  Data\deliverytracking.json<br/>  DataService\ProductDeliveryTrackingDataService.cs<br/>  ViewModels\BaseViewModel.cs<br/>   <br/>  <b>Android:</b><br/>  Assets\UIFontIcons.ttf <br/>  Assets\Montserrat-Bold.ttf <br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>   <br/>  <b>iOS:</b><br/>  Resources\UIFontIcons.ttf<br/>  Resources\Montserrat-Bold.ttf<br/>  Resources\Montserrat-Medium.ttf<br/>  Resources\Montserrat-Regular.ttf<br/>  Resources\Montserrat-SemiBold.ttf<br/>   <br/>  <b>UWP:</b><br/>  Assets\UIFontIcons.ttf<br/>  Assets\Montserrat-Bold.ttf<br/>  Assets\Montserrat-Medium.ttf<br/>  Assets\Montserrat-Regular.ttf<br/>  Assets\Montserrat-SemiBold.ttf<br/>
		</td>
	</tr>
</table>	