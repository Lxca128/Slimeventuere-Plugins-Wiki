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

# ranks.yml

In the <mark style="color:green;">ranks.yml</mark>, which is located under `plugins/SlimeRanks/`, are the ranks of your server stored. So if you want to configure them manually, you're right here.

Now I will explain what the structure of this configuration is and what every key does.

## 💾 The default ranks.yml

{% code fullWidth="false" %}
```yaml
ConfigVersion: 1
Ranks:
  Admin:
    Tab:
      Active: true
      Format: <color:#e63946>Admin</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
      Priority: 2
    Chat:
      Active: true
      Format: <color:#e63946>Admin</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
        <dark_gray>»</dark_gray> <color:#ededed>{message}</color>
      ColoredMessages: true
    NameTag:
      Active: true
      Format: <color:#e63946>Admin</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
      HideOnSneak: false
    RankPriority: 1
    Permission: slimeranks.rank.admin
  Player:
    Tab:
      Active: true
      Format: <color:#b0b0b0>Player</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
      Priority: 1
    Chat:
      Active: true
      Format: <color:#b0b0b0>Player</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
        <dark_gray>»</dark_gray> <color:#ededed>{message}</color>
      ColoredMessages: false
    NameTag:
      Active: true
      Format: <color:#b0b0b0>Player</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
      HideOnSneak: false
    RankPriority: 0

```
{% endcode %}

## 📃 Every key explained

| Key                                       | Description                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ConfigVersion`                           | The value of this key is just for internal use. The value should NOT be changed manually!                                                                                                                                                                                                                                                                                             |
| `Ranks.<Identifier>.Tab.Active`           | <p>This indicator sets whether the player name should be displayed with the rank in the tablist.<br><br>To activate the feature, set the value to <code>true</code>, to deactivate the feature, use <code>false</code>.</p>                                                                                                                                                           |
| `Ranks.<Identifier>.Tab.Format`           | <p>This is the format that will be used to display players with that rank in the tablist.<br><br>To show the player's name, use the <code>{player}</code> placeholder.<br><br>The format should be written in the MiniMessage format. I recommend using the <a href="https://webui.advntr.dev/">MiniMessage Viewer</a>.</p>                                                           |
| `Ranks.<Identifier>.Tab.Priority`         | <p>This represents the weight for the tablist sorting. The higher the number, the higher players with the rank will be displayed in the tablist.<br><br>To deactivate the tablist sorting, simply set the value to <code>0</code>.</p>                                                                                                                                                |
| `Ranks.<Identifier>.Chat.Active`          | <p>This indicator determines if the messages of players with this rank should be displayed in the specified format.<br><br>To activate the feature, set the value to <code>true</code>, to deactivate the feature, use <code>false</code>.</p>                                                                                                                                        |
| `Ranks.<Identifier>.Chat.Format`          | <p>This is the format that will be used to display players with that rank in the chat.<br><br>To show the player's name, use the <code>{player}</code> placeholder.<br>To show the player's message, use <code>{message}</code>.<br><br>The format should be written in the MiniMessage format. I recommend using the <a href="https://webui.advntr.dev/">MiniMessage Viewer</a>.</p> |
| `Ranks.<Identifier>.Chat.ColoredMessages` | This indicator determines if players with this rank should be allowed to use the MiniMessage format in the chat to make their message prettier with colors and gradients.                                                                                                                                                                                                             |
| `Ranks.<Identifier>.NameTag.Active`       | <p>This indicator determines if the name tag of players with this rank should be displayed in the specified format.<br><br>To activate the feature, set the value to <code>true</code>, to deactivate the feature, use <code>false</code>.</p>                                                                                                                                        |
| `Ranks.<Identifier>.NameTag.Format`       | <p>This is the format that will be used to display the player's name tag.<br><br>To show the player's name, use the <code>{player}</code> placeholder.<br><br>The format should be written in the MiniMessage format. I recommend using the <a href="https://webui.advntr.dev/">MiniMessage Viewer</a>.</p>                                                                           |
| `Ranks.<Identifier>.NameTag.HideOnSneak`  | <p>This indicator determines if name tags of players with this rank should be completely hidden on sneaking.<br><br>To activate the feature, set the value to <code>true</code>, to deactivate the feature, use <code>false</code>.</p>                                                                                                                                               |
| `Rank.<Identifier>.RankPriority`          | This represents the weight of the rank. When players have multiple ranks, the rank with the highest value will be applied.                                                                                                                                                                                                                                                            |
| `Rank.<Identifier>.Permission`            | <p>This represents the permission that you have to give players that they obtain this rank.<br><br>This key is completely optional. If you want every player to have this rank by default, just remove the entire line.</p>                                                                                                                                                           |

## ⚒️ How to create a rank

If you want to create a rank manually, you have to copy the following snippet, which you have to insert into the <mark style="color:green;">ranks.yml</mark> at the end of the file.

{% hint style="warning" %}
Make sure that you keep and match to the indentation of the existing ranks.
{% endhint %}

```yaml
  Admin:
    Tab:
      Active: true
      Format: <color:#e63946>Admin</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
      Priority: 2
    Chat:
      Active: true
      Format: <color:#e63946>Admin</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
        <dark_gray>»</dark_gray> <color:#ededed>{message}</color>
      ColoredMessages: true
    NameTag:
      Active: true
      Format: <color:#e63946>Admin</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
      HideOnSneak: false
    RankPriority: 1
    Permission: slimeranks.rank.admin
```

After you insert the snippet, you can configure the values. To do that, please read the instructions for every key above.

After finishing the configuration, you can run the `/slimeranks reload` command on the server. Now the ranks should be loaded and can be applied to players.

***

## ❓ FAQ

<details>

<summary>How to give a player a rank?</summary>

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
