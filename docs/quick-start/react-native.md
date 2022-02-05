---
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# React Native

## Installation

After getting the API key, follow the steps below to install your package from here.

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

Install the Pod library:

```
 pod install
```

## Initialize the library

```js
import AirSnap from '@airsnap/react-native'

AirSnap.start('<api-key>')
```
