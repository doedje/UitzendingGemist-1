# ![Apple TV](http://images.apple.com/v/tv/c/images/shared/buy_tv_logo_resized_large.png) Uitzending Gemist 

```UitzendingGemist``` is an unofficial native application for the Apple TV developed in [Swift](https://developer.apple.com/swift/). It will allow you to browse and watch all video streams of the Nederlandse Publieke Omroep's (e.g. NPO, the Dutch public broadcaster) [Uitzending Gemist](http://www.npo.nl/uitzending-gemist) website on your Apple TV.

![Uitgelicht](/Tips.png)

Watching videos is very snappy and almost instantaneous, contrary to streaming from your iDevice to Apple TV over Airplay or using the built-in player in your smart tv.

# Okay, that's great! But how do I get this on my ![Apple TV](http://images.apple.com/v/tv/c/images/shared/buy_tv_logo_resized_large.png)?

Unfortunately the app cannot be distributed in the Appstore as the NPO does not allow third parties in doing so. However, using a free Apple Developer account you *can* compile it yourself and install it in your own Apple TV 4. 

**Prerequisites:**

- an [Apple TV](http://www.apple.com/tv/) 4th generation (the one that has an AppStore)
- a recent Apple Computer running ```OS X 10.10.x Yosemite``` or ```OS X 10.11.x El Capitan```
- a (free) Apple Developer account (signup [here](http://developer.apple.com))
- a USB-C cable to connect your Apple TV to your Apple Computer

## 1. Xcode

The code was developed in [Xcode 7.1.1](https://developer.apple.com/xcode/download/) so you need to have it installed. Continue with the following steps when you have finished installing ```Xcode```.

## 2. Homebrew

[Homebrew](http://brew.sh) is the missing package manager for OS X, which can be used to install all sorts of open source projects. To install, execute the following from ```Terminal```:

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## 3. Carthage

The code relies on a number of dependencies that are managed by the [Carthage](https://github.com/Carthage/Carthage) dependency manager. Before working with the code you first need to [install Carthage](https://github.com/Carthage/Carthage#installing-carthage). In short, execute the following command in ```Terminal```:

```
brew install carthage
```

## 4. Clone the project

It is advisable to have a ```Developer``` folder on your machine. Execute the following code in ```Terminal``` to create those folders and clone this project:

```
mkdir -p ~/Developer/tvOS
cd ~/Developer/tvOS
git clone https://github.com/4np/UitzendingGemist.git
cd UitzendingGemist
```

## 5. Fetching and compiling dependencies

Now that you have ```Xcode``` and ```Carthage``` on your system, you can fetch and compile the depencies. Execute the following command in ```Terminal``` from within your project folder to fetch and compile the dependencies.

```
cd ~/Developer/tvOS/UitzendingGemist
carthage bootstrap
```

## 6. Open the project

Now that everything is in place, you can open the project file ```UitzendingGemist.xcodeproj``` in ```Finder```. Alternatively, when you still have ```Terminal``` open you can also execute the following command:

```
open UitzendingGemist.xcodeproj
```

## 7. Connect the Apple TV 4 to your computer

Connect the ```Apple TV 4``` using the USB-C cable to your Mac. 


## 8. Set the bundle identifier

See the screenshot below and click on **1** and **2** to get to the screen shown below. Set the bundle identifier (**3**) to some name. This should be something in reverse domain format, for example ```com.JohnAppleseed.UitzendingGemist```.

![Steps](/Steps.png)

## 9. Select the team

In order to deploy the application to the Apple TV it needs to be signed with your team (see **4** in the screenshot above). If you do not have a team (e.g. ```None```), or you see the message ```No Matching provisioning profiles found``` click the ```Fix Issue``` and login with your Apple ID / Apple Developer Account credentials.

## 10. Select the Build Device

On the top left in Xcode click on the device the compiled program will be deployed to (see **5** in the screnshot above). If your Apple TV 4 is properly connected you will be able to pick you Apple TV device (otherwise it will run in the Simulator).

## 11. Run the application

Finally you are able to compile the program and deploy it onto your Apple TV! Click the play icon (see **6** in the screenshot above). The application will be compiled and deployed on your Apple TV 4. After this the application will remain on the Apple TV. 

## 12. Sit back and enjoy :)

You're done! You can disconnect your Apple TV and start watching! :)

# More screenshots

## Highlighted, popular and recently broadcasted programs

![Uitgelicht](/Tips.png)

## All broadcasted programs, by date for the past seven days

![Per Dag](/Daily.png)

## All shows

![Programma's](/Programs.png)

## All episodes for a show

![Series](/Series.png)

## One episode for a show

![Episode](/Episode.png)

## Watching an episode

![Player](/Player.png)

# License

See the accompanying [LICENSE](LICENSE) and [NOTICE](NOTICE) files for more information.

```
Copyright 2015 Jeroen Wesbeek

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

