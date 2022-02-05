---
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# React Native

## Installation

### What you'll need

- [React Native](https://reactnative.dev/) version 60 or above:
- iOS 10+

<Tabs
defaultValue="npm"
values={[
{label: 'NPM', value: 'npm'},
{label: 'Yarn', value: 'yarn'},
]}>

<TabItem value="npm">

```
  npm i @airsnap/react-native
```

</TabItem>

<TabItem value="yarn">

```
 yarn add @airsnap/react-native
```

</TabItem>

</Tabs>

<Tabs
defaultValue="ios"
values={[
{label: 'iOS', value: 'ios'},
{label: 'Android', value: 'android'},
]}>

<TabItem value="ios">

Install the Pod library:

```
 pod install
```

</TabItem>

<TabItem value="android">

Unfortunately we do not support Android at the moment. 😢

Please contact us if you'd like to see support here.

</TabItem>

</Tabs>

## Initialize the library

After getting the API key, initialize AirSnap.

```js
import AirSnap from '@airsnap/react-native';

AirSnap.start('<api-key>');
```
