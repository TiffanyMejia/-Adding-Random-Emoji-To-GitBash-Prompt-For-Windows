# Adding Random Emoji To GitBash Prompt For Windows

Step 1: Getting to GitBash profile

​	Open GitBash

​	type: vim ~/.bash_profile

​	Hit enter

Step 2: Place script into terrible looking GitBash

​	Press 'i' on keyboard to go into --insert-- mode

​	Copy and paste script

```````bash
# generate random emoji for prompt

HOST_NAME= Your Name Goes Here
# colors I may or may not use in PS1
red='\e[0;31m'      # Red
purple='\e[1;35m'   # Bold Purple
green='\[\033[0;32m\]'    # Green
reset='\e[0m'       # Text Reset
# choose emojis..kinda full list below
emojis=("🧀" "🌮" "⛵" ️"🚀" "💾" "💡" "🌈" "😺" "😸" "😹" "😻" "😼" "😽" "🙀" "😿" "😾" "💖" "💗" "💘" "💙" "💚" "💛" "💜" "🌱
" "🌲" "🌳" "🌴" "🌵" "🌷" "🌸" "🌹" "🌺" "🌻" "🌼" "🌽" "🌾" "🌿" "🍀" "🍁" "🍂" "🍃" "🍄" "🍅" "🍆" "🍇" "🍈" "🍉" "🍊" "🍋" "🍌" "🍍" "🍎" "🍏" "🍐" "🍑" "🍒" "🍓" "🍔" "🍕" "🍘" "🍙" "🍚" "🍛" "🍜" "🍝" "🍞" "🍟" "🍠" "🍡" "🍢" "🍣" "🍤" "🍥" "🍦" "🍧" "🍨" "🍩" "🍫" "🍭" "🍯" "🍰" "🍱" "🍲" "🐀" "🐁" "🐂" "🐃" "🐄" "🐅" "🐆" "🐇" "🐈" "🐉" "🐊" "🐋" "🐌" "🐍" "🐎" "🐏" "🐐" "🐑" "🐒" "🐓" "🐔" "🐕" "🐖" "🐗" "🐘" "🐙" "🐚" "🐛" "🐜" "🐝" "🐞" "🐟" "🐠" "🐡" "🐢" "🐣" "🐤" "🐥" "🐦" "🐧" "🐨" ">🐩" "🐪" "🐫" "🐬" "🐭" "🐮" "🐯" "🐰" "🐱" "🐲" "🐳" "🐴" "🐵" "🐶" "🐷" "🐸" "🐹" "🐺" "🐻" "🐼" "🐾" "👻" "👽" "👾" "🌑" ">🌒" "🌓" "🌔" "🌕" "🌖" "🌗" "🌘" "🌙" "🌚" "🌛" "🌜" "🌝" "🎵" "🎶" "🎷" "🎸" "🎹" "🎺" "🎻" "🎼" "🎃" "🔬" "🔭" "🔮")
# make it random
EMOJI=${emojis[$RANDOM % ${#emojis[@]} ]}

# don't know if this is relivant anymore...probably not 
parse_git_branch() {

  ref=$(git-symbolic-ref HEAD 2> /dev/null) || return
  echo "("${ref#refs/heads/}")"
}

# what shows on prompt
PS1="\n$purple$HOST_NAME: $green\$PWD\n $purple\n$EMOJI >"
```````

After placing script change HOST_NAME: to your name

Note: you can not use mouse to click around and can only copy, and past via right clicking on mouse.

Step 3: Save and Close GitBash Profile 

​	Press 'esc' key

​	Type :wq 

​	Hit Enter

​	Close and reopen GitBash

Great now you have a random emoji with your username, and file path....but the emoji looks terrible.... I KNOW

Step 4: Getting those sweet sweet colorful emojis

​	Open git bash with admin privilege. (by right clicking GitBash and selecting "Run as Administrator")

​	Type each line below individually hitting enter after each one. (copy and paste for ease) 

```
cd "C:/Program Files/Git/usr/share/mintty"
mkdir -p emojis
cd emojis
curl https://raw.githubusercontent.com/wiki/mintty/mintty/getemojis > getemojis
./getemojis -d
```

