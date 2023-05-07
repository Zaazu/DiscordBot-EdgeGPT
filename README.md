# DiscordBot-EdgeGPT
> ### Using Bing on discord bot, your Microsoft account needs to be able to access Bing first.

> **Warning**
> ### 2023/5/7: Can get image by create conversation style, but sometime will fail.
> ### 2023/5/4: Can't get image by create conversation style

## Update
> ### 2023/5/7: Mention bot for replyall messsages.
> ### 2023/4/26 : Create a separate chat for each user.
> ### 2023/4/24 : Now can generate images by Creative style.
   
## Features

<details>
   <summary>
   
   ### Slash command

   </summary>
   
> ### will create a separate chat for each user.
   
* bing: `/bing [message]`

   | USE_SUGGEST_RESPONSES: True  (can change in file ```config.yml```) |
   |---|
  ![edgegpt](https://i.imgur.com/cLPL156.png)

   | USE_SUGGEST_RESPONSES: False (can change in file ```config.yml```) |
   |---|
  ![edgegpt](https://i.imgur.com/yK3P9Kt.png)
  
  | conversation style: Creative |
   |---|
  ![creative_style](https://i.imgur.com/IIzRsqj.png)
  
* bing image creator: `/create_image [prompt]`
  
  ![bingimage.png](https://i.ibb.co/0rxNbnk/2023-04-07-191036.png)
 
* conversation style (default balanced): `/switch_style [style]`
  
  ![style.png](https://i.ibb.co/54KMWKH/2023-04-07-200312.png)

* reset: `/reset`

  ![reset](https://i.imgur.com/AG5qQ1F.png)
</details>

<details>
   <summary>
   
   ### Mention bot

   </summary>

> ### same function as the slash command, but this will reply all user messages.

* If only the bot is mentioned, you will get a drop-down list of settings.

  ![dropdown1](https://i.imgur.com/XDcnTuC.png)
  ![dropdown2](https://i.imgur.com/azHIUqv.png)

* Same as use `/bing`,

  ![mention1](https://i.imgur.com/aC5ZM9y.png)
  
  after switching styles to creative, you can also generate images!
  
  ![mention2](https://i.imgur.com/3w0vYKt.png)

</details>

<details>
   <summary>
   
   ### Prefix command (available only to bot owner)

   </summary>
 
 > ### bot owner setting.
   
 * `!unload [file_name_in_cogs_folder]`: Disable command from the specified file.
 * `!load [file_name_in_cogs_folder]`: Enable the command from the specified file.
 
   ![load & unload](https://i.imgur.com/spsyAEG.png)
  
 * `!clean`: Empty discord_bot.log file.
 * `!getLog`: Get discord_bot.log file. Real-time tracking of the bot's operating status.
   
   ![getLog](https://i.imgur.com/LHX4yWV.png)
 
 * `!upload [.txt_file]`: Because Bing Cookies will expire, so this command can set new Cookies directly and restart bot. You just need to copy bing cookies and past,                           the Cookies will auto convert to .txt file.
 
   ![upload](https://i.imgur.com/UN1Ac7N.png)
</details>

## Install
```
pip install -r requirements.txt
```

## Usage
1. Rename the file`.env.dev`to`.env`, then open it and edit it. If you don't want a limit channel to mention a bot, you don't need to set up a   MENTION_CHANNEL_ID, just leave it blank.
   ```
   DISCORD_BOT_TOKEN=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
   MENTION_CHANNEL_ID=123456789
   ```
   
2. Get Bing authentication.
   * Install the cookie editor extension for Chrome or Firefox.
   * Go to [bing.com](http://bing.com/chat)
   * Click "Export" on the bottom right.
   * Paste your cookies into a file `cookies.json`

4. Start run your bot, hosted locally or on a server.

   -> Recommended Free Servers: [fly.io](https://fly.io/)

## Credits
* EdgeGPT - [https://github.com/acheong08/EdgeGPT](https://github.com/acheong08/EdgeGPT)
* BingImageCreator - [https://github.com/acheong08/BingImageCreator](https://github.com/acheong08/BingImageCreator)
* other - [https://github.com/Zero6992/chatGPT-discord-bot](https://github.com/Zero6992/chatGPT-discord-bot)

## Contributors

This project exists thanks to all the people who contribute.

 <a href="https://github.com/FuseFairy/DiscordBot-EdgeGPT/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=FuseFairy/DiscordBot-EdgeGPT" />
 </a>
