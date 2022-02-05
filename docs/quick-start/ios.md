---
sidebar_position: 3
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# iOS

## Installation

<Tabs
defaultValue="cocoaPods"
values={[
{label: 'CocoaPods', value: 'cocoaPods'},
{label: 'Swift Package Manager', value: 'swiftPackageManager'},
{label: 'Carthage', value: 'carthage'},
]}>
<TabItem value="cocoaPods">

Add to your `Podfile`

```
  pod 'AirSnap'
```

Then run

```
  $ pod install
```

</TabItem>

<TabItem value="swiftPackageManager">

Add to your `Package.swift`

```swift
import PackageDescription

let package = Package(
    dependencies: [
        .Package(url: "https://github.com/airsnapio/airsnap-ios")
    ]
)
```

</TabItem>

<TabItem value="carthage">

Unfortunately we do not support Carthage at the moment. 😢

Please [create an issue](https://github.com/airsnapio/airsnap-ios/issues/new) if you'd like to see support here.

</TabItem>
</Tabs>

## Usage

<Tabs
defaultValue="swift"
values={[
{label: 'Swift', value: 'swift'},
{label: 'Objective-C', value: 'objectiveC'},
]}>

<TabItem value="swift">

```jsx title="AppDelegate.swift"
import AirSnapSDK

func application(...) -> Bool {
    ...

    AirSnap.start(withAppKey: "<api-key>", privacyRule: .mask) // .mask or .unmask
    AirSnap.setUser(id: "user@example.com")
}
```

</TabItem>

<TabItem value="objectiveC">

```jsx title="AppDelegate.m"

#import <AirSnapSDK/AirSnapSDK-Swift.h>

- (BOOL)application:... {
    ...

    [AirSnap startWithAppKey:@"<api-key>" privacyRule:PrivacyRuleUnmask]; // PrivacyRuleUnmask or PrivacyRuleMask
    [AirSnap setUserWithId:@"user@example.com"]
}
```

</TabItem>

</Tabs>
