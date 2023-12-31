# JetpackComposeMVVM
Sample Jetpack compose project with MVVM architecture. Project includes Hilt for dependecy injection and Flow for emit the data and collect on UI.

# Jetpack Compose Understandings

- Jetpack Compose provides a native way to navigate through multiple composable components.
- With NavHost and NavController, you can push or pop you composables.
- All those fragment transactions, navigations and intents for activities are handle by Navigation.

#### NavHost
- Graphs are wrapped in a single NavHost. 
- It has declaration of the Routes.

#### navController
- It is initialized at the root and passed to every graph. 
- It is shared among them.
- Every screen have access to the navController.
- It provides API to move around the declared routes.
- Stack can be viewed as a history of the composables

# Frequently used methods are

- rememberNavController()
- navController.navigate("SecondScreen")
- navController.popBackStack()
- navController.popBackStack(inclusive: false)
    - Inclusive parameter tells us if the targeted composable should be removed too

## Video of my work

https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/b2d6bfc6-fd31-485e-8f7d-ed455f60747d

## Features included in this project are

- Jetpack Compose
- MVVM architecture [ model-View-View Model]
- Hilt for DI
- Scaffold
- TopAppBar
- BottomBar [ NavigationBar ]
- BottomNavItem
- Navigation compose
- Retrofit
- OkHttp logging
- Gson converter factory
- Kotlin Coroutine
- Flow for emit and collect data
- Coil for Image loading
- Swipe Refresh in Home and Detail screen
- Adaptive Icon : Theme based Icon support
- Shimmer Effect (Theme based)
- Network Check
- Retry functionality
- App Bar
- Bottom Navigation Bar

## This repository show the List of Country Flags and you can select to know it's name

- Show circular loader until API response come.
- Coil lib used to load the image
- Center crop the image


| #1                                                                                                                                            | #2                                                                                                                                            | #3                                                                                                                                            | #4                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/bdf0a830-b7ce-4e73-9fa8-169e4d7859cb" width="100%" height="100%"> | <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/9ad77585-3eab-4502-b044-d29393da4f43" width="100%" height="100%"> | <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/80c4fa9e-8096-4a98-8dee-6a68dfee0cc4" width="100%" height="100%"> | <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/67d4f10d-e6ab-417d-9e30-049b75dee68c" width="100%" height="100%"> |

### Internet check and Retry feature

<img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/f661f4a1-414f-4b0e-b383-5aace70e757e" width="30%" height="50%">

### Top App Bar and Bottom Navigation

| #1                                                                                                                                            | #2                                                                                                                                            | #3                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/fcee4867-7486-4a8e-b46a-baf839c4d347" width="100%" height="100%"> | <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/fb896992-bfd4-4507-8aff-6bd62e90b75a" width="100%" height="100%"> | <img src="https://github.com/NrupParikh/JetpackComposeMVVM/assets/108717119/2ef7ef43-8c59-4d0b-9cef-e04484758765" width="100%" height="100%"> |

### To support theme based icon (Adaptive Icon) Do below configuration changes.

- compileSdk 33
- targetSdk 33
- Remove android:roundIcon="@mipmap/ic_launcher_round" from AndroidManifest.xml
- in res->drawable folder add one XML file name like adaptive_icon.xml


Add this line

~~~
<monochrome android:drawable="@drawable/adaptive_icon"/>
~~~
So, your anydpi-v26/launcher.xml looks like

~~~
<?xml version="1.0" encoding="utf-8"?>
<adaptive-icon xmlns:android="http://schemas.android.com/apk/res/android">
    <background android:drawable="@color/ic_launcher_background"/>
    <foreground android:drawable="@drawable/ic_launcher_foreground"/>
    <monochrome android:drawable="@drawable/adaptive_icon"/>
</adaptive-icon>
~~~

And make Vector drawable of your app icon with below constraints :

- Make the canvas 108x108 px
- Make the App Icon 48x48 px
- Make sure, icon don't have shadow

- To generate App icon to SVG (png to svg) use
  https://svg2vector.com/


- To create adaptive icon, [48px x 48px]
  make your app icon black and white and make blank space as a transparent.

- Use Paint.net software for that.
Reference:  https://www.getpaint.net/download.html

Reference
https://developer.android.com/develop/ui/views/launch/icon_design_adaptive

## Link to learn compose step by step
https://developer.android.com/courses/android-basics-compose/course

## Other useful links
- Bottom Navigation in Jetpack Compose Android
https://medium.com/geekculture/bottom-navigation-in-jetpack-compose-android-9cd232a8b16

- A simple example of using NavHost and NavController
https://tomas-repcik.medium.com/android-jetpack-compose-and-navigation-59f5ffa1219e

- Putting composables into an appropriate structure
https://betterprogramming.pub/android-jetpack-compose-and-nesting-navigation-f72df5a84691
