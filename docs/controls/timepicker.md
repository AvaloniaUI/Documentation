# TimePicker

The `TimePicker` control allows the user to pick a time value.

### Examples

This example shows how to create a simple time picker with a header in XAML or in code.

{% tabs %}
{% tab title="XAML" %}
```markup
<TimePicker Header="Arrival time"/>
```
{% endtab %}

{% tab title="CS" %}
```csharp
TimePicker arrivalTimePicker = new TimePicker();
arrivalTimePicker.Header = "Arrival time";
```
{% endtab %}
{% endtabs %}

### Remarks <a id="remarks"></a>

Use a `TimePicker` to let a user enter a single time value. You can customize the `DatePicker` to use a 12-hour or 24-hour clock.

![](../../.gitbook/assets/image%20%2822%29.png)

### 12-hour and 24-hour clocks

By default, the time picker shows a 12-hour clock with an AM/PM selector. You can set the [ClockIdentifier](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.controls.timepicker.clockidentifier?view=winrt-19041#Windows_UI_Xaml_Controls_TimePicker_ClockIdentifier) property to "24HourClock" to show a 24-hour clock instead.

```markup
<TimePicker Header="12HourClock" SelectedTime="14:30"/>
<TimePicker Header="24HourClock" SelectedTime="14:30" ClockIdentifier="24HourClock"/>
```

![](../../.gitbook/assets/image%20%2819%29.png)

#### Minute increment <a id="minute-increment"></a>

You can set the [MinuteIncrement](https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.controls.timepicker.minuteincrement?view=winrt-19041#Windows_UI_Xaml_Controls_TimePicker_MinuteIncrement) property to indicate the time increments shown in the minute picker. For example, 15 specifies that the `TimePicker` minute control displays only the choices 00, 15, 30, 45.

```markup
<TimePicker MinuteIncrement="15"/>
```

![](../../.gitbook/assets/image%20%2810%29.png)

#### Time values <a id="time-values"></a>

The time picker control has both Time / TimeChanged and SelectedTime / SelectedTimeChanged APIs. The difference between these is that `Time` is not nullable, while `SelectedTime` is nullable.

The value of `SelectedTime` is used to populate the time picker and is `null` by default. If `SelectedTime` is `null`, the `Time` property is set to a [TimeSpan](https://docs.microsoft.com/en-us/dotnet/api/system.timespan?view=dotnet-uwp-10.0&preserve-view=true) of 0; otherwise, the `Time` value is synchronized with the `SelectedTime` value. When `SelectedTime` is `null`, the picker is 'unset' and shows the field names instead of a time.

![](../../.gitbook/assets/image%20%2820%29.png)

**Initializing a time value**

In code, you can initialize the time properties to a value of type `TimeSpan`:

```csharp
TimePicker timePicker = new TimePicker
{
    SelectedTime = new TimeSpan(14, 15, 00) // Seconds are ignored.
};
```

You can set the time value as an attribute in XAML. This is probably easiest if you're already declaring the `TimePicker` object in XAML and aren't using bindings for the time value. Use a string in the form _Hh:Mm_ where _Hh_ is hours and can be between 0 and 23 and _Mm_ is minutes and can be between 0 and 59.

```markup
<TimePicker SelectedTime="14:15"/>
```

To use the time value in your app, you typically use a data binding to the `SelectedTime`or `Time` property, use the time properties directly in your code, or handle the `SelectedTimeChanged` or `TimeChanged` event. 

### Reference <a id="reference"></a>

[TimePicker](http://reference.avaloniaui.net/api/Avalonia.Controls/TimePicker/)

### Source code <a id="source-code"></a>

[TimePicker.cs](https://github.com/AvaloniaUI/Avalonia/blob/master/src/Avalonia.Controls/DateTimePickers/TimePicker.cs)

