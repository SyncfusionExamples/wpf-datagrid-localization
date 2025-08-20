# Localization in WPF DataGrid (SfDataGrid)

This repository contains sample which shows localization of Syncfusion [WPF DataGrid](https://www.syncfusion.com/wpf-controls/datagrid).

[Localization](https://help.syncfusion.com/wpf/localization) is the process of translating the application resources into different language for the specific cultures. You can localize the WPF DataGrid by adding a resource file for each language.

### Changing application culture

When you change the application culture, you can localize the application based on application culture by creating .resx file.

``` csharp
public partial class MainWindow
{
    public MainWindow() 
    {     
        InitializeComponent();  
        System.Threading.Thread.CurrentThread.CurrentUICulture = new System.Globalization.CultureInfo("de");   
    }
}
```

### Creating .resx files

You can create .resx files for any language by following these steps:

1. Right-click your project and add a new folder named as `Resources`.

2. Add the [default resource files](https://github.com/syncfusion/wpf-controls-localization-resx-files) to the libraries you are using to the `Resources` folder and ensure `AccessModifier` is specified as Public.

3. Now, right-click `Resources` folder and select Add and then `NewItem`. In the `Add New Item` wizard, select the Resource File option and name the filename as `Syncfusion.SfGrid.WPF.<culture name>.resx`. For example, you have to give name as `Syncfusion.SfGrid.WPF.de.resx` for `German` culture. In the same way, add new resource files for other libraries used in your application.

4. Now, select Add and add resource file for German culture in `Resources` folder and set `AccessModifier` property to No code generation.

5. Now, you can copy the key names from the default resource files and assign values based on the culture and the resource files’ targets.

![Localized WPF DataGrid](wpf-datagrid-localization.PNG)