Its going to take forever.....longer than two dogs going poop one at a time by my records

Step 5: Make it pretty

​	Right click on GitBash when that finishes

​	Click options

​	Click text

​	Change settings to match ones below

 ![image-20220113192159296](C:\Users\Heather\AppData\Roaming\Typora\typora-user-images\image-20220113192159296.png)



Be happy....because it took me hours to figure this out and now you can too in less than 10 minuets 



Sorta Full List of Emojis: Remember to put quotes around the ones you add. I am not doing it for you because it took me too long to do the ones in the script. 

````bash
⌚ ⌛ ⏩ ⏪ ⏫ ⏬ ⏰ ⏳ ▪ ▫ ▶ ◀ ◻ ◼ ◽ ◾ ☀ ☁ ☎ ☑ ☔ ☕ ☝ ☺ ♈ ♉ ♊ ♋ ♌ ♍ ♎ ♏ ♐ ♑ ♒ ♓ ♠ ♣ ♥ ♦ ♨ ♻ ♿ ⚓ ⚠ ⚡ ⚪ ⚫ ⚽ ⚾ ⛄ ⛅ ⛎ ⛔ ⛪ ⛲ ⛳ ⛵ ⛺ ⛽ ✂ ✅ ✈ ✉ ✊ ✋ ✌ ✏ ✒ ✔ ✖ ✨ ✳ ✴ ❄ ❇ ❌ ❎ ❓ ❔ ❕ ❗ ❤ ➕ ➖ ➗ ➡ ➰ ⤴ ⤵ ⬅ ⬆ ⬇ ⬛ ⬜ ⭐ ⭕ 🀄 🃏 🌀 🌁 🌂 🌃 🌄 🌅 🌆 🌇 🌈 🌉 🌊 🌋 🌌 🌍 🌎 🌏 🌐  🌞 🌟 🌠 🌰  🍳 🍴 🍵 🍶 🍷 🍸 🍹 🍺 🍻 🍼 🎀 🎁 🎂  🎄 🎅 🎆 🎇 🎈 🎉 🎊 🎋 🎌 🎍 🎎 🎏 🎐 🎑 🎒 🎓 🎠 🎡 🎢 🎣 🎤 🎥 🎦 🎧 🎨 🎩 🎪 🎫 🎬 🎭 🎮 🎯 🎰 🎱 🎲 🎳 🎴 🎽 🎾 🎿 🏀 🏁 🏂 🏃 🏄 🏆 🏇 🏈 🏉 🏊 🏠 🏡 🏢 🏣 🏤 🏥 🏦 🏧 🏨 🏩 🏪 🏫 🏬 🏭 🏮 🏯 🏰 👀 👂 👃 👄 👅 👆 👇 👈 👉 👊 👋 👌 👍 👎 👏 👐 👒 👓 👔 👕 👖 👗 👘 👙 👚 👛 👜 👝 👞 👟 👠 👡 👢 👣 👤 👥 👦 👧 👨 👩 👪 👫 👬 👭 👮 👯 👰 👱 👲 👳 👴 👵 👶 👷 👸 👹 👺 👿 💀 💁 💂 💃 💄 💅 💆 💇 💈 💉 💊 💋 💌 💍 💎 💏 💐 💑 💒 💓 💔 💕 💝 💞 💟 💠 💡 💢 💣 💤 💥 💦 💧 💨 💩 💪 💫 💬 💭 💮 💯 💰 💱 💲 💳 💴 💵 💶 💷 💸 💹 💺 💻 💼 💽 💾 💿 📀 📁 📂 📃 📄 📅 📆 📇 📈 📉 📊 📋 📌 📍 📎 📏 📐 📑 📒 📓 📔 📕 📖 📗 📘 📙 📚 📛 📜 📝 📞 📟 📠 📡 📢 📣 📤 📥 📦 📧 📨 📩 📪 📫 📬 📭 📮 📯 📰 📱 📲 📳 📴 📵 📶 📷 📹 📺 📻 📼 🔀 🔁 🔂 🔃 🔄 🔅 🔆 🔇 🔉 🔊 🔋 🔌 🔍 🔎 🔏 🔐 🔑 🔒 🔓 🔔 🔕 🔖 🔗 🔘 🔙 🔚 🔛 🔜 🔝 🔞 🔟 🔠 🔡 🔢 🔣 🔤 🔥 🔦 🔧 🔨 🔩 🔪 🔫 🔯 🔰 🔱 🔲 🔳 🔴 🔵 🔶 🔷 🔸 🔹 🔺 🔻 🔼 🔽 🕐 🕑 🕒 🕓 🕔 🕕 🕖 🕗 🕘 🕙 🕚 🕛 🕜 🕝 🕞 🕟 🕠 🕡 🕢 🕣 🕤 🕥 🕦 🕧 🗻 🗼 🗽 🗾 🗿 😀 😁 😂 😃 😄 😅 😆 😇 😈 😉 😊 😋 😌 😍 😎 😏 😐 😑 😒 😓 😔 😕 😖 😗 😘 😙 😚 😛 😜 😝 😞 😟 😠 😡 😢 😣 😤 😥 😦 😧 😨 😩 😪 😫 😬 😭 😮 😯 😰 😱 😲 😳 😴 😵 😶 😷  🙅 🙆 🙇 🙈 🙉 🙊 🙋 🙌 🙍 🙎 🙏 🚀 🚁 🚂 🚃 🚄 🚅 🚆 🚇 🚈 🚉 🚊 🚌 🚍 🚎 🚏 🚐 🚑 🚒 🚓 🚔 🚕 🚖 🚗 🚘 🚙 🚚 🚛 🚜 🚝 🚞 🚟 🚠 🚡 🚢 🚣 🚤 🚥 🚦 🚧 🚨 🚩 🚪 🚫 🚬 🚭 🚮 🚯 🚰 🚱 🚲 🚳 🚴 🚵 🚶 🚷 🚸 🚹 🚺 🚻 🚼 🚽 🚾 🚿 🛀 🛁 🛂 🛃 🛄 🛅 🅰 🆎 🅱 🆑 🆒 🆓 ℹ 🆔 Ⓜ 🆕 🆖 🅾 🆗 🅿 🆘 ™ 🆙 🆚 🈁 🈂 🈹 🉑 🈴 🈺 🉐 🈯 🈷 🈶 🈵 🈚 🈸 ㊗ 🈲 ㊙ 🈳 💖 💗 💘 💙 💚 💛 💜🌱 🌲 🌳 🌴 🌵 🌷 🌸 🌹 🌺 🌻 🌼 🌽 🌾 🌿 🍀 🍁 🍂 🍃 🍄 🍅 🍇 🍈 🍉 🍊 🍋 🍌 🍍 🍎 🍏 🍐 🍒 🍓 🍔 🍕 🍘 🍙 🍚 🍛 🍜 🍝 🍞 🍟 🍠 🍡 🍢 🍣 🍤 🍥 🍦 🍧 🍨 🍩 🍪 🍫 🍬 🍭 🍮 🍯 🍰 🍱 🍲 😸 😹 😺 😻 😼 😽 😾 😿 🙀 🐀 🐁 🐂 🐃 🐄 🐅 🐆 🐇 🐈 🐉 🐊 🐋 🐌 🐍 🐎 🐏 🐐 🐑 🐒 🐓 🐔 🐕 🐖 🐗 🐘 🐙 🐚 🐛 🐜 🐝 🐞 🐟 🐠 🐡 🐢 🐣 🐤 🐥 🐦 🐧 🐨 🐩 🐪 🐫 🐬 🐭 🐮 🐯 🐰 🐱 🐲 🐳 🐴 🐵 🐶 🐷 🐸 🐹 🐺 🐻 🐼 🐽 🐾 👻 👼 👽 👾 🌑 🌒 🌓 🌔 🌕 🌖 🌗 🌘 🌙 🌚 🌛 🌜 🌝 👑  🔬 🔭 🔮
````

