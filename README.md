# ionic-sidemenu-bug

### How to setup
```
git clone https://github.com/RafaelKr/ionic-sidemenu-bug
cd ionic-sidemenu-bug/
npm install
ionic serve
```

### How to reproduce the bug
Use Chrome in Version 54+.

Open the link printed by `ionic serve` in Chrome (maybe also in Chromium)  
`dev server running: http://localhost:8100/`

Now press F12, to toggle developer tools. Switch to "Device Toolbar". On Linux this is `Ctrl+Shift+M`.  

Scroll down, open the sidemenu and look, if all or some of the Infoboxes are disappearing. Maybe only partially. If not, close the menu, scroll and try again.

##### Description I've posted to ionic-worldwide.slack.com:
> Hi everyone. Yesterday I had this mysterious bug with the ionic-starter-sidemenu, but had no code to share. Now I encapsulated the problem and maybe you could have a look.  
First my repo: https://github.com/RafaelKr/ionic-sidemenu-bug
>
>The problem is, if you scroll down and then open the sidemenu, the elements (maybe only some of them) are disappearing.  
I encounter this issue when using `ionic serve` in Chrome Version 55.0.2883.75 (64-bit) on Linux and in Chrome Version 54.0.2840.98 (64-bit) on Mac.  
It doesn't happens on Chromium Version 53.0.2785.143 Built on Ubuntu , running on LinuxMint 18 (64-bit). Also not in Firefox 50.0.2 on Linux.  
Also with Ionic View on an iPhone 6 it behaves, as it should. So maybe this is a bug in Chrome 54+.
>
>And this happens not only with ionic serve. Also if I run it with ionic run android on my device.  
Another thing, that would be indicative that it's a Chrome bug is, that if I use chrome://inspect with screencast,  
sometimes it shows the elements in the screencast, but not on the device.
>
>I also should mention, that the mode is always set to iOS, because that's also the case in the application we're developing, but it also happens, if you remove that line in app.module.ts  
Who else experiences this issue?
