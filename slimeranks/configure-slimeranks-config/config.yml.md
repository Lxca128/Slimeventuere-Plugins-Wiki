---
icon: file-code
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# config.yml

In the <mark style="color:green;">config.yml</mark>, which is located under `plugins/SlimeRanks/`, you have the option to make minor adjustments that are not directly related to ranks or messages. These settings are completely optional, and the default values are well-optimized to meet the average use case.

## 📃 Overview of all settings

| Config Key                | Default Value | Description                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ConfigVersion`           | `1`           | This is just for internal use and should not be changed!                                                                                                                                                                                                                                                                                                                                                                               |
| `UpdateChannel`           | `RELEASE`     | <p>The <code>UpdateChannel</code> defines which updates you are being notified about.</p><p>Available are the <code>RELEASE</code> channel for full plugin releases and stable versions. There is also a <code>BETA</code> channel, which includes all beta versions of SlimeRanks. Beta versions might contain bugs and changing features; therefore, this channel should only be used if you want to experiment with SlimeRanks.</p> |
| `NameUpdateInterval`      | `0`           | <p>This setting determines the interval (in seconds) for refreshing all player rank names.</p><p>Activate this setting only when using placeholders in your ranks.</p><p>If the value is 0, the names won't update automatically.</p>                                                                                                                                                                                                  |
| `NotifyForPluginUpdates`  | `true`        | This setting determines whether players with the `slimeranks.admin` permission should be notified about plugin updates upon join.                                                                                                                                                                                                                                                                                                      |
| `NotifyForVersionUpdates` | `true`        | This setting determines whether players with the `slimeranks.admin` permission should be notified about plugin updates for newer major Minecraft versions upon join.                                                                                                                                                                                                                                                                   |
