## How to use Vertix Hosting
---
So you want to get free hosting but know how to use Vertix Hosting? How do you make an account and create your server? This guide will give you all the information your need from starting your server, to uploading your files with WinSCP (SFTP) we can cover it all for you.

External Reading: 
> https://support.vertixstudios.com/how-to-use-vertix-hosting

## Creating your account.
----
To create your account head over to #commands in our Discord, and using  simply type `/` and you will be greeted with all the commands the bot has, to make the account type: `/createaccount <username>` - you will then see a ticket created at the *top* of the server where you can fill out the required information `<email> <password>`.

You can then head over to https://panel.vertixstudios.com/ and login with the information you just provided us; *please allow 1 minute for our database to update.*

##  Creating your first server.
----
Once you have your account created you can then head back over to #commands and using the slash commands type: `/servercreate <type> <name>` - you will then see the bot reply with a message, this is the bot created your server. Once the bot has created your server it will edit the message with another message that has a button attached to it, clicking the button will open up your server in our panel. 

When you open your panel for the first time it will run through a installation, this can take up to 3 minutes so please be patient.

**SERVER TYPES**
When you ran this command you were asked to fill in a param called `<type>` - this is the type of server that will be created the following are the current types of servers there is: 
- `NodeJs`
- `Python` 
- `AIO`
- `Java`
- `MongoDB`
- `RedIs`

## Uploading files manually to your server.
----
You can then upload your files under the file manager tab found on the left side nav here you can upload your files - to create a folder/directory click the `create directory` at the top. You can drag and drop single files such as `index.js` etc but folders must be created with the `create directory` button. 

Make sure to not upload `node_modules` as the server will automaticaly run `npm i` and install all packages from `package.json`

##  Uploading files to your server using a SFTP uploader.
----
If you don't want to manualy upload your files you can use a SFTP uploader,to use a SFTP with the server head over to `Settings` on the side nav and then you will see a `SFTP DETAILS` card at the top, you will see a `Server Adress` and a `Username`

Something like this: 

**Server Adress**
`sftp://panel.vertixstudios.com/3423`

**Username**
`kiphlo.82jg9ioe`

You will then see a `Launch SFTP` button which once clicked will open your SFTP.

We recommend using [WinSCP](https://winscp.net/eng/index.php) for your SFTP client.

You will see a window that looks likes this: 
![](https://kiphlo.reeee.ee/4EpZP2.png)

The Left side is your local machine (computer) and the right side is your server you created, simple select all the files on the left **EXPECT NODE_MODULES** and WinSCP will upload the files to the server and you are good to go.

## Starting your server
----
Once all of your files and folders have been uploaded you can head back to the `Conole` in the panel by clicking on `Console` on the left side nav.

On the left side you will see `OFFLINE`; To turn the server online simply click the green `START` button and the server will go through and install all of your dependencies from the `package.json` file you uploaded. 

Boom! You are now live and running, now its time to enjoy the application you created.
