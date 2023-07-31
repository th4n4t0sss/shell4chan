<h1 align="center">SHELL4CHAN</h1>
<p align="center">shell4chan is pure POSIX complient shell script that lets you grab and display threads from the very intelligent website 4chan.<br>This shit is still in the early fucking stages of development.
</p>

## REQUIREMENTS

* `dash` or any POSIX complient shell,usually `dash` if you are not brainlet 
* `curl` - you should have already if you are not fucking bastard
* `jq` - with sh branc compiled
* `timg` - sorry again for bloat nigger.your faggot ass needed image viewer [timg](https://github.com/hzeller/timg)
* `img2sixel` - if you want better image viewer install this and read bellow how to enable it. 
* `herbe` - (optional,you need it when you use -b argument) the best fucking notification manager [herbe](https://github.com/zeta3301/herbe) otherwise it will use stupid `notify-send`
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
I am to lazy now to documante this.I go to sleep tomorrow i will say how to do that now read code.

## License
Perhaps /g/ autists can't run script if there is no license even though i said that you can do what the fuck you want with this stupid shit.So I added AGPL License.

Feel free to modify it as needed motherfucker.
