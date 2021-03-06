# OLX Tracker

## Building And Running The Project (Requirements)
* Swift 5.0+
* Xcode 11.1+
* iOS 11.0+

### General Application Frameworks
SwiftLint: [Linting tool](https://github.com/realm/SwiftLint)

# Getting Started
If this is your first time encountering swift/ios development, please follow [the instructions](https://developer.apple.com/support/xcode/) to setup Xcode and Swift on your Mac. And to setup cocoapods for dependency management, make use of [CocoaPods](https://guides.cocoapods.org/using/getting-started.html#getting-started)
-checkout Master branch to run latest version
## Setup Configs
* Open the project by double clicking the `OLXTrack.xcworkspace` file
```
// App Settings
APP_NAME = OLX Tracker (Dev)
PRODUCT_BUNDLE_IDENTIFIER = com.abuzeid.OLXTrack.dev

#targets:
* OLXTrack
* OLXTrackTests
* OLXTrackUITests

```


# In your terminal, go to the project root directory. Make sure you have cocoapods setup, then run:
pod install

# Build and or run application by doing:
* Select the build scheme which can be found right after the stop button on the top left of the IDE
* [Command(cmd)] + B - Build app
* [Command(cmd)] + R - Run app

## Architecture
This application uses the Model-View-ViewModel (refered to as MVVM) architecture. The main purpose of the MVVM is to move the data state from the View to the ViewModel.

### Model
In the MVVM design pattern, Model is the same as in MVC pattern. It represents simple data.

### View
View is represented by the UIView or UIViewController objects, accompanied with their .xib and .storyboard files, which should only display prepared data. 

### ViewModel
Only a simple, formatted string that comes from the ViewModel.

ViewModel hides all asynchronous networking code, data preparation code for visual presentation, and code listening for Model changes. All of these are hidden behind a well-defined API modeled to fit this particular View.

One of the benefits of using MVVM is testing.

## Structure

### Extensions
This is to group every component's extension / reusable functions / wrappers of external framworks


### Modules
- include seperate modules, Networking, caching...etc.

### Scenes
This is for group of app scenes: categories view, items view and details view


## Add New Feature
 * you could  add new feature by folling OneFlow Model  (https://www.endoflineblog.com/oneflow-a-git-branching-model-and-workflow)
 * to start new featre, checkout from master, your branch should be under feature group
 
 ## Improvements

 * add staging environment
 * cach the images 
 * reach 100% code coverage
