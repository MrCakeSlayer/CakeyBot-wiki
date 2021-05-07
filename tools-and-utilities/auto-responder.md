# Auto Responder

### Overview

This feature allows you to set up custom responses that Cakey Bot can handle. For example, you can make Cakey Bot respond to messages such as `wot` with a link to a funny gif. You can also set some flags to determine what types of messages Cakey Bot will respond to.

### Setup

{% hint style="warning" %}
You will need **`Manage Server`** or **`Administrator`** permission to manage guilds and custom commands.
{% endhint %}

1. Login to the web dashboard on the [main website here](https://cakeybot.app/dashboard/public).
2. Click on the guild you want to edit custom commands on.
3. Go to the "Auto Responder" page.
4. You can then create, delete, and edit any responses on this page. You can get an overview of any flags that are available below. 

### Flags

* Exact Match
  * Default behavior, looks for exact match strings
* Contains
  * Will search the entire message to see if it contains this string/trigger
* Starts With
  * Will check to see if the message begins with this string/trigger
* Ends With
  * Will check to see if the message ends with this string/trigger
* Contains Files
  * Will check to see if the message contains any files/attachments. \(i.e. documents, images, videos\)
  * **Note:** When using this flag, the "Command" field is still required. However, it is not used to actually trigger the auto response. It's purely a cosmetic property.

### Limitations/Restrictions

Cakey Bot will ignore any messages that are sent by other bots or sent via webhooks. This is to prevent spam loops or command loops between both bots.

### Using Emoji/Emotes in Responses

Emoji/Emotes CAN be used in Custom Commands. However, it requires slightly more work due to how discord parses emotes. Normally in Discord, you could just type `:lel:` or `:smile:` to get an emote, however in Cakey Bot, neither of these will work. In order to get valid emojis you have to send the emojis in discord but place a backward slash in front of it to get the emote's full ID. Like so: `\:lel:` or `\:smile:` which will produce these results: `<:lel:408424717217693717>` or for Unicode emoji: `😄` . Once you have the full emoji id or the raw Unicode output, you can paste these into Cakey Bot's web dashboard and they should work as long as Cakey Bot is in a guild that has that custom emote in it. 

{% hint style="info" %}
It is worth noting that Cakey Bot can use emojis in between guilds \(similar to nitro users\). So if you have an emoji in Guild \#1, you can use that emoji in a custom command in Guild \#2 if Cakey bot is in both of those guilds.
{% endhint %}

### Using Images in Responses

To use images in responses, you can simply just type the image URL/link like you would in a normal message. If you have the file on your local machine/PC but no URL/link, you can upload it to an image hosting website \(such as [Imgur](https://imgur.com/upload)\) and paste the URL they provide into the response.

### Placeholders/Variables

Auto Responder will work with BOTH **Basic Placeholders** & **Advanced Placeholders**. Placeholders can be included in the response section and can modify the behavior/output of the response. You can find the list of supported placeholders [here](../setup/placeholders-variables.md). 

{% hint style="warning" %}
Auto Responder will **NOT** work with the **Advanced Placeholders**.
{% endhint %}
