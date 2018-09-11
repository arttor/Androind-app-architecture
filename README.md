# Android native application proposal

## Language  - Kotlin
Pros | Cons
------------ | -------------
Supported by Google - all documentation examples in Kotlin | Experienced Kotlin devs are still a rarity
More strict than Java: Kotlin is null safe by default | 
Easy transition from Java | 
Much more succinct than the Java:<br>  - KTX extensions from Google <br>  - Streams and Lambdas [Android is not fully compatible  with java 8](https://developer.android.com/studio/write/java8-support) <br> - 40% less code than java ([according to study](https://arxiv.org/pdf/1808.00025.pdf)) | 

### Alternatives: Java


## Architecture & Components - Android Jetpack

![Android Jetpack](http://tim4dev.com/wp-content/uploads/2018/05/Screen-Shot-2018-05-05-at-11.49.30-AMimage1.png)

Learn from the best! [Android Jetpack](https://developer.android.com/jetpack/) is Android components and development guidelines suggested by Google: 
> Jetpack is a collection of Android software components to make it easier for you to develop great Android apps. These components help you  follow best practices, free you from writing boilerplate code, and simplify complex tasks, so you can focus on the code you care about.
> Jetpack comprises the androidx.* package libraries, unbundled from the platform APIs. This means that it offers backward compatibility   and is updated more frequently than the Android platform, making sure you always have access to the latest and greatest versions of the Jetpack components.

[Example](https://github.com/googlesamples/android-sunflower)

* UI Components - [Material design](https://material.io/develop/android/)
* DataBinding - bind observable data to UI elements
* Lifecycle-aware-components - provides classes and interfaces that let you build components—which can automatically adjust their behavior based on the current lifecycle state of an activity or fragment
* LiveData - lifecycle-aware observable data holder
* Room - SQLite persistance library
* Retrofit - REST client
* Dagger 2 - dependency injection
* Test
  * Unit - JUnit + Mockito
  * UI - Espresso
![Architecture](https://developer.android.com/topic/libraries/architecture/images/final-architecture.png)
### Summary
Combination of listed components will help to:
 * avoid memory leaks by using lifecycle-aware components
 * build responsive app with LiveData observable
 * automatically maintain application state between screen transformations by using ViewModel
 * provide better user expreince in offline-mode or due poor connection conditions (cache remote data with SQLite & room and perform remote calls in background)
 * separate data model and logic from UI


## Tooling
Free IDE Android Studio shipped with device emulator

# Flutter
https://flutter.io/
Flutter is Google’s mobile app SDK for crafting high-quality native interfaces on iOS and Android in record time. Flutter works with existing code, is used by developers and organizations around the world, and is free and open source.

Pros | Cons
------------ | -------------
Same codebase for Android and iOS | Small community
Contains iOs style and Android (Material) [widgets](https://flutter.io/widgets/) | Uses Dart
Easy transition to Dart from Java | New (not much examples running in production) <br> Flutter is still being developed and is not yet at 1.0
Good for prototyping | 

## What is inside the Flutter SDK?
 * Heavily optimized, mobile-first 2D rendering engine with excellent support for text
 * Modern react-style framework
 * Rich set of [widgets](https://flutter.io/widgets/) for Android and iOS
 * APIs for unit and integration tests
 * Interop and plugin APIs to connect to the system and 3rd-party SDKs
 * Headless test runner for running tests on Windows, Linux, and Mac
 * Command-line tools for creating, building, testing, and compiling your apps

*- From Flutter website*

## Tooling
Free IDE Android Studio shipped with device emulator
