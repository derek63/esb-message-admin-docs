# Resubmit Messages

## Overview
ESB Message Admin (EMA) provides capabilities for resubmitting messages back to the ESB that may have previously resulted
in error or need to reprocessed for some other reason.


## Resubmit Sequence
This sequence diagram outlines the steps involved in resubmitting a message from EMA.  In addition to resubmitting the
information provided in the request, EMA also attempts to re-insert any sensitive information previously extracted and
encrypted during the persist phase to the message before submitting it to the ESB.  See the [Persist](persist/README.md)
section for more information about the extraction and encryption of sensitive information.

![Persist Sequence](/images/ema-sequence-resubmit.png)

## Resubmit Example
The screenshot below shows how a message can be resubmitted via the EMA web application.

![Resubmit Screenshot](/images/ema-screenshot-resubmit.png)