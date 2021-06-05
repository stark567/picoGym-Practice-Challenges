# Category - General Skills
# Author - SYREAL
Description
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `6d448c9c`


# Solution 
This challenge launches an instance on demand.
Its current status is: NOT_RUNNING


```
zerodaytea@Patryk:~$ ssh ctf-player@venus.picoctf.net -p 52218
The authenticity of host '[venus.picoctf.net]:52218 ([3.131.124.143]:52218)' can't be established.
ECDSA key fingerprint is SHA256:NrQkIxNEQQho/GA7jE0WlIa7Jh4VF9sAvC5awkbuj1Q.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[venus.picoctf.net]:52218,[3.131.124.143]:52218' (ECDSA) to the list of known hosts.
ctf-player@venus.picoctf.net's password:
Welcome to Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@pico-chall$
```


if this is the first time you are sshing to the particular network you will have to type "yes" aftering being prompted whether to add the network host to the list of your computer's known hosts. We are then prompted for the password to our ctf-player user which we get from the description and are able to get our bash shell. Looking at the files in our current directory we see a "1of3.flag.txt" file which we cat out as well as a "instructions-to-2of3.txt" file which we cat out to get a hint for where to find the next part of the flag.

```
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$
```
