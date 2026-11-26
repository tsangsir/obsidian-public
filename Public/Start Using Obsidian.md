I evaluated many note taking app / web pages, like Notion, Google Keep, OneNote, Confluence. I couldn't settle to any one: people always said something else is better, so I was always planning a switch.

After evaluating my requirements against different products, I decide to give Obsidian a try.

My requirements:
1. Free usage
2. Messages are usually copy and pasted, but require edit and merge function
3. Support nested tables, merged cells
4. Message arranged in tree / hierarchical structure 
5. Message can link to another tree
6. Support images
7. Usable both on computer and mobile phone

After some chat with AI, 3 candidates remained
1. Notion
2. Obsidian 
3. Capacities 

### Comparison

### Obsidian was Selected!

### Obsidian Cavaets and Solutions
1. Local application
2. File Name as Title
3. Sync / usage between devices - Windows, Linux, FreeBSD, Android
4. Encryption of Private Notes

### Git Setup
To make Git support Chinese (UTF8?) character in Title, i.e., file name, the following configuration is needed.

```$ git config core.quotePath false```

I made this a local, repository specific setting. Though it seems OK to set it in global level (`--global).` This needs to be set in every device.
### Encryption
Once considered making the Obsidian vault of Private Notes a RClone Vault, so that the data was committed to github encrypted. This is unfortunately rejected, because of the following incompatibilities.

On RClone side:
 - Can RClone in Termux mount a crypt to a directory visible by other Apps (instead of inside the Termux filesystem). This may be possible but not checked yet.
 - RSAF may be able to mount and expose as SAF. However, Obsidian does not support SAF. And RSAF is not in Play Store yet.
 - Round Sync, RCX seem not active updated, and mountpoints are exposed as SAF too.

On Obsidian side:
- SAF not supported. Plugins may be available for SAF, need further evaluation.

On Git side:
 - No meaningful version control
 - Evaluate Git Crypt next

Currently no secret in Private Notes yet, so it is still acceptable.