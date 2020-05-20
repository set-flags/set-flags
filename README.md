# Set Flags

Last login: Tue May 19 23:52:52 on ttys000
Yijuns-Air.lan
yy66@Yijuns-Air ~ % df -h
Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1s5   112Gi   11Gi  6.8Gi    61%  487483 1174983277    0%   /
devfs          201Ki  201Ki    0Bi   100%     703          0  100%   /dev
/dev/disk1s1   112Gi   91Gi  6.8Gi    94% 2277844 1173192916    0%   /System/Volumes/Data
/dev/disk1s4   112Gi  3.0Gi  6.8Gi    31%       6 1175470754    0%   /private/var/vm
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /System/Volumes/Data/home
yy66@Yijuns-Air ~ % mkdir tmp
yy66@Yijuns-Air ~ % cd tmp
yy66@Yijuns-Air tmp % pbpaste > Dockerfile
yy66@Yijuns-Air tmp % docker build -t gitpod .
Sending build context to Docker daemon  2.048kB
Step 1/9 : FROM gitpod/workspace-full
latest: Pulling from gitpod/workspace-full
767fb6cc1b89: Pulling fs layer 
c917d9c558a3: Pulling fs layer 
6fef7dab6264: Pulling fs layer 
bd7950fd118d: Pulling fs layer 
3ffa145b6100: Pulling fs layer 
a5dec3ed7b85: Pulling fs layer 
ec38c403de6c: Waiting 
501559b8a3c1: Waiting 
80fe7603817c: Waiting 
36e39ecb389b: Pull complete 
ca2e5aaeae2c: Pull complete 
45edd1f3df92: Pull complete 
798d4904b0a1: Pull complete 
d9f8617634d9: Pull complete 
ffa26ddda8e9: Pull complete 
f91baca3a7a7: Pull complete 
3ec9a85bcaf3: Pull complete 
6bfb1f07b214: Pull complete 
938c257f42a8: Pull complete 
7e5fc71c8b9c: Pull complete 
32028efa82b5: Extracting [==================================================>]  423.7MB/423.7MB
f039b4327bc1: Download complete 
8426bf467890: Download complete 
cdcccd0aaa36: Download complete 
67cdd0cebcda: Download complete 
9588a1e82bdb: Download complete 
68c48429a63c: Download complete 
532cbee2a69c: Download complete 
5a3330ee7170: Download complete 
546956fed7f9: Download complete 
fe41185dfb99: Download complete 
df0bcf4052d8: Download complete 
failed to register layer: Error processing tar file(exit status 1): symlink /home/gitpod/.sdkman/candidates/maven/3.6.3 /home/gitpod/.sdkman/candidates/maven/current: structure needs cleaning
yy66@Yijuns-Air tmp % df -h
Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1s5   112Gi   11Gi   10Mi   100%  487483 1174983277    0%   /
devfs          201Ki  201Ki    0Bi   100%     703          0  100%   /dev
/dev/disk1s1   112Gi   97Gi   10Mi   100% 2277591 1173193169    0%   /System/Volumes/Data
/dev/disk1s4   112Gi  3.0Gi   10Mi   100%       6 1175470754    0%   /private/var/vm
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /System/Volumes/Data/home
yy66@Yijuns-Air tmp % docker system prune -af
Total reclaimed space: 0B
yy66@Yijuns-Air tmp % df -h
Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1s5   112Gi   11Gi  113Mi    99%  487483 1174983277    0%   /
devfs          201Ki  201Ki    0Bi   100%     703          0  100%   /dev
/dev/disk1s1   112Gi   97Gi  113Mi   100% 2277984 1173192776    0%   /System/Volumes/Data
/dev/disk1s4   112Gi  3.0Gi  113Mi    97%       6 1175470754    0%   /private/var/vm
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /System/Volumes/Data/home
yy66@Yijuns-Air tmp % cd ~/Library/Application\ Support 
yy66@Yijuns-Air Application Support % ls
AddressBook				MediaHuman				com.apple.kvs
Adobe					Microsoft				com.apple.replayd
App Store				Microsoft AU Daemon			com.apple.sbd
Automator				Microsoft AutoUpdate			com.apple.sharedfilelist
BaiduMacHi				Microsoft Update Assistant		com.apple.siri.remembers
BibDesk					Mixin					com.apple.spotlight
BraveSoftware				MobileSync				com.apple.touristd
CEF					Mozilla					com.apple.transparencyd
CallHistoryDB				Oracle					com.baidu.BaiduNetdisk-mac
CallHistoryTransactions			Postgres				com.crashlytics
Chromium				Quick Look				com.eltima.cloudmounter
Citrix					ReadyAPI-2.5.0				com.eltima.cmd1
CloudDocs				Skype					com.expandrive.exfs
Code - Insiders				Skype Helper				com.kite.KiteAutostart
CoreParsec				Spectacle				com.kite.KiteHelper
CrashReporter				SyncServices				com.microsoft.teams
DiskImages				System Preferences			cordova-simulate
Dock					Trader Workstation			dmd
Docker Desktop				TrustedPeersHelper			iCloud
Dropbox					Zotero					iLifeMediaBrowser
Electron				accountsd				icdd
Faasoft Audio Converter			binstar					org.videolan.vlc
FileProvider				com.apple.AMPLibraryAgent		ru.keepcoder.Telegram
Google					com.apple.ContextStoreAgent		syncdefaultsd
HP					com.apple.ProtectedCloudStorage		transmission-daemon
JREInstaller				com.apple.TCC				transparencyd
Java					com.apple.accounts.dom			videosubscriptionsd
Jitsi					com.apple.appleseed.FeedbackAssistant	zoom.us
Knowledge				com.apple.backgroundtaskmanagementagent	微信开发者工具
Kobo					com.apple.exchangesync
yy66@Yijuns-Air Application Support % cd ../Caches 
yy66@Yijuns-Air Caches % ncdu
yy66@Yijuns-Air Caches % cd ../Application\ Support 
yy66@Yijuns-Air Application Support % ncdu
yy66@Yijuns-Air Application Support % df -h
Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1s5   112Gi   11Gi  1.7Gi    87%  487483 1174983277    0%   /
devfs          195Ki  195Ki    0Bi   100%     674          0  100%   /dev
/dev/disk1s1   112Gi   96Gi  1.7Gi    99% 2277931 1173192829    0%   /System/Volumes/Data
/dev/disk1s4   112Gi  3.0Gi  1.7Gi    65%       6 1175470754    0%   /private/var/vm
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /System/Volumes/Data/home
yy66@Yijuns-Air Application Support % ssh aws
Welcome to Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-45-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

 * MicroK8s passes 9 million downloads. Thank you to all our contributors!

     https://microk8s.io/

 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

Welcome to Alibaba Cloud Elastic Compute Service !

Last login: Tue May 19 22:54:27 2020 from 51.6.38.11
iZj6cdfzpgl8j2ugshk8t9Z

ubuntu@iZj6cdfzpgl8j2ugshk8t9Z:~$ s mixin
There is a screen on:
	2469.mixin	(05/19/2020 07:32:18 PM)	(Multi, detached)
1 Socket in /run/screen/S-ubuntu.

= Set Flags =
  
An exemplar project for setting personal, verifiable flags as part of regular investing in yourself.

== Requirements ==

See the functioning prototype at https://group-mixin.droneidentity.eu.

== Design ==

* Model

Database tables

* View

RESFTful API's

* Controller

Front-end

== Implementation ==

* The source will be organised using Model-View-Controller (MVC) architecture.

models/

views/

controllers/
