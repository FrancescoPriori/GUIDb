# GUIDb

 creare un nuovo progetto MAUI (App .NET MAUI)
 
 ![creazione MAUI](https://github.com/FrancescoPriori/GUIDb/assets/116790887/a5891165-7304-46ee-886b-c6c00b7d59a3)
 
 Aggiungere il file chinook.db alla cartella Raw

![Raw](https://github.com/FrancescoPriori/GUIDb/assets/116790887/7a07a2e2-ab1c-4787-96ce-31bd39905b83)

impostare copia sempre sulle proprieta del file 

![copia sempre](https://github.com/FrancescoPriori/GUIDb/assets/116790887/9b2b8940-588e-479f-9c4a-220eed93dac5)

Creare la classe Record.cs
Tasto destro sul nome del progetto tasto sinistro su aggiungi e tasto sinistro su classe


![classe](https://github.com/FrancescoPriori/GUIDb/assets/116790887/34cfe0ff-22b1-4f97-a96c-14699b960b07)

Nella classe Recors.cs scrivere:
```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace priori.francesco._4h.GUIDb
{
   public class Album
   {
       public int AlbumId { get; set; }
       public string Title { get; set; }
       public int ArtistId { get; set; }
   }

   public class Artist
   {
       public int ArtistId { get; set; }
       public string Name { get; set; }
   }

   public class Track
   {
       public int TrackId { get; set; }
       public string Name { get; set; }
       public int AlbumId { get; set; }
       public int MediaTypeId { get; set; }
       public int GenreId { get; set; }
       public string Composer { get; set; }
       public Int64 Milliseconds { get; set; }
       public Int64 Bytes { get; set; }
       public double UnitPrice { get; set; }

   }
}
```
In MainPage.xaml scrivere:
```
<Window x:Class="priori.francesco._4h.GUIDb.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:priori.francesco._4h.GUIDb.MainWindow"
        mc:Ignorable="d"
        Title="MainWindow" Height="450" Width="800">
    <Grid>
        <StackPanel Orientation="Vertical">
            <StackPanel>
                <Button Width="100" Click="Button_Click"></Button>
            </StackPanel>

            <DataGrid x:Name="dgDati"></DataGrid>
        </StackPanel>
    </Grid>
</Window>
```

