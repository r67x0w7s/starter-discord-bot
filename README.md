
**Update Time: 2024/04/16 20:46:53**

# starter-discord-bot

Follow these instructions after deploying this repo on Cyclic.sh

[![Deploy to Cyclic](https://deploy.cyclic.app/button.svg)](https://deploy.cyclic.app/)


## Set-up and configuration

### **1.** Create discord application

Navigate to Discord's developer portal and create a new application
 - https://discord.com/developers/applications

<p align="center">
    <img src="./doc/1.png"  width="500px"/>
</p>

### **2.** Get application keys and parameters
After creating the application, you are taken to the application's dashboard. There you can configure an app icon, description, etc. 

Retrieve:
- `APPLICATION ID` (Discord also calls this `CLIENT ID`)
- `PUBLIC KEY`

Configure your Cyclic App with these environment variables.

<p align="center">
    <img src="./doc/2.png"  width="500px"/>
</p>

### **3.** Enable the Bot in the application
On the left hand side, go to `Bot` then click on `Add Bot`

You will need to create the bot token. 
Press `Reset Token` and confirm.
<p align="center">
    <img src="./doc/3.png"  width="400px"/>
</p>


Retrieve the `TOKEN` string and configure your Cyclic App with this environment variable.

### **4.** Adding the bot to your server
The easiest way to add the bot to your server is via url. 

Go to `OAuth2` > `URL Generator` on the left, select the permissions:
- `applications.commands` - allows you to register slash commands
- `bot` - this will show additional permissions for the bot
  - `Send Messages` - to allow the bot to send messages 

<p align="center">
    <img src="./doc/4.png"  width="500px"/>
</p>

Copy and navigate to the generated URL at the bottom. 

The page will ask you to select a server to install your bot on, it will go through a few prompts to verify that you are human. 

<p align="center">
    <img src="./doc/5.png"  width="400px"/>
</p>

After you authorize, the bot will appear in your server.
<p align="center">
    <img src="./doc/6.png"  width="400px"/>
</p>

**Keep in mind, the bot does not yet have any code running, so it will not do anything just yet**



### **5.** Get your Server ID
To get the server id (Discord also calls this GUILD ID), you first have to enable developer mode for in your discord user settings > advanced:
<p align="center">
    <img src="./doc/0.png"  width="500px"/>
</p>

With developer mode on, you will be able to right click the discord server name to copy it's id:
<p align="center">
    <img src="./doc/7.png"  width="200px"/>
</p>

Developer mode allows you to right click all kinds of things in discord to get their id's (channels, users, messages, etc.)


## **6.** Set up environment variables
At this point, make sure you've collected all the variables you will use in your environment
- CLIENT_ID (same as Application ID)
- PUBLIC_KEY
- TOKEN
- GUILD_ID (same as Server ID)

<p align="center">
    <img src="./doc/8.png"  width="600px"/>
</p>

# Set up interactions endpoint
