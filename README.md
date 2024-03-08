<a href="https://github.com/sponsors/FANMixco/" target="_blank">
   <img src="https://raw.githubusercontent.com/FANMixco/Xamarin-SearchBar/master/bmc-rezr5vpd.gif" alt="sponsor" />
</a>

# Xamarin-OneMoreFabMenu

Another floating action button menu with expand/collapse behavior. This Xamarin solution is based on André Servidoni's version: https://github.com/DeKoServidoni/OMFM

![Example gif](https://raw.githubusercontent.com/DeKoServidoni/OMFM/master/images/example_v1.0.3.gif) 

## How to use

### **Basic example:**

**XML:**

```xml
<com.dekoservidoni.omfm.OneMoreFabMenu
	android:id="@+id/fabMenu"
	android:layout_width="wrap_content"
	android:layout_height="wrap_content"
	android:layout_gravity="bottom|end"
	app:content_options="@menu/omfm_content_options"
	app:color_main_button="@color/colorPrimaryDark"
	app:close_on_click="true"
	app:color_secondary_buttons="@color/colorPrimary"
	app:expanded_background_color="@color/colorGrayTrans"/>
```

**Menu:**

**omfm_content_options.xml**

```xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

	<!-- First button is the initial Fab of the menu -->
	<!-- Don't need the title in this case, so let it empty -->
	<item
		android:id="@+id/main_option"
		android:icon="@drawable/icon1"
		android:title=""/>

	<!-- Options buttons of the Fab menu -->

	<item
		android:id="@+id/option1"
		android:icon="@drawable/icon2"
		android:title="@string/options_1" />

	<item
		android:id="@+id/option2"
		android:icon="@drawable/icon3"
		android:title="@string/options_2" />

	<item
		android:id="@+id/option3"
		android:icon="@drawable/icon4"
		android:title="@string/options_3" />
</menu>
```

**C#:**

```csharp
private OneMoreFabMenu FabButtonMenu { get; set; }

public partial class MainActivity : AppCompatActivity, OneMoreFabMenu.IOptionsClick
{
	protected override async void OnCreate(Bundle savedInstanceState)
	{
		base.OnCreate(savedInstanceState);
		FabButtonMenu = FindViewById<OneMoreFabMenu>(Resource.Id.fabMenu);
		FabButtonMenu.SetOptionsClick(this);
	}
}

public void OnOptionClick(Integer p0)
{
	switch (Convert.ToInt32(p0))
	{
		case Resource.Id.option1:
			break;
		case Resource.Id.option2:
			break;
		case Resource.Id.option3:
			break;
	}
}
```

## Download

|  Package  |Latest Release|
|:----------|:------------:|
|**Xamarin-OneMoreFabMenu**|[![NuGet Badge Xamarin-OneMoreFabMenu](https://buildstats.info/nuget/Xamarin-OneMoreFabMenu)](https://www.nuget.org/packages/Xamarin-OneMoreFabMenu/)|

## Licence

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

### Follow me at:

|  LinkedIn  |YouTube|Amazon|Goodreads|Instagram|Cyber Prophets|Sharing Your Stories|
|:----------|:------------:|:------------:|:------------:|:------------:|:------------:|:------------:|
|[![LinkedIn](https://i.stack.imgur.com/idQWu.png)](https://bit.ly/lfanmixco)|[![YouTube](https://i.stack.imgur.com/CFPMR.png)](https://youtube.com/c/FedericoNavarrete)|[![Amazon](https://i.stack.imgur.com/NFOeE.png)](https://www.amazon.com/Federico-Navarrete/e/B08NJTXQRV)|[![Goodreads](https://i.stack.imgur.com/oBk0g.jpg)](https://www.goodreads.com/author/show/21125413.Federico_Navarrete)|[![Instagram](https://i.stack.imgur.com/PIfqY.png)](https://www.instagram.com/federico_the_consultant)|[![RedCircle Podcast](https://i.stack.imgur.com/4XICF.png)](https://redcircle.com/shows/cyber-prophets)|[![RedCircle Podcast](https://i.stack.imgur.com/4XICF.png)](https://redcircle.com/shows/sharing-your-stories)|

