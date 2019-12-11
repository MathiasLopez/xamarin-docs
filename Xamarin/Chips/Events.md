---
layout : post
title : Events for Syncfusion ChipGroup control in Xamarin.Forms
description : Learn more about SfChipGroup events SelectionChanging and SelectionChanged
platform : xamarin
control : Chips
documentation : ug
---

# Event

## SelectionChanging Event
The [SelectionChanging](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangingEventArgs.html) event is triggered before the Chip is selected. You can restrict a chip from being selected, by canceling this event, by setting Cancel property in the event argument to true. The argument contains the following information,

 * [AddedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangingEventArgs~AddedItem.html) - Used to get the selected chip from [SfChipGroup](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfChipGroup.html).
 * [RemovedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangingEventArgs~RemovedItem.html) - Used to get the previous selected or deselected chip from [SfChipGroup](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfChipGroup.html).
 * [Cancel](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangingEventArgs~Cancel.html) - Used to set the value indicating whether the selection should be canceled. 

## SelectionChanged Event
The [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangedEventArgs.html
) event triggered after a chip is selected. The argument contains the following information,

 * [AddedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangedEventArgs~AddedItem.html
) - Get the selected chip from [SfChipGroup](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfChipGroup.html).
 * [RemovedItem](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangedEventArgs~RemovedItem.html
) - Get the previous selected or deselected chip from [SfChipGroup](https://help.syncfusion.com/cr/xamarin/Syncfusion.Buttons.XForms~Syncfusion.XForms.Buttons.SfChipGroup.html).

N>  Currently, `Choice` and `Filter` types are only supported for [SelectionChanging](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangingEventArgs.html) and [SelectionChanged](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Buttons.XForms~Syncfusion.Buttons.XForms.SfChip.SelectionChangedEventArgs.html
) events.
