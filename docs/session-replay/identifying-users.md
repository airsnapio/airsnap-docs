---
sidebar_position: 5
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Identifying Users

AirSnap allows you to identify the user by getting setting a custom ID. In addition, you're also able to retrieve the `sessionId` and `userId` via our SDK.

<Tabs
defaultValue="reactNative"
values={[
{label: 'React Native', value: 'reactNative'},
{label: 'iOS', value: 'ios'},
]}>

<TabItem value="reactNative">

<h2>getSessionId</h2>

Returns the current session ID

```jsx
const sessionId = await AirSnap.getSessionId();
```

<h2>getUserId</h2>

Returns the user ID that is used to distinguish users. This can be a custom identifier that you set, otherwise it will use the [IDFV Device ID](https://app.airsnap.io/) by default.

```jsx
const userId = await AirSnap.getUserId();
```

<h2>setUserId</h2>

Sets the user ID that is used to distinguish users. This can be the internal identifier for your application. If param is an empty string or `null`, it will reset the identifier back to the Device ID.

```jsx
AirSnap.setUserId('john.doe@airsnap.io');

// Resets user id to device id. Ex: logging out
AirSnap.setUserId('');
AirSnap.setUserId();
```

</TabItem>

<TabItem value="ios">

```jsx title="iOS"
AirSnap.start(withAppKey: "<api-key>", privacyRule: .unmask)
```

</TabItem>

<TabItem value="ios">

<h2>getSessionId</h2>

Returns the current session ID

```jsx
AirSnap.sessionId: string
```

<h2>getUserId</h2>

Returns the user ID that is used to distinguish users. This can be a custom identifier that you set, otherwise it will use the [IDFV Device ID](https://app.airsnap.io/) by default.

```jsx
AirSnap.userId: string
```

<h2>setUserId</h2>

Sets the user ID that is used to distinguish users. This can be the internal identifier for your application. If param is an empty string or `null`, it will reset the identifier back to the Device ID.

```jsx
AirSnap.userId: string
```

</TabItem>

</Tabs>
