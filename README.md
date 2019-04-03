Android Sunflower Java(alpha)
=========================
[![CircleCI](https://circleci.com/gh/googlesamples/android-sunflower/tree/master.svg?style=shield)](https://circleci.com/gh/googlesamples/android-sunflower/tree/master)



>This project forked from [googlesamples/android-sunflower](https://github.com/googlesamples/android-sunflower) . I translated all **Kotlin** implementaions to **Java**, and added **[app-java]** module as the Java version of Sunflower app, so there are two app modules in  [**Android Sunflower Java**](https://github.com/hatewx/android-sunflower-java):
>
>**[app]**           Kotlin implementation of Sunflower app. 
>[README](./README-kotlin.md)
>
>**[app-java]**   Java implementation of Sunflower app. 
>[中文 README](./README-cn.md)
>
>
>
>The the Intention to create [**Android Sunflower Java**](https://github.com/hatewx/android-sunflower-java):
>
>+ Many people may find it difficult to learn [Android Jetpack](https://developer.android.com/jetpack/) because they are not familiar with Kotlin.
>+ Many teams are keen to implement [Android Jetpack](https://developer.android.com/jetpack/) in existing projects, but still prefer to use the java language to approach.



A gardening app illustrating Android development best practices with Android Jetpack.

Android Sunflower is currently released as an alpha and is under heavy development. To view the
latest changes, please visit the
[Releases page](https://github.com/googlesamples/android-sunflower/releases).
Note that some changes (such as database schema modifications) are not backwards
compatible during this alpha period and may cause the app to crash. In this
case, please uninstall and re-install the app.

Introduction
------------

Android Jetpack is a set of components, tools and guidance to make great Android apps. They bring
together the existing Support Library and Architecture Components and arranges them into four
categories:

![Android Jetpack](screenshots/jetpack_donut.png "Android Jetpack Components")

Android Sunflower demonstrates utilizing these components to create a simple gardening app.
Read the
[Introducing Android Sunflower](https://medium.com/androiddevelopers/introducing-android-sunflower-e421b43fe0c2)
article for a walkthrough of the app.

Getting Started
---------------
This project uses the Gradle build system. To build this project, use the
`gradlew build` command or use "Import Project" in Android Studio.

There are two Gradle tasks for testing the project:
* `connectedAndroidTest` - for running Espresso on a connected device
* `test` - for running unit tests

For more resources on learning Android development, visit the
[Developer Guides](https://developer.android.com/guide/) at
[developer.android.com](https://developer.android.com).

Screenshots
-----------

![List of plants](screenshots/phone_plant_list.png "A list of plants")
![Plant details](screenshots/phone_plant_detail.png "Details for a specific plant")
![My Garden](screenshots/phone_my_garden.png "Plants that have been added to your garden")

Libraries Used
--------------
* [Foundation][0] - Components for core system capabilities and support for
  multidex and automated testing.
  * [AppCompat][1] - Degrade gracefully on older versions of Android.
  * [Test][4] - An Android testing framework for unit and runtime UI tests.
* [Architecture][10] - A collection of libraries that help you design robust, testable, and
  maintainable apps. Start with classes for managing your UI component lifecycle and handling data
  persistence.
  * [Data Binding][11] - Declaratively bind observable data to UI elements.
  * [Lifecycles][12] - Create a UI that automatically responds to lifecycle events.
  * [LiveData][13] - Build data objects that notify views when the underlying database changes.
  * [Navigation][14] - Handle everything needed for in-app navigation.
  * [Room][16] - Access your app's SQLite database with in-app objects and compile-time checks.
  * [ViewModel][17] - Store UI-related data that isn't destroyed on app rotations. Easily schedule
     asynchronous tasks for optimal execution.
  * [WorkManager][18] - Manage your Android background jobs.
* [UI][30] - Details on why and how to use UI Components in your apps - together or separate
  * [Animations & Transitions][31] - Move widgets and transition between screens.
  * [Fragment][34] - A basic unit of composable UI.
  * [Layout][35] - Lay out widgets using different algorithms.
* Third party
  * [Glide][90] for image loading

[0]: https://developer.android.com/jetpack/foundation/
[1]: https://developer.android.com/topic/libraries/support-library/packages#v7-appcompat
[2]: https://developer.android.com/kotlin/ktx
[4]: https://developer.android.com/training/testing/
[10]: https://developer.android.com/jetpack/arch/
[11]: https://developer.android.com/topic/libraries/data-binding/
[12]: https://developer.android.com/topic/libraries/architecture/lifecycle
[13]: https://developer.android.com/topic/libraries/architecture/livedata
[14]: https://developer.android.com/topic/libraries/architecture/navigation/
[16]: https://developer.android.com/topic/libraries/architecture/room
[17]: https://developer.android.com/topic/libraries/architecture/viewmodel
[18]: https://developer.android.com/topic/libraries/architecture/workmanager
[30]: https://developer.android.com/jetpack/ui/
[31]: https://developer.android.com/training/animation/
[34]: https://developer.android.com/guide/components/fragments
[35]: https://developer.android.com/guide/topics/ui/declaring-layout
[90]: https://bumptech.github.io/glide/
[91]: https://kotlinlang.org/docs/reference/coroutines-overview.html

Upcoming features
-----------------
Updates will include incorporating additional Jetpack components and updating existing components
as the component libraries evolve.

Interested in seeing a particular feature of the Android Framework or Jetpack implemented in this
app? Please open a new [issue](https://github.com/googlesamples/android-sunflower/issues).

Android Studio IDE setup
------------------------
For development, the latest version of Android Studio 3.3 is required. The latest version can be
downloaded from [here](https://developer.android.com/studio/).

Additional resources
--------------------
Check out these Wiki pages to learn more about Android Sunflower:

- [Notable Community Contributions](https://github.com/googlesamples/android-sunflower/wiki/Notable-Community-Contributions)

- [Publications](https://github.com/googlesamples/android-sunflower/wiki/Sunflower-Publications)

Non-Goals
---------
The focus of this project is on Android Jetpack and the Android framework.
Thus, there are no immediate plans to implement features outside of this scope.

A note on dependency injection - while many projects (such as
[Plaid](https://github.com/nickbutcher/plaid)) use
[Dagger 2](https://github.com/google/dagger) for DI, there are no plans to
incorporate DI into Sunflower.  This allows developers unfamiliar with dependency
injection to better understand Sunflower's code without having to learn DI.

Support
-------

- Google+ Community: https://plus.google.com/communities/105153134372062985968
- Stack Overflow:
  - http://stackoverflow.com/questions/tagged/android
  - http://stackoverflow.com/questions/tagged/android-jetpack

If you've found an error in this sample, please file an issue:
https://github.com/googlesamples/android-sunflower/issues

Patches are encouraged, and may be submitted by forking this project and submitting a pull request
through GitHub.

Third Party Content
-------------------
Select text used for describing the plants (in `plants.json`) are used from Wikipedia via CC BY-SA 3.0 US (license in `ASSETS_LICENSE`).

License
-------

Copyright 2018 Google, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
