# TH-relay
Bot that relay messages from discord to Twitter and Stocktwits

uses fallguy(alertrelay@thetradehub.net) for user_token

Commands

addch <channelMention> <currency> <delay>optional <totalHashtags>optional
remch <channelMention>
.send <message>

p!add_user <@user>
p!remove_user <@user>
p!add_ch <#channel> <stocks/crypto> [# of minutes delay - `0` if none] <# of hashtags>
p!remove_ch <#channel>
p!stocktwits <message> (TBD: (can upload image as well that will be sent with post))


3 tokens are required

bot_token for Discord bot to see message data and use .stocktwits command to manually post
user_token is for the Discord account used to login and take a screenshot of the messages being relayed. !USE AN ALT!
access_token is stocktwits token

if using linux, make sure 'executable path' on line 16 is set to your chromedriver path
/usr/lib/chromium-browser/chromedriver

// to get stocktwits access_token\\
to get stocktwits auth key paste this in browser console;
or f12 > application > in storage click cookies > stocktwits.com > access_token

OR paste this in browser console

function getCookie(cname) {
  var name = cname + "=";
  var ca = document.cookie.split(';');
  for(var i = 0; i < ca.length; i++) {
    var c = ca[i];
    while (c.charAt(0) == ' ') {
      c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
      return c.substring(name.length, c.length);
    }
  }
  return "";
}
console.log(getCookie("access_token"))

// ^^ stocktwits access_token \\
