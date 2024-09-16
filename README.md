# Getting Started with WPF Tabcontrol (TabControlExt)

This repository contains the sample to get started with the Syncfusion's Tabcontrol for WPF.

##  Adding WPF TabControl via XAML
To add the TabControl manually in XAML, follow these steps:

1.  Create a new WPF project in Visual Studio.

2.  Add the following required assembly references to the project:

    *    Syncfusion.Tools.WPF
    *    Syncfusion.Shared.WPF
3.  Import Syncfusion WPF schema http://schemas.syncfusion.com/wpf, and declare the TabControl in XAML page.

**[XAML]**

```
<Grid Name="grid">
    <syncfusion:TabControlExt Name="tabControl" Height="100" Width="280" />
</Grid>
```

##  Adding WPF TabControl via C#
To add the TabControl control manually in C#, follow these steps:

1.  Create a new WPF application via Visual Studio.

2.  Add the following assembly references to the project,
    *   Syncfusion.Shared.WPF
3.  Include the required namespace and create an instance of TabControl and add it to the window.

4.  Declare the TabControl control using C#.

**[C#]**
```
using Syncfusion.Windows.Tools.Controls;
   
public partial class MainWindow : Window 
{
    public MainWindow() 
    {
        InitializeComponent();
   
        // Creating an instance of the TabControl
        TabControlExt tabControlExt = new TabControlExt();
   
        // Setting height and width to TabControl
        tabControlExt.Height = 100;
        tabControlExt.Width = 280;
   
        //Adding TabControl as window content
        this.Content = tabControlExt;
    }
}
```

## How to run this application?

To run this application, you need to first clone the getting-started-with-wpf-tabcontrol repository and then open it in Visual Studio 2022. Now, simply build and run your project to view the output.

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## License

Syncfusion has no liability for any damage or consequence that may arise by using or viewing the samples. The samples are for demonstrative purposes, and if you choose to use or access the samples, you agree to not hold Syncfusion liable, in any form, for any damage that is related to use, for accessing, or viewing the samples. By accessing, viewing, or seeing the samples, you acknowledge and agree Syncfusion’s samples will not allow you seek injunctive relief in any form for any claim related to the sample. If you do not agree to this, do not view, access, utilize, or otherwise do anything with Syncfusion’s samples.