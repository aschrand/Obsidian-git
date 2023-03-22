[Sync Your Obsidian Vault for Free with Github – Curtis McHale](https://curtismchale.ca/2022/05/18/sync-your-obsidian-vault-for-free-with-github/)

To get started you’re going to need to go to Github and create an account if you don’t have one. Then in the top right corner click the small + button and choose New Repository to create a new repository to house your Obsidian Vault.

To start, open your command line application, macOS ships with Terminal, and use the cd command to change to the directory where you want to save your new Obsidian vault. I’m going to put mine in my documents folder so my command is cd ~/Documents.

Next, you’ll need to create a folder to hold your Obsidian Vault. I’ll call mine obsidian-git-sync which means the command to use is mkdir obsidian-git-sync. Then we’ll need to move into that directory with cd obsidian-git-sync.

Now we need to turn this folder into one that supports Git by using git init.
Now we need to head back to our web browser and look at the commands that Github provided us once we had created the repository. We want to use the set of commands that allow us to push an existing repository to Github.