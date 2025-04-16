---
description: >-
  Here you will learn how to use the SlimeRanks GUI and configure/modify ranks
  with the GUI.
icon: display
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

# Configure SlimeRanks (GUI)

## 🖼️ The GUI

These are the two GUI pages used to provide an overview of all existing ranks and the page where you can configure a rank in detail. By default, there are two pre-configured ranks that are already listed here.

<div><figure><img src="../.gitbook/assets/Rank Overview GUI.png" alt=""><figcaption><p>Rank overview GUI example</p></figcaption></figure> <figure><img src="../.gitbook/assets/Edit Rank GUI.png" alt=""><figcaption><p>Rank edit GUI example</p></figcaption></figure></div>

## 🆕 How to create a new rank

Creating a new rank is quite simple. Just follow these steps, and you'll have your own rank set up in a couple of seconds.

{% stepper %}
{% step %}
### Open the GUI

First, you need to open the GUI to manage the ranks. Simply type `/slimeranks gui` into the chat.\
Please note that you need the `slimeranks.admin` permission or `OP` for this
{% endstep %}

{% step %}
### Start the process

To start the rank creation process, click on the crafting table at the bottom right.\
Afterwards, the GUI will close.
{% endstep %}

{% step %}
### Input the rank identifier

You will now be prompted to enter a rank identifier in the chat. Normally, the rank identifier is the name of the rank without any formatting. Please note that only letters are allowed.
{% endstep %}

{% step %}
### Configure the rank

The rank is now created; you can customize it as you wish.\
In the next section, you'll learn how and what you can
{% endstep %}
{% endstepper %}

## 🖊️ Customize a rank

Now you want to configure your ranks to match your server theme.\
This section explains what each item does and how you can configure it.

To configure a rank, you must first open the GUI if it doesn't open automatically after creating a rank.\
You can open it with `/slimeranks gui`. In the open GUI, select the rank you want to configure.

<details>

<summary>Tablist format <sub>(JUNGLE_SIGN)</sub></summary>

The <mark style="color:green;">Tablist format</mark> defines how the rank should be displayed in the tablist.

The default format for the player rank is

```
<color:#b0b0b0>Player</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
```

When clicking on the item, you can enter your desired format into the chat.

To display the player name, you can simply use `{player}`, which will be replaced with the player's name who has the rank.

{% hint style="info" %}
You can use the [MiniMessage Viewer](https://webui.advntr.dev/) to create tablist formats easily.
{% endhint %}

</details>

<details>

<summary>Chat format <sub>(WRITABLE_BOOK)</sub></summary>

The <mark style="color:green;">Chat format</mark> determines how the rank is displayed in the chat.

The default format for the player rank is

```
<color:#b0b0b0>Player</color> <dark_gray>|</dark_gray> <gray>{player}</gray> <dark_gray>»</dark_gray> <color:#ededed>{message}</color>
```

When clicking on the item, you can enter your desired format into the chat.

To display the player name, you can simply use `{player}`, which will be replaced with the player's name who has the rank.\
To display the message the player wants to send, use⁣ `{message}`.

{% hint style="info" %}
You can use the [MiniMessage Viewer](https://webui.advntr.dev/) to create tablist formats easily.
{% endhint %}

</details>

<details>

<summary>Name tag format <sub>(NAME_TAG)</sub></summary>

The <mark style="color:green;">Name tag format</mark> defines how the rank should be displayed above the player.

The default format for the player rank is

```
<color:#b0b0b0>Player</color> <dark_gray>|</dark_gray> <gray>{player}</gray>
```

When clicking on the item, you can enter your desired format into the chat.

To display the player name, you can simply use `{player}`, which will be replaced with the player's name who has the rank.

{% hint style="info" %}
You can use the [MiniMessage Viewer](https://webui.advntr.dev/) to create tablist formats easily.
{% endhint %}

</details>

<details>

<summary>Rank priority <sub>(ANVIL)</sub></summary>

The <mark style="color:green;">Rank priority</mark> is used to manage which rank a player should have when there are multiple options.\
A player will use the rank with the highest priority available to him.

To change the rank priority simply click on the item and enter the desired rank priority as a number in the chat.

</details>

<details>

<summary>Permission <sub>(FLOWER_BANNNER_PATTERN)</sub></summary>

The <mark style="color:green;">Permission</mark> determines which permission a player must have to obtain the rank.

By default, a rank will get a permission in the following format: `slimeranks.rank.<rank_identifier>`.\
When creating a new rank, ensure the right players get this permission to display the rank correctly.

If you want every player to get this rank by default, you can remove the permission by using shift-click on the item.\
To change the permission, simply click the item and enter the desired permission into the chat.

</details>

<details>

<summary>Tab priority <sub>(NETHERITE_UPGRADE_SMITHING_TEMPLATE)</sub></summary>

The <mark style="color:green;">Tab priority</mark> determines how the rank is sorted in the tab list.\
A higher number places the rank higher on the list.\
If the value is 0, no sorting is performed.

To change the tab priority, simply click the item and enter the desired priority number in the chat.

</details>

<details>

<summary>Hide name tag on sneak <sub>(ENDER_EYE)</sub></summary>

The <mark style="color:green;">Hide name tag on sneak</mark> setting determines whether the player's name tag should be hidden when the player sneaks, or only not be visible through walls.

By default, this setting is deactivated to match the vanilla sneaking behavior.

To enable the feature, click the dye below the item.

</details>

<details>

<summary>Colored Chat Messages <sub>(GLOW_INC_SAC)</sub></summary>

The <mark style="color:green;">Colored Chat Messages</mark> setting determines whether a player with this rank is allowed to use color codes to customize their chat messages.

The color code format would look something like `<green>hey`. To generate messages with color codes, we recommend using the [MiniMessage Viewer](https://webui.advntr.dev/).

To enable or disable the feature, click the button below this item.

</details>
