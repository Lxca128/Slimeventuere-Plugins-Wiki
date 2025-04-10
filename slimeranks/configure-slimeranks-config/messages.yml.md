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

# messages.yml

In the <mark style="color:green;">messages.yml</mark>, which is located under `plugins/SlimeRanks/`, you have the option to change the displayed messages. For example, you could change the language or just the colors.

## The message format

SlimeRanks uses the MiniMessage message format. With that you have the ability to use every possible color or even create gradients. That means messages look like `<green>SlimeRanks</green>` to get something like <mark style="color:green;">SlimeRanks</mark>.

For easier creation of messages in the MiniMessage format, I recommend using the MiniMessage Viewer, which allows you to simply create messages and preview them.

{% embed url="https://webui.advntr.dev/" %}

## The implementation of custom messages

After you successfully created your message, you have to replace the old one in the `messages.yml`.

To display the message now in-game, you need to either restart the server or use the `/slimeranks reload` command to reload the `messages.yml`.

***

{% hint style="info" %}
Currently SlimeRanks only has english messages, so if you want to display messages in a other language you have to manually translate them.

In the feature when SlimeRanks gets more popular there will be a transaltion system which will include multiple languages.
{% endhint %}
