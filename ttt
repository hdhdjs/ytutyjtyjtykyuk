const Discord = require('discord.js');
const moment = require('moment');
const PREFIX = "#"
const fs = require('fs');
var prefix = "#";
const KiNg66S = new Discord.Client();
KiNg66S.on('ready', () => {
    console.log(`Logged in as ${KiNg66S.user.tag}!`);
    console.log(`in ${KiNg66S.guilds.size} servers `)
    console.log(`[Users] ${KiNg66S.users.size}`)

});



KiNg66S.on("message", function(message) {

  const bannedwords = [
    "كسمك",
"يا ابن المتناكة",
"kosomk",
"kosomen omk",
"kosomenomk",
"يا ابن الشرموطة",
"fk you",
"كسم مستر احمد",
"معرص",
"معيرص",
"يا ابن العرص",
"Gay",
"كصمك",
"هنيكك",
"متناكة",
"ك سمك",
"k.osomk",
"كسم",
"mtnak",
"ea abn el mtnaka",
"3rs"



  ];

  if(bannedwords.some(word => message.content.includes(word))) {
    message.delete()
    message.reply("ممنوع تشتم يسطي").then(m => m.delete(2000));
  };
});

KiNg66S.on('message', message => {
    if(message.content.includes('discord.gg')){
                                            if(!message.channel.guild) return message.reply('** advertising me on DM ? 🤔   **');
        if (!message.member.hasPermissions(['ADMINISTRATOR'])){
        message.delete()
    return message.reply(`:anger: ممنوع نشر سيرفرات  `).then(m => m.delete(3000));
    }
}
});

KiNg66S.on('message', eyad => {
  if (eyad.content.startsWith('mute')) {

if (!eyad.member.hasPermission("MOVE_MEMBERS")) return eyad.channel.send("**انت لا تمتلك الخاصيه المطلوبه** | ❎ ");
let men = eyad.mentions.users.first()
let mas = eyad.author
if(!men) return eyad.channel.send('`منشن الشخص الذي تريد ان تعطيه ميوت كتابي` ');
eyad.guild.channels.forEach(c => {
c.overwritePermissions(men.id, {
          SEND_MESSAGES: false
})
    })
const embed = new Discord.RichEmbed()
.setColor("RANDOM")
.setDescription(`**
 <@${men.id}>
لقد تم اعطائك ميوت كتابي
بواسطة : <@${eyad.author.id}> **`)

          
KiNg66S.users.get(men.id).sendEmbed(embed)
const Embed11 = new Discord.RichEmbed()
.setColor("RANDOM")
.setAuthor(eyad.guild.name, eyad.guild.iconURL)
.setDescription(`          <@${men.id}>
لقد تم اعطائه الميوت الكتابي بنجاح
بواسطة : <@${eyad.author.id}> `)
eyad.channel.sendEmbed(Embed11).then(eyad => {eyad.delete(20000)})
    }
})
KiNg66S.on('message', eyad => {
  if (eyad.content.startsWith('unmute')) {
          

if (!eyad.member.hasPermission("MOVE_MEMBERS")) return eyad.channel.send("**انت لا تمتلك الخاصيه المطلوبه** | ❎ ");
 let men = eyad.mentions.users.first()
 let mas = eyad.author
 if(!men) return eyad.channel.send('`منشن الشخص الذي تريد فك الميوت عنه `');
 eyad.guild.channels.forEach(c => {
 c.overwritePermissions(men.id, {
         SEND_MESSAGES: true
         })
    })
const embed = new Discord.RichEmbed()
.setColor("RANDOM")
.setDescription(`**
 <@${men.id}>
تم فك الميوت الكتابي 
بواسطة : <@${eyad.author.id}> **`)

KiNg66S.users.get(men.id).sendEmbed(embed)
const Embed11 = new Discord.RichEmbed()
.setColor("RANDOM")
.setAuthor(eyad.guild.name, eyad.guild.iconURL)
.setDescription(`          <@${men.id}>
تم فك الميوت الكتابي 
بواسطة : <@${eyad.author.id}>
`)

eyad.channel.sendEmbed(Embed11).then(eyad => {eyad.delete(20000)})
    }
})




KiNg66S.on ("guildMemberAdd", member => {
  
   var role = member.guild.roles.find ("name", "Fans <3");
   member.addRole (role);
  
})

KiNg66S.on ("guildMemberRemove", member => {
   
})

