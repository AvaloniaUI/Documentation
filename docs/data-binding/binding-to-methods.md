### Binding to Methods
In Avalonia you could also bind to methods directly without creating a Command.
Consider this simple ViewModel:
```csharp
public class MyViewModel
{
    public bool IsMethodExecuted { get; set; }
    public void MyMethod()
    {
        IsMethodExecuted = true;
    }
}
```
let's add a simple button to our View:
```xml
 <Button Command="{Binding MyMethod}" Content="MyContent"/>
```
Here we are assuming you have set `MyViewModel` as DataContext to the View.

![Gif](https://user-images.githubusercontent.com/53405089/172401616-9d0a6956-4d19-4bbc-b658-7b84142f43d5.gif)
It just works!

Let's consider more complex examples.
