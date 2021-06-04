## How to use Vertix Hosting
So you want to get free hosting but know how to use Vertix Hosting? How do you make an account and create your server? This guide will give you all the information your need from starting your server, to uploading your files with WinSCP (SFTP) we can cover it all for you.

External Reading: 
> https://support.vertixstudios.com/how-to-use-vertix-hosting

## Creating your account.
To create your account head over to #commands in our Discord, and using  simply type `/` and you will be greeted with all the commands the bot has, to make the account type: `/devcreate` - some options should show up, these are called *parameters*. The parameters that are required are `username`, `email`, and `password`. Once you've filled out those fields, hit enter on your keyboard, or send on your mobile device, and you should get a response that looks something like this: 

![](https://devnoah.reeee.ee/rj7M9l.png).

You can then head over to https://panel.vertixstudios.com/ and login with the information that was provided back to you.

##  Creating your first server.
Once you have your account created you can then head back over to #commands and using the slash command, type: `/servercreate <type> <name>` - you will then see the bot reply with a message, this is the bot created your server. Once the bot has created your server it will edit the message with another message that has a button attached to it, clicking the button will open up your server in our panel. 

When visiting our panel for the first time, it will prompt you to login, so again, please login with the information that was provided back to you on the `/devcreate` command.

**SERVER TYPES**
When you ran this command you were asked to fill in a param called `<type>` - this is the type of server that will be created the following are the current types of servers there is: 
- `NodeJs`
- `Python` 
- `AIO`
- `Java`
- `MongoDB`
- `RedIs`

### For the remainder of this guide, we will assume that you are using a NodeJS server.
 Additional Documentation for other server types will be provided soon.

## Uploading files manually to your server.
You can then navigate to the *File Manager*. You can find this page by clicking on your server, then taking a look at the sidebar located on the left. By default, the main directory for your NodeJS application is `/home/container`, but as usual, you can navigate to other files using `./` or `../`. You can drag and drop single files such as `index.js`, or upload ZIP files, which can then be *unarchived*, allowing all the contents in the ZIP to be extracted and put into the server.. 

*Optional:* You can choose to not upload your `node_modules` as the server will automaticaly run `npm i` and install all packages from your `package.json`

##  Uploading files to your server using a SFTP uploader.
If you don't want to upload your files through the panel, you can use an SFTP uploader, to use a SFTP with the server head over to `Settings` tab. You can find this page by clicking on your server, then taking a look at the sidebar located on the left. You will then see an `SFTP DETAILS` card at the top, you will see a `Server Adress` and a `Username`

Something like this: 

![](https://devnoah.reeee.ee/vIwnWW.png)

You will then see a `Launch SFTP` button which once clicked will open your SFTP preferred SFTP client.

*Note:* We recommend using [WinSCP](https://winscp.net/eng/index.php) for your SFTP client.

You will see a window that looks likes this: 
![](https://kiphlo.reeee.ee/4EpZP2.png)

The Left side is your local machine (computer) and the right side is your server you created, simply select all the files that you wish to transfer on the left, drag them over to the right, and WinSCP will upload the files to the server and you are good to go.

## Starting your server
Once all of your files and folders have been uploaded you can head back to the `Console` in the panel by clicking on `Console` Tab. You can find this page by clicking on your server, then taking a look at the sidebar located on the left.

On the upper left side of this page, you will see an `OFFLINE` button; To turn the server online, simply click the green `START` button and the server will go through and install all of your dependencies from the `package.json` file you uploaded. 

Boom! You are now live and running, now its time to enjoy the application you created.
