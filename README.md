# Getting Started with WPF TabControl (TabControlExt)

This sample demonstrates the basic steps to integrate and use the **Syncfusion WPF TabControlExt** control in a WPF application. It shows how to add the control via XAML and C#, configure its size, and create multiple tab items with custom headers and content.

---

## Prerequisites
- **Visual Studio** (latest version recommended)
- **.NET Framework / .NET Core**
- Syncfusion WPF assemblies:
  - `Syncfusion.Tools.WPF`
  - `Syncfusion.Shared.WPF`

---

## Steps to Add TabControlExt

### 1. Create a WPF Project
Open Visual Studio and create a new WPF application.

### 2. Add Required Assemblies
Add references to:
- `Syncfusion.Tools.WPF`
- `Syncfusion.Shared.WPF`

### 3. Import Syncfusion Namespace
Add the following namespace in your XAML file:
```xml
xmlns:syncfusion="http://schemas.syncfusion.com/wpf"
```

---

## Adding TabControl via XAML

```xml
<Window x:Class="TabControlDemo.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:syncfusion="http://schemas.syncfusion.com/wpf"
        mc:Ignorable="d"
        Title="TabControl Demo" Height="450" Width="800">
    <Grid>
        <syncfusion:TabControlExt Name="tabControl"
                                  ShowTabListContextMenu="True"
                                  ShowTabItemContextMenu="True"
                                  TabScrollStyle="Extended"
                                  TabScrollButtonVisibility="Visible"
                                  CloseButtonType="Both"
                                  IsNewButtonEnabled="True"
                                  NewButtonClick="TabControl_NewButtonClick"
                                  TabStripPlacement="Top">

            <syncfusion:TabItemExt Header="tabItem1">
                <TextBlock Text="This is the first tab item." />
                <syncfusion:TabItemExt.ContextMenuItems>
                    <syncfusion:CustomMenuItem Header="Menu1" />
                </syncfusion:TabItemExt.ContextMenuItems>
            </syncfusion:TabItemExt>

            <syncfusion:TabItemExt Header="tabItem2" IsSelected="True" CanClose="False" CloseButtonState="Collapsed">
                <TextBlock Text="This is the second tab item." />
                <syncfusion:TabItemExt.ContextMenuItems>
                    <syncfusion:CustomMenuItem Header="Menu2" />
                </syncfusion:TabItemExt.ContextMenuItems>
            </syncfusion:TabItemExt>

            <syncfusion:TabItemExt Header="tabItem3">
                <TextBlock Text="This is the third tab item." />
                <syncfusion:TabItemExt.ContextMenuItems>
                    <syncfusion:CustomMenuItem Header="Menu3" />
                </syncfusion:TabItemExt.ContextMenuItems>
            </syncfusion:TabItemExt>

        </syncfusion:TabControlExt>
    </Grid>
</Window>
```

---

## Adding TabControl via C#

```csharp
using Syncfusion.Windows.Tools.Controls;

public partial class MainWindow : Window {
    public MainWindow() {
        InitializeComponent();

        // Create TabControlExt instance
        TabControlExt tabControlExt = new TabControlExt {
            Height = 100,
            Width = 280
        };

        // Add TabControl to window
        this.Content = tabControlExt;
    }
}
```
---

## Key Features Demonstrated
- Adding **TabControlExt** via XAML and C#
- Adding multiple **TabItemExt** with custom headers and content
- Enabling **context menus** for individual tabs
- Configuring **close button visibility**
- Adding **New Tab button** with event handling
- Supporting **tab scrolling and placement**

---

## Run the Sample
- **Option 1:** Open the solution in Visual Studio and run.
- **Option 2:** From the project folder (PowerShell):
  - **Build:** `dotnet build`
  - **Run:** `dotnet run`

---

## Documentation
- [Syncfusion WPF Documentation](https://help.syncfusion.com/wpf/tabcontrol/getting-started)
- [TabControlExt API Reference](https://help.syncfusion.com/cr/wpf/Syncfusion.Windows.Tools.Controls.TabControlExt.html)

