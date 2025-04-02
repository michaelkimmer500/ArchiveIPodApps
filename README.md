# ArchiveIPodApps
Steps to archive Ipod apps as .ipa files (works as of 4/1/25)

Help was obtained from here: https://www.reddit.com/r/LegacyJailbreak/wiki/guides/crackingapps/

## Steps to Crack IPod Apps

Make sure your IPod is connected to Wi-Fi (the same as your computer)

1.) Jailbreak ipod (if not done already, there are other tutorials that can help with this)

2.) Open Cydia app on IPod

3.) Open Cydia and click on `Sources`. Click `Edit` and then `Add`. Type in `http://repo.kawaiizenbo.me` and click `Add Source`, then wait patiently for the repo to be added. (If you haven't clicked Complete Upgrade from a fresh jailbreak install, click on Manage on the tab bar and then click Sources) 

**(Shoutout to KawaiiZenbo for rehosting Crackulous)**

4.) Install `Crackulous` from `kawaiizenbo` and `iFile` from `BigBoss`. To find both apps, you may need to scroll for a while before you see it.

4.5) If you do not see `BigBoss`, then click `Edit` and then `Add`. Type in `http://apt.thebigboss.org/repofiles/cydia` and click `Add Source`, then wait until the repo is added.

5.) Reboot iPod once both are installed

6.) Open the new app called `Crackulous`

7.) (Optional) If you want to know who cracked the apps in the filename, you can change this in under `Settings` under `Cracker Name`

8.) In the `Applications` tab, click on all the apps that you want to archive

9.) Wait for all the apps to finish cracking (you can see the progress under the `Cracking` tab)

## Connect to IPod from Computer

Once all apps have finished cracking, you can then ssh into your IPod from your computer in order to retrieve the .ipa files

10.) Open Cydia on the IPod again. This time, install OpenSSH (go to **Sources --> All Sources --> OpenSSH**, you may have to scroll for a while until you find it). Alternatively, under the `Cydia` tab in the Cydia app, there should be instructions to innstall OpenSSH under `OpenSSH Access How-To`

11.) Once installed, check the IP address of your IPod on the Wi-Fi network by going to **Settings --> Wi-Fi --> \<Network Name\>**. You should see an IP address that looks like 192.XXX.XXX.XXX or something

12.) On your computer, open a terminal window (terminal application)

13.) Create a folder called `CrackedIPAs` by running `mkdir CrackedIPAs`

14.) `ssh` into your IPod by running `ssh root@<ipod_IP_addr>` where <ipod_IP_addr> is the IP address from step 11. This may take quite a while the first time.

15.) When it asks for a password, enter `alpine` (the letters will not show up). You should then be connected to your IPod from your computer.

## (Recommended) Change SSH Password

Now that you have openSSH installed, other people can potentially connect to your IPod if they wanted. Since the default password is always `alpine`, it would be best to change it.

16.) After ssh-ing to your IPod, type `passwd` and hit `Enter`.

17.) Enter in a new password that you will need to use when SSHing into your IPod. It will ask you to type it twice. Like before, you will not see the letters.

18.) Now, type `passwd mobile` and hit `Enter`. Enter in the same password (twice again).

19.) Now, your ssh password should be changed. Write it down / don't forget it because this is the password you will use from now on to ssh into your IPod.

## Transfer Files from IPod to Computer

20.) If still ssh-ed to your IPod, type `exit` and hit `Enter` to disconnect from your IPod.

21.) On your IPod, all of the cracked apps should be stored at `/var/root/Documents/Cracked/`

22.) Run `scp "root@<ipod_IP_addr>:/var/root/Documents/Cracked/*" CrackedIPAs/` to copy the .ipa files from your IPod to your computer. You will need to enter in your ssh password again.

23.) The files should copy one-by-one, and eventually you should have them all

24.) Upload the IPA files somewhere for archival (There should be tutorials on the ios archive discord: https://discord.com/invite/HruUgkJDkF) 
