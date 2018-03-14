[![Version](https://img.shields.io/cocoapods/v/nxus_ios_cocoapod.svg?style=flat)](http://cocoapods.org/pods/nxus_ios_cocoapod)
[![License](https://img.shields.io/cocoapods/l/nxus_ios_cocoapod.svg?style=flat)](http://cocoapods.org/pods/nxus_ios_cocoapod)
[![Platform](https://img.shields.io/cocoapods/p/nxus_ios_cocoapod.svg?style=flat)](http://cocoapods.org/pods/nxus_ios_cocoapod)

## Summary
TechMpire nxus platform SDK CocoaPods distribution for iOS developers

## Installation

mpire_nxus_measurement is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "mpire_nxus_measurement"
```

## SDK initialisation
After you completed the previous step, you are ready to initialise the library and start sending events.
Open <b>AppDelegate.m</b> class and import the library header file:
```
#import "include/MpireNxusMeasurement/MpireNxusMeasurement.h"
```

Then, initialise it within AppDelegate's <b>didFinishLaunchingWithOptions</b> method:
```
[MpireNxusMeasurement initializeLibrary:@"YOUR_API_KEY"];
```

## Sending custom events
You can send custom events by calling the method <b>trackEvent</b>:
```
[MpireNxusMeasurement trackEvent:@"event-name"];
```

If you have any additional parameters you would like to send, pass in an instance of <b>NSMutableDictionary</b>:
```
NSMutableDictionary *params = [[NSMutableDictionary alloc] init];
[params setValue:@"value" forKey:@"key"];
[MpireNxusMeasurement trackEvent:event params:params];
```

## Sending predefined events
You can send predefined events using the SDK, with following methods:
```
[MpireNxusMeasurement trackEventInstall:params];
[MpireNxusMeasurement trackEventOpen:params];
[MpireNxusMeasurement trackEventRegistration:params];
[MpireNxusMeasurement trackEventPurchase:params];
[MpireNxusMeasurement trackEventLevel:params];
[MpireNxusMeasurement trackEventTutorial:params];
[MpireNxusMeasurement trackEventAddToCart:params];
[MpireNxusMeasurement trackEventCheckout:params];
[MpireNxusMeasurement trackEventInvite:params];
[MpireNxusMeasurement trackEventAchievement:params];
```
Every method takes additional parameters using <b>NSMutableDictionary</b>:
```
NSMutableDictionary *params = [[NSMutableDictionary alloc] init];
[params setValue:@"value" forKey:@"key"];
```

## Logging
To enable logging, call the method debuggingEnabled before library initialisation:
```
[MpireNxusMeasurement debuggingEnabled:YES];
```

## Author

TechMpire ltd.

## License

mpire_nxus_measurement is available under the MIT license. See the LICENSE file for more info.
