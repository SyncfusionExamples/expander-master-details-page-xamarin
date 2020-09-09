# How to load Expander into MasterDetailsPage in Xamarin.Forms (SfExpander)

You can load the SfExpander[https://help.syncfusion.com/xamarin/expander/getting-started] in the [MasterDetailPage](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.masterdetailpage) in Xamarin.Forms.

You can also refer the folloiwng article.

https://www.syncfusion.com/kb/11923/how-to-work-with-expander-in-the-masterdetailspage-in-xamarin-forms-sfexpander

**XAML**

Load **SfExpander** in the [Master](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.masterdetailpage.master#Xamarin_Forms_MasterDetailPage_Master) page of the **MasterDetailPage**.

``` xml
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:syncfusion="clr-namespace:Syncfusion.XForms.Expander;assembly=Syncfusion.Expander.XForms"
             xmlns:local="clr-namespace:ExpanderXamarin"
             x:Class="ExpanderXamarin.Views.ExpanderMasterDetailMaster"
             Title="Menu">
    <StackLayout>
        <Grid BackgroundColor="#f54291" HeightRequest="100">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="70"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <Image Source="UserImage.png" HeightRequest="60" WidthRequest="60" Margin="10,10,10,10"/>
            <Label Text="John" Grid.Column="1" VerticalOptions="Center" HorizontalOptions="Start"/>
        </Grid>
        <ScrollView BackgroundColor="#EDF2F5">
            <StackLayout>
                <syncfusion:SfExpander HeaderIconPosition="End">
                    <syncfusion:SfExpander.Header>
                        <Grid HeightRequest="50">
                            <Grid.ColumnDefinitions>
                                <ColumnDefinition Width="50"/>
                                <ColumnDefinition Width="*"/>
                            </Grid.ColumnDefinitions>
                            <Image Source="home.png" HeightRequest="25" WidthRequest="25" HorizontalOptions="Center" VerticalOptions="Center"/>
                            <Label Text="Home" Grid.Column="1" TextColor="#495F6E" VerticalTextAlignment="Center" />
                        </Grid>
                    </syncfusion:SfExpander.Header>
 
                    <syncfusion:SfExpander.Content>
                        <StackLayout Padding="10,10,10,10" BackgroundColor="#FFFFFF">
                            <Label HeightRequest="50" Text="Tasks" TextColor="#303030" VerticalTextAlignment="Center" />
                            <Label HeightRequest="50" Text="Settings" TextColor="#303030" VerticalTextAlignment="Center" />
                        </StackLayout>
                    </syncfusion:SfExpander.Content>
                </syncfusion:SfExpander>
            </StackLayout>
        </ScrollView>
    </StackLayout>
</ContentPage>
```

**Output**

![ExpanderMasterDetailsPage](https://github.com/SyncfusionExamples/expander-master-details-page-xamarin/blob/master/ScreenShot/ExpanderMasterDetailsPage.png)
