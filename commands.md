# Commands

This is the first file in the project, the commands are not sorted yet, they
might be at some point.

## tar

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
