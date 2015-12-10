# Persisting Messages

## Overview
ESB Message Admin (EMA) provides a REST interface for persisting messages, along with associated
metadata such as origin information, JMS headers, and error messages.
The [EsbMessage class]("https://raw.githubusercontent.com/esbtools/esb-message-admin/master/api/src/main/java/org/esbtools/message/admin/model/EsbMessage.java")
for all the fields that can be supplied when persisting an error message.

## Persist Sequence
This sequence diagram outlines the steps involved in persisting a message in EMA.  In addition to persisting the
information provided in the request, EMA also attempts to extract searchable data from the message that have been
previously configured in the application.  See the [Search Keys](search-keys/README.md) section of the documentation for more information
 on configuring search keys.
![Persist Sequence](/images/ema-sequence-persist.png)

## Sample Persist Request
The JSON below provides a sample message persisting an error message into ESB Message Admin.

```
  {
    "errorQueue": "GITHUB_ORG_ERROR",
    "messageId": "JMS8675309",
    "timestamp": "2015-08-12T12:00:00",
    "messageGuid": "8675309",
    "messageType": "ORDER",
    "sourceQueue": "GITHUB_ORG_CREATE",
    "sourceLocation": "Internet",
    "sourceSystem": "GitHub",
    "originalSystem": "GitHub",
    "serviceName": "GitHub",
    "errorComponent": "GitHubOrgCreate",
    "errorMessage": "That organization already exsits",
    "errorDetails": "There was a problem creating your GitHub organization",
    "errorSystem": "GitHub",
    "errorType": "DATA_ERROR",
    "occurrenceCount": "1",

    "payload": "<?xml version=\"1.0\" encoding=\"UTF-8\"?><GitHubOrganization><OrganizationName>esbtools</OrganizationName><BillingEmail>admin@esbtools.org</BillingEmail><OrganizationsPlan>Open Source</OrganizationsPlan><Visibility>Public</Visibility></GitHubOrganization>",
    "headers": [
      {
        "name": "SERVER_ID",
        "value": "1"
      }
    ]
  }
```