KiNg66S.on('ready', () => {console.log('ready')});
KiNg66S.on('message', message => {
    let args = message.content.split(' ').slice(1);
    if(message.content.startsWith(prefix + 'role')) {
        let member = message.mentions.users.first();
        let role = args.join(' ').replace(member, '').replace(args[0], '').replace(' ', '');
        console.log(role);
        if(member) {
              if(role.startsWith('-')) {
                let roleRe = args.join(' ').replace(member, '').replace(args[0], '').replace('-', '').replace(' ', '');
                console.log(roleRe);
                let role1 = message.guild.roles.find('name', roleRe);
                console.log(`hi`);
                if(!role1) return message.reply(`الرتبة غير موجودة بالسيرفر تأكد من الاسم`);
                message.guild.member(member).removeRole(role1.id);
            } else if(!role.startsWith('-')) {
                let roleRe = args.join(' ').replace(member, '').replace(args[0], '').replace('-', '').replace(' ', '');
                let role1 = message.guild.roles.find('name', roleRe);
                if(!role1) return message.reply(`الرتبة غير موجودة بالسيرفر تأكد من الاسم`);
                message.guild.member(member).addRole(role1);
            } else {
                message.reply(`يجب عليك كتابة اسم الرتبة`);
            } 
        }
 else if(args[0] == 'all') {
    if(role) {
    let role1 = message.guild.roles.find('name', role);
    if(!role1) return message.reply(`الرتبة غير موجودة بالسيرفر تأكد من الاسم`);
    message.channel.send(`الرجاء الانتظار حتى يتم الانتهاء من الامر`).then(msg => {
        message.guild.members.forEach(m => {
            message.guild.member(m).addRole(role1);
        });
        msg.edit(`تم الانتهاء من الامر ${message.guild.members.size}`);
    });
}
} else if(args[0] == 'humans') {
    if(role) {
        let role1 = message.guild.roles.find('name', role);
        if(!role1) return message.reply(`الرتبة غير موجودة بالسيرفر تأكد من الاسم`);
        message.channel.send(`الرجاء الانتظار حتى يتم الانتهاء من الامر`).then(msg => {
            message.guild.members.filter(m =>m.user.bot == false).forEach(m => {
                message.guild.member(m).addRole(role1);
            });
            msg.edit(`تم الانتهاء من الامر ${message.guild.members.size}`);
        });
    }
} else if(args[0] == 'bots') {
    if(role) {
        let role1 = message.guild.roles.find('name', role);
        if(!role1) return message.reply(`الرتبة غير موجودة بالسيرفر تأكد من الاسم`);
        message.channel.send(`الرجاء الانتظار حتى يتم الانتهاء من الامر`).then(msg => {
            message.guild.members.filter(m =>m.user.bot == true).forEach(m => {
                message.guild.member(m).addRole(role1);
            });
msg.edit(`تم الانتهاء من الامر ${message.guild.members.size}`);
});
}
}
}
});

KiNg66S.on('message', function(message) {
if (message.author.bot) return;
if (message.author.id === KiNg66S.user.id) return;
if (message.author.equals(KiNg66S.user)) return;
if (!message.content.startsWith(prefix)) return;

var args = message.content.substring(prefix.length).split(' ');
switch (args[0].toLocaleLowerCase()) {
case "مسح" :
message.delete()
if(!message.channel.guild) return
if(message.member.hasPermissions(0x2000)){ if (!args[1]) {
message.channel.fetchMessages()
.then(messages => {
message.channel.bulkDelete(messages);
var messagesDeleted = messages.array().length;
message.channel.sendMessage(' '+ " " + messagesDeleted + " " +  '**: عدد الرسائل التي تم مسحه**').then(m => m.delete(2500));
})
} else {
let messagecount = parseInt(args[1]);
message.channel.fetchMessages({limit: messagecount}).then(messages => message.channel.bulkDelete(messages));
message.channel.sendMessage(' '+ " " + args[1] + " " +  '**: عدد الرسائل التي تم مسحه**').then(m => m.delete(2500));
message.delete(60000);
}
} else {
var manage = new Discord.RichEmbed()
.setDescription('You Do Not Have Permission MANAGE_MESSAGES :(')
.setColor("RANDOM")
message.channel.sendEmbed(manage)
return;
}
}
});

 KiNg66S.on('message', message => {
           if (message.content.startsWith(prefix + "id")) {
                       if (!message.channel.guild) return message.reply('⚠ ممنوع الكتابة في الخاص ');

        var args = message.content.split(" ").slice(1);
      let user = message.mentions.users.first();
       var h = message.mentions.users.first();
          var h;
            if(h){
                var h = h;
            } else {
                var h = message.author;
                
            }
              var z = message.mentions.members.first();
          var z;
            if(z){
                var z = z;
            } else {
                var z = message.member;
            }
             moment.locale('ar-ly');
            let heroo = new Discord.RichEmbed()
            .setColor('RANDOM')
            .setThumbnail(h.avatarURL)
            .setAuthor(h.username,h.avatarURL)
            .addField(': تاريخ دخولك الدسكورد',`${moment(h.createdAt).format('D/M/YYYY h:mm a')} **\n** \`${moment(h.createdAt).fromNow()}\``,true)            
            .addField(': تاريخ دخولك السيرفر',`${moment(z.joinedAt).format('D/M/YYYY h:mm a ')} \n\`\`${moment(z.joinedAt).startOf(' ').fromNow()}\`\``, true)      
             .setFooter(`${h.tag}`,"https://images-ext-2.discordapp.net/external/JpyzxW2wMRG2874gSTdNTpC_q9AHl8x8V4SMmtRtlVk/https/orcid.org/sites/default/files/files/ID_symbol_B-W_128x128.gif")
            if(message.author.bot) return message.channel.send("**# Bots cannot excute commands!**");
            if(h.bot) return message.channel.send("**# Bots have no profiles!**");
         message.channel.send({embed:heroo})
           }
         });


KiNg66S.login(process.env.BOT_TOKEN2);
