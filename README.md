# 👋 Introduction to Avalonia

## Welcome

Welcome to Avalonia - the best open source, easy to learn .NET C\# multiplatform package for desktop \(Windows, Mac and Linux\)  development.

* Avalonia is under rapid development by [a large group of open source contributors](https://github.com/AvaloniaUI/Avalonia/graphs/contributors).
* Avalonia is [100% open source - and will continue as an open source project](https://github.com/AvaloniaUI/Avalonia), has constantly expanding documentation and a large number of open source samples showing how to use it.
* Avalonia has [free support on Avalonia Gitter](https://gitter.im/AvaloniaUI/Avalonia), one can also post questions on [Avalonia Github Discussions](https://github.com/AvaloniaUI/Avalonia/discussions). If you're in need of more support you can opt for a  [paid support plan](https://avaloniaui.net/support.html) which helps support the continued growth of the project.
* Avalonia has Visual Studio and Rider support for creating XAML files while having advantage of XAML IntelliSense. Visual Studio also has a visual preview.
* Avalonia has a tool that facilitate the visual development and debugging called [DevTools](docs/getting-started/developer-tools.md). This tool is also multiplatform - meaning you can use it on Mac and Linux and completely open source.

If you're familiar with WPF or UWP then you should feel right at home with Avalonia. Although Avalonia is not API compatible with either of these frameworks \(and so controls can't be used without porting\), there's a lot of similarity. If you're a WPF user we have a [page which describes the main differences between WPF and Avalonia](misc/wpf/).


## Why Avalonia is a Hit

* Avalonia allows creating applications that look and behave the same on most popular Desktop platforms \(Windows, Mac, various flavors of Linux\) while also allowing the platform specific customizations.
* Avalonia is supported by the following companies:

| | | | 
|:---:|:---:|:---:|
| [![](.gitbook/assets/se.png)](https://www.se.com/us/en/) | [![](.gitbook/assets/jblogo%20%282%29.png)](https://www.jetbrains.com/)  | [![](.gitbook/assets/unitylogo.png)](https://unity.com/) |
| [![](.gitbook/assets/logo_thales_500.png)](https://www.thalesgroup.com/) | [![](.gitbook/assets/synergy-logo.png)](https://synergysports.com/)  | [![](.gitbook/assets/gritworld-logo.png)](https://en.gritworld.com/) |
| [![](.gitbook/assets/wasabi-wallet-logo.svg)](https://www.wasabiwallet.io/) | [![](.gitbook/assets/mailbird-logo.png)](https://www.getmailbird.com/) |

  and many other smaller companies.

* Avalonia \(just like WPF and Silverlight\) is fully compositional: you can create a button out of Avalonia primitives in a fashion similar to creating a complex page, while its competitors \(Web, Xamarin and Java\) packages are not compositional to the same degree.
* Avalonia UI, unlike JavaScript has full advantage of a strongly typed language. Also Avalonia has full advantage of a compiled-to-binary code language.
* Avalonia is an open source multiplatform descendant of great Microsoft packages - WPF and Silverlight which brought the UI development on a completely new level creating a set of new concepts and which allow to create a full blown UI application in fraction of time and effort in comparison to other technologies. Here is the list of some of the concepts:

  * Visual and Logical Trees
  * Attached or Dependency Properties which can be defined outside of the object on which they are used and do not take any extra memory unless they are assigned a non-default value and have a special event to fire when their values change.
  * Attached Routed Events that can be defined outside of the objects that fire them and can propagate and be handled up and down on the trees.
  * Bindings and the related MVVM pattern
  * Control Templates
  * Data Templates
  * Styles
  * Behaviors provide way to modify and augment the behavior of a C\# class without modifying the class itself by using the events.

  All these paradigms have been implemented for multiple platforms in Avalonia.

## Supported .NET Version

Avalonia is supported on [all platforms that support .NET Standard 2.0](https://github.com/dotnet/standard/blob/master/docs/versions/netstandard2.0.md#platform-support)

## Supported Platforms

Avalonia is supported on the following platforms:

* Windows 8 and higher
  * **Note**: Avalonia works correctly on Windows 7 also,but not supported *officially*
* MaxOS High Sierra 10.13 and higher
* for Linux:
  * Debian 9 \(Stretch\) and higher
  * Ubuntu 16.5 and higher
  * Fedora 30 and higher

## Supported Development Environments

The following environments support Avalonia XAML with IntelliSense:

* Visual Studio 2017 and higher \(with or without Resharper 2020.3\). Avalonia Visual Designer is also supported.
* JetBrains Rider 2020.3 and higher.

[Installing Avalonia Extension for Visual Studio](docs/getting-started/ide-support/README.md)

[JetBrains Rider Setup](docs/getting-started/ide-support/jetbrains-rider-setup.md)
