# AlarmWatcher

AlarmWatcher is a versatile, self-hosted and intuitive to use alarm management system. It is designed to serve as the central hub for handling alarms across various applications and systems. Whether you're managing alarms for smart home, industrial equipment, or other interconnected devices, AlarmWatcher simplifies alarm handling.

<a target="_blank" href="https://github.com/johnny-de/alarmwatcher"><img src="https://img.shields.io/github/stars/johnny-de/alarmwatcher?style=flat" /></a> 
<a target="_blank" href="https://github.com/johnny-de/alarmwatcher"><img src="https://img.shields.io/github/v/release/johnny-de/alarmwatcher" /></a> 
<a target="_blank" href="https://github.com/johnny-de/alarmwatcher"><img src="https://img.shields.io/github/last-commit/johnny-de/alarmwatcher" /></a>
<a target="_blank" href="https://hub.docker.com/r/johnny-de/alarmwatcher"><img src="https://img.shields.io/docker/pulls/johnny-de/alarmwatcher" /></a> 
<a target="_blank" href="https://hub.docker.com/r/johnny-de/alarmwatcher"><img src="https://img.shields.io/docker/v/johnny-de/alarmwatcher/latest?label=docker%20image%20ver" /></a>

## Key Features

- **Centralized Alarm Management:** Aggregate and manage alarms from multiple systems in one place.
- **Customizable Alarm Handling:** Define alarm priorities, require acknowledgment, and configure auto-deletion.
- **Built-In Expiration Mechanism:** Automatically remove alarms after a set duration to avoid clutter.
- **Simple, Yet Powerful API:** Easily integrate with any system through a flexible and straightforward http-API.
- **Web-based Frontend:** View and manage alarms through an intuitive web interface, allowing for custom filters.

### Alarm Handling

AlarmWatcher is built around an mechanism where every alarm is identified by a unique ID. Once an alarm is raised, it remains active in the system until one of two conditions is met:

1. The alarm is **cleared**.
2. The defined **duration** for that specific alarm expires.

Each alarm must belong to one of the predefined alarm classes, which determine its priority and how it is displayed in the system:

1. **Alarm (Highest Priority - Red):** Critical issues requiring immediate attention.
2. **Warning (Medium Priority - Orange):** Important issues that are not yet critical, but may soon become critical if not addressed.
3. **Event (Lowest Priority - Gray):** Informational messages or routine events that require no action.

Alarms are handled entirely by the server. Users can view and manage alarms via a web-based frontend, which supports advanced filtering to make it easy to find and respond to specific alarms.

### Acknowledgment Mechanism

AlarmWatcher also includes an acknowledgment mechanism to ensure critical alarms are not overlooked. When an alarm is raised, it can be marked as requiring acknowledgment. This ensures that even if the alarm is cleared or its defined duration expires, the alarm will remain visible in the system until a user acknowledges it.
This feature is especially useful for high-priority alarms, ensuring that critical incidents receive the necessary attention and are not missed by automation or system rules.

## Getting Started

To learn how to install, configure, and run AlarmWatcher, please visit the detailed guide in our [Wiki](https://github.com/johnny-de/alarmwatcher/wiki).

## Milestones

Below is an outline of the planned milestones for version 1.0.0 and beyond.

### Version 1.0.0

The first major release (v1.0.0) will focus on delivering a fully functioning backend and a user-friendly frontend, along with essential features for alarm management.
- **Backend:** Complete and thoroughly test the backend for alarm management, handling alarm states, acknowledgments, and filtering. Ensure stability and reliability for all server-side operations.
- **Frontend:** Implement a fully functional, web-based frontend for monitoring and managing alarms. Integrate notification support, allowing browsers to push notifications into the underlying OS notification systems.
- **Docker Image:** Create and publish a Docker image on DockerHub to simplify deployment and installation.
- **Wiki Documentation:** Prepare and publish a detailed Wiki to guide users on how to install, configure, and use AlarmWatcher.

### Version 1.1.0

The second major release (v1.1.0) will enhance AlarmWatcher with additional features and interfaces.
- **HTTPS Support:** Add support for secure connections using HTTPS.
- **Email Interface:** Introduce an interface for receiving alarms via email (SMTP). Idea is to provide predefined addresses (e.g. uptime-kuma@alarmwatcher) and also allowed users to create custom email-interfaces to raise or clear alarms based on specific keywords in incoming emails.

### Version 1.2.0

The third major release (v1.2.0) will focus on building a comprehensive alarm history system, improving database performance, and optimizing filtering.
- **Alarm Archiving:** Introduce an alarm archiving feature, allowing alarms to be stored beyond their active state, creating a history of all alarms.
- **Database Optimization:** Optimize the database structure to handle larger datasets efficiently.
- **Advanced Filtering:** Improve the filtering capabilities of the frontend, enabling more advanced search options and filtering based on alarm history.

### Future Milestones

Beyond the core milestones for AlarmWatcher, additional features and extensions are planned to broaden the system's reach and usability.
- **Open-Source Android App:** Develop and release an open-source Android app that allows users to view alarms and receive push notifications on their mobile devices.
- **Public Demo:** Set up a public, free-to-use demo instance of AlarmWatcher, allowing users to test its features with the following limitation: alarms will be saved for a maximum of 100 days.
- **Node-RED Integration:** Create AlarmWatcher nodes for Node-RED.

## Bug Reports / Feature Requests

If you want to report a bug or request a new feature, feel free to open a [new issue](https://github.com/johnny-de/alarmwatcher/issues).
