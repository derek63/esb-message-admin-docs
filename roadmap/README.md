# ESB Message Admin Roadmap

## Overview
The initial focus of the ESB Message Admin application was error management, and most of the documented use cases and
application functionality at this stage is concerned with managing messages in error.  There are a number of other ESB
administration capabilities we want to include in the tool as time progresses, which are described below in priority rank.

## 0 - Error Management
* Persist Errors
* Search/View Errors
* Resubmit Error Messages
* Resync Message From Originating System
* Search/Sync Key Management

## 1 - Basic Message Tracking
* Message Status Updates
    * Delivered to ESB
    * Picked Up by ESB
    * Processed by ESB
    * Delivered to End System(s)
* Message Error Reporting
    * Link to Error Management App to take action on error
    * Error Count Summaries By End System
* Message Data Persistence
    * Store/View Message Payloads
    * Uniform, short retention period

## 2 - Health Dashboard
* Real-Time ESB Metrics Visualizations
* Historical Trend Visualization

## 3 - Configuration Management
* Outage Management (Start/Stop)
* Feature Flag Control (Enable/Disable)
* Route Management (Enable/Disable)
* Display Deployed Component Versions

## 4 - Reporting
* Identify Most Common Errors ( by Entity )
* Identify Most Updated Parties / etc.

## 5 - Enhanced Message Tracking
* Additional Message Status Updates
    * Event Published
    * Message Created
    * Picked Up By End System
    * Processed By End System
* Message Management
    * Advanced Query Capabilities (full-text search)
    * Saved Searches
    * Reflow Messages (prepare, show, execute, update)
    * Configure Retention Period (By Entity, End System, Content)
* Configuration Management
    * End System-Specific Configurations (Message Size, Messages Per Cycle, etc.)
