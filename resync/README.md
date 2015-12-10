# Resync Messages

## Overview
ESB Message Admin (EMA) provides capabilities for triggering sync messages (i.e. the current state of an integrated entity)
from end systems using configured key fields.  See ![Sync Keys](/sync-keys/README.md) for more information on managing
sync keys.


## Resync Sequence
This sequence diagram outlines the steps involved in resyncing a message from EMA.

![Persist Sequence](/images/ema-sequence-resync.png)

## Resync Example
The screenshot below shows how a message can be resynced via the EMA web application.

![Resync Screenshot](/images/ema-screenshot-sync.png)