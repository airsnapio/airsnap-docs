---
sidebar_position: 1
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

import SessionReplay from '@airsnap/session-replay';

# Overview

AirSnap Session Replay is not a video recording.

It works by serializing the view hierarchy of the application, then rendering it on the browser for playback. This allows us to compress the data and perform additional optimizations that isn't possible on a traditional video recording. As a result, **AirSnap recordings are incredibly small!**

Our demo below comes in at **546KB for 53 seconds** of content.

# Demo

<div style={{ height: 700 }}>
<SessionReplay.ReplayProvider url="/session/session-demo.asnp" fps={5}>
<SessionReplay.Replayer />
</SessionReplay.ReplayProvider>
</div>
