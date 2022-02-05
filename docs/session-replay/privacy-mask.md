---
sidebar_position: 1
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Privacy Mask

AirSnap prioritizes privacy and therefore enables privacy masking by default. The masking will automatically be applied to the session replay, network requests and events.

import PrivacyImageUrl from '@site/static/img/privacy-mask.png';

# <img src={PrivacyImageUrl} />

:::info

AirSnap's session replay is based on drawing operations, where text, images, and personal data are
masked at the source by default, such that masked data never leaves a user's device.

:::

You can disable the privacy mask by passing the following parameter to `AirSnap.start`

<Tabs
defaultValue="reactNative"
values={[
{label: 'React Native', value: 'reactNative'},
{label: 'iOS', value: 'ios'},
]}>

<TabItem value="reactNative">

```jsx title="React Native"
AirSnap.start('<api-key>', 'unmask'); // "mask" or "unmask"
```

</TabItem>

<TabItem value="ios">

```jsx title="iOS"
AirSnap.start(withAppKey: "<api-key>", privacyRule: .unmask)
```

</TabItem>

</Tabs>
