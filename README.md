<h1 align="center">SHELL4CHAN</h1>
<p align="center">shell4chan is POSIX complient shell script that lets you grab and display threads from the very intelligent website 4chan.<br>This shit is still in the early fucking stages of development.
</p>

##
<p align="center">
<img src="./preview.mkv" alt="Video Preview" width="500px">
</p>

## REQUIREMENTS

* `dash` or any POSIX complient shell,usually `dash` if you are not brainlet 
* `curl` - you should have already if you are not fucking bastard
* `jq` - you need to have jq with sh-support branch compiled
here is shell command to compile my own fork of jq with sh-support
```sh
git clone https://github.com/zeta3301/jq /opt/jq/
cd /opt/jq/
autoreconf -fi
./configure
make -j8
sudo make install
```
* `timg` by default script will use this image viewer [timg](https://github.com/hzeller/timg/)<br>
but you can use libsixel to make better and faster image viewer.
`libsixel` [sixel](https://github.com/saitoha/libsixel)
for using img2sixel as image viewer you should uncomment this line
```sh
#sh_text("curl --create-dirs -sO --output-dir ~/.cache/shell4chan/ https://i.4cdn.org/\($board)/\(.tim)\(.ext) && img2sixel -w \(.tn_w) -h \(.tn_h) ~/.cache/shell4chan/\(.tim)\(.ext)")#
```
and comment or remove this line
```sh
sh_text("curl --create-dirs -sO --output-dir ~/.cache/shell4chan/ https://i.4cdn.org/\($board)/\(.tim)\(.ext) && timg -g\(.tn_w / 4)x\(.tn_h / 4) ~/.cache/shell4chan/\(.tim)\(.ext)")
```

shell command for compiling libsixel with libcurl
```sh
git clone https://github.com/saitoha/libsixel /opt/libsixel/
cd /opt/libsixel/
./configure --with-jpeg --with-png --with-libcurl 
make
sudo ln -s /opt/libsixel/converters/img2sixel /usr/local/bin/img2sixel
```
* `herbe`(optional,you need it when you use -b argument) the best fucking notification manager [herbe](https://github.com/zeta3301/herbe) otherwise it will use stupid `notify-send`

## Installation and Usage
curl **shell4chan** to your **$PATH** and give execute permissions.

```sh
$ doas curl -sL "https://raw.githubusercontent.com/zeta3301/shell4chan/main/shell4chan" -o /usr/local/bin/shell4chan
$ doas chmod +x /usr/local/bin/shell4chan
```

```sh
$ shell4chan BOARD THREAD_NUMBER
```

after viewing thread with less you have prompt to run commands on it
```sh
:thread THREAD_NUMBER
```
this will change thread variable and will give you new thread

```sh
:board BOARD
```
this command is still in work,you will be able to browse boards and chooose thread

```sh
:background
```
your thread will run in background and will give you notifications if there is new reply.<br>
if you don't have $TERMINAL exported,script will use xterm as default terminal.

```sh
:refresh
```
this will refresh the thread you are already watching with new posts

```sh
:quit
```
I will add more commands like :post or :reply, but that's are harder ones.

## License
Perhaps /g/ autists can't run script if there is no license even though i said that you can do what the fuck you want with this stupid shit.So I added AGPL License.

Feel free to modify it as needed motherfucker.
