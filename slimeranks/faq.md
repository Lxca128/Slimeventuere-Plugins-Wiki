---
icon: question
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

# FAQ

Here you can find answers to frequently asked questions. So before you ask for support, it's worth taking a look here.

<details>

<summary>How do I give players a rank?</summary>

At first you need a plugin that manages permissions. I personally recommend [LuckPerms](https://luckperms.net/download) for doing that.

In the case you also use LuckPerms, you can use the following command to give a specific player a rank.

```
/lp user <PlayerName> permission set <Permission> true
```

{% hint style="info" %}
Replace \<PlayerName> with the name of the player, you want to give the rank to and \<Permission> with the permission you set in the ranks.yml.
{% endhint %}

After that, the player can rejoin, and the name of the player should be displayed in the right rank format.

</details>

<details>

<summary>Can I use the old color codes like <code>&#x26;a</code>?</summary>

No, SlimeRanks doesn't support the old color code format. And it's not planned to do in the future.

All messages and formats use the MiniMessage format. When you are unfamiliar with MiniMessage, I can recommend the [MiniMessage Viewer](https://webui.advntr.dev/).

</details>

***

## ⁉️ Didn't find an answer in the wiki?

If you still have any questions or need further assistance, feel free to open a new discussion in the [SlimeRanks GitHub repository](https://github.com/Lxca128/SlimeRanks/discussions); we’re always happy to help and hear your feedback!
