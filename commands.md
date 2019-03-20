# Commands [![ReadMe](Pictures/git.png)](https://github.com/iZome/Useful_commands)

This is the first file in the project, the commands are not sorted yet, they
might be at some point.

* [tar](#tar)
* [screen](#screen)

## tar
<a name="tar"></a>

tldr:
``` tar -xvzf file.tar.gz```

* ```f```: this must be the last flag of the command, and the tar file must be immediately after. It tells tar the name and path of the compressed file.
* ```z```: tells tar to decompress the archive using gzip
* ```x```: tar can collect files or extract them. ```x``` does the latter.
* ```v```: makes tar talk a lot. Verbose output shows you all the files being extracted.
source: https://askubuntu.com/questions/25347/what-command-do-i-need-to-unzip-extract-a-tar-gz-file

When downloading a file ending with ".tar.gz" you can use tar to extract the files.
Normally the command over will work smoothly, but if the file is not been gzipped you will get some error message like:
```gzip: stdin: not in gzip format```
Then drop the ```z``` and write.

``` tar -xvf file.tar.gz```


## screen
<a name="screen"></a>

tldr:  
``` screen -S [session name]```  
``` screen -r ```  
``` screen -ls ```  
``` screen -X -S [session # you want to kill] quit```

What is cool with **screen**?
* Have a terminal session that can be used on a remote computer without getting screwed by disconnects.
* Possibility to reconnect to a terminal session, even from a different location.
* Have multiple shells on one connection.
* Possibility to deactivate window.

To activate a screen simply write ```screen``` and ```screen -r``` when reattaching. To do any **screen** commands first use the combination **"ctrl+a"** followed up by:
  - "?" - list possible combinations in a **help** page
  - "c" - **c**reate new window
  - "n" - switch to **n**ext window in loop
  - "p" - switch to **p**revious window in loop
  - write ```exit``` to close window, is all windows are closed the screen is terminated
  - "d" - **d**etach from screen
  - "S"  - opportunity to give meaningful session name, will show when performing ```screen -ls```
  - "X" - send command to running
