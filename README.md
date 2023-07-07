<h1 align="center">SHELL4CHAN</h1>
<p align="center">shell4chan is pure POSIX complient shell script that lets you grab and display threads from the very intelligent website 4chan.<br>This shit is still in the early fucking stages of development.
</p>

## REQUIREMENTS

* `dash` or any POSIX complient shell,usually `dash` if you are not brainlet 
* `curl` - you should have already if you are not fucking bastard
* `jq` fucking install it now
* `dmenu` it's optional but sorry for bloat.u need dmenu only if you want to search through boards.use my build of [dmenu](https://github.com/zeta3301/dmenu).If you don't have center patch remove -c from script
* `viu` sorry again for bloat nigger.your faggot ass needed image viewer [viu](https://github.com/atanunq/viu)
* `herbe`(optional,you need it when you use -b argument) the best fucking notification manager [herbe](https://github.com/zeta3301/herbe) otherwise it will use stupid `notify-send`
## Installation and Usage
curl **shell4chan** to your **$PATH** and give execute permissions.

```sh
$ doas curl -sL "https://raw.githubusercontent.com/zeta3301/shell4chan/main/shell4chan" -o /usr/local/bin/shell4chan
$ doas chmod +x /usr/local/bin/shell4chan
```
hahahaha use doas idiot

```sh
$ shell4chan BOARD THREAD_NUMBER
```
### background mode
```sh
$ shell4chan BOARD THREAD_NUMBER -b
```
### download thread
```sh
$ shell4chan BOARD THREAD_NUMBER -d 
```
Script will redirect the output to /home/$USER/.local/share/shell4chan/BOARD/THREAD_NUMBER.thread<br>
You can view the thread with less -R THREAD_NUMBER.thread.If you want to change the directory you can just modify the script.I will not add stupid argument for that.
## Functionality
The current version of this trashy Shell4chan has barely any functionality to speak of.<br>It just pulls and vomits out a thread from 4chan, and it looks as raw as your stupid face right now.<br>
This script is still being worked on, and more features and improvements will be added.

## License
Perhaps /g/ autists can't run script if there is no license even though i said that you can do what the fuck you want with this stupid shit.

## Disclaimer
Listen up, you braindead idiot.<br>The shell4chan script has nothing to do with the official 4chan website. Use it at your own risk, and don't blame me if you get banned or end up in some internet flame war.

### Will be added soon
* ~~Images in terminal(probably with w3m)~~
* Support for multiple threads and boards,
* ~~Perhaps you will have some options and filters for you to play with, you ungrateful twat.~~
* I might even think about throwing in some error handling, just to shut you up.
* Post reply
* ~~Run thread on background and send notification if new reply was added~~

Feel free to modify it as needed motherfucker.
