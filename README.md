# Kurdish-mod-Modlog-docs2
Hey there! You want to make modlogs for your bot? Well Perfect place, Today i'll give you an example of my bots modlog And all of the current modlogs i know about! 





Alright lets get started!
You will have to know a bit of js to do this!
So here is the example i'll give (which you can use as a to get you started and to make all of the events!)
First of all, Make a category called "events" 
After you have done  make a channel called "messageDelete.js"
Paste this in


channel called "messageDelete.js"

--------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------
```const Discord = require("discord.js");

    const logChannel = message.guild.channels.cache.find(c => c.name === "modlog");

    if (!logChannel) return;

    let chunked;
    if (message.content.length > 1024) {
        chunked = message.content.substring(0, message.content.length - 1024) + "...";
    } else {
        chunked = message.content;
    }

    let embed = new Discord.MessageEmbed()
        .setAuthor(message.author.tag, message.author.displayAvatarURL({ dynamic: true }))
        .setFooter(`User ID: ${message.author.id} | Message ID: ${message.id}`)
        .setTimestamp()
        .setDescription([
            `**Message sent by** <@!${message.author.id}> **deleted in** <#${message.channel.id}>`,
            chunked
        ].join("\n"))

    logChannel.send(embed); 
}```

--------------------------------------------------------------------------------------------------------------
You will need to know js to use it
Just add 1 line of code.
Anyways
After you have done that!
Try to understand how it works
If you failed dm me Aian#9999 And i might be able to help
----------------------------------------------------
Anyways
These all are of the events **I KNOW ABOUT**
messageDeleteBulk.js

messageUpdate.js

guildMemberUpdate.js

guildMemberAdd.js

voiceChannelJoin.js

voiceChannelLeave.js

guildMemberSpeaking.js

emojiCreate.js

emojiUpdate.js

emojiDelete.js

guildBanAdd.js

guildBanRemove.js

guildMemberRemove.js

guildMembersChunk.js

channelCreate.js

channelDelete.js

messageReactionAdd.js

messageReactionRemove.js

roleCreate.js

roleDelete.js
------------------------------------------------------------------------------------------------
Alright so these are all of the current ones i know off, If you know more feel free to tell me about it
