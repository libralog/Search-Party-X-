# Search-Party-X-
<!-- blockquote -->
>The above script uses command line options to search for the specified input inside the HTML, JavaScript, Nmap scans and header files. The script simply traverse through all the collected data and uses grep to find the matching keywords.
<!-- code blocks -->
```bash
root@ubuntu:~/example.com$ ./search.sh -h
[+]USAGE: ./search.sh  (OPTIONS)
-j (string) - search in javascript files
-x (string) - search in header files
-e (string) - search in  html files
-n (string) - search nmap scans
-h - help
```
```bash
chmod 755 search.sh
```
```bash
$ ./search.sh -j "admin"
```
```bash
$ ./search.sh -x "nginx"
```
```bash
$ ./search.sh -e "s3.amazonaws"
```
```bash
$ ./search.sh -n "ssh" #searching nmap scans for the string ssh
```
<!-- blockquote -->
>In the first example, the string “admin” will be searched inside all the JavaScript files. In the second example, the string “nginx” will be searched inside all the header responses which we gathered in the data collection phase and the third example will look for the string “s3.amazonaws” in the response bodies.
<!-- code blocks -->
<!-- blockquote -->
>Try it yourself: If you want you can create a custom word-list and can write a simple shell script to pass on the words from the word-list to the search.sh script for quick asset discovery
