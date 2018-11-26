# ToxRatingsControl

This is a very simple but flexible Ratings Control for WPF. The core of the code is based on the control by Sacha Barber that was posted on CodeProject in 2009: https://www.codeproject.com/Articles/45210/WPF-A-Simple-Yet-Flexible-Rating-Control

It almost fitted my needs, but had some quirks. I made several additions and changes to his code, as it did not work correctly in VS 2015 (which I used at the time). The following options were added:
- size of stars can be changed
- allow background to be transparent
- improved mask handling

There is a demo program available to show how to use the control.

## Usage

Add the control to the XAML in the windows (or page) tag:

``` xmlns:external="clr-namespace:ToxRatingsControl;assembly=ToxRatingsControl" ```


Then add the control to the position you want:

```
 <external:RatingsControl x:Name="ratings1" 
                              Value="4.2"
                              NumberOfStars="5"
                              Margin="5" 
                              HorizontalAlignment="Left"
                              StarSize="30"/>
```

And for example in the CS file (can of course also be in the XAML file):
```
ratings1.BackgroundColor = Brushes.Transparent;
ratings1.StarForegroundColor = Brushes.Orange;
ratings1.StarOutlineColor = Brushes.Orange;
```

All the properties are bindable, so it is not required to hardcode them.
