##  Basic work with files

- Create directory test1

```console
mkdir test1
```

- Create file test1.txt inside the test1 directory.

```console
cd\test1
touch test.txt
```

-   Create copy of folder test1 with name test2.

```console
~/Desktop/test/test_ggs$ cp -r test1 test2
```

-    Delete file test1.txt inside test2 directory.

```console
~/Desktop/test/test_ggs/test2$ rm test1.txt 
```
-    Rename test2 folder into directory_without_file

```console
~/Desktop/test/test_ggs$ mv test2 directory_without_file
```

-    Insert 'test1' text into test1/test1.txt file.

```console
~/Desktop/test/test_ggs/test1$ printf 'test1' > test1.txt 
```
- print the text from the test1/test1.txt file.

```console
~/Desktop/test/test_ggs/test1$ cat test1.txt
test1
```

-    Insert 'test2' into the end of test1/test1.txt file.

```console
~/Desktop/test/test_ggs/test1$ echo "test2" >> test1.txt 
```
- print the text from the test1/test1.txt file.

```console
~/Desktop/test/test_ggs/test1$ cat test1.txt 
test1
test2
```
- check the size of test1 directory
```console
~/Desktop/test/test_ggs/test1$ ls -la
total 12
drwxrwxr-x 2 lytui lytui 4096 Jan 24 12:44 .
drwxrwxr-x 5 lytui lytui 4096 Jan 24 12:56 ..
-rw-rw-r-- 1 lytui lytui   13 Jan 24 13:13 test1.txt
```
## Permissions

-   Create test directory and block access for all to it.
```console 
~/Desktop/test/test_ggs$ chmod 0000  permision/
```
-   Try to remove that directory
```
I can delete it, because i am  creator
```

-    Create simple script which prints current date. Try to execute it.
```console
lytui@GGS:~$ date
```

## Log checking

-  Count lines in the file test.txt.

```console
~/Desktop/test/test_ggs$ wc  test.txt 
  200  3272 41699 test.txt
```

- Show last 3 lines from the test.txt file. 
 
```console
~/Desktop/test/test_ggs$ tail -3 test.txt 
54.236.1.13 - - [17/Jan/2022:00:32:25 -0600] "GET /blog/post/meet_me_in_morocco__a_vibrant_garden_party_inspired_by_north_africas_gem HTTP/1.1" 403 699 "-" "Mozilla/5.0 (compatible; Pinterestbot/1.0; +http://www.pinterest.com/bot.html)"
18.237.220.122 - - [17/Jan/2022:00:31:19 -0600] "GET / HTTP/1.1" 403 699 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.116 Safari/537.36"
18.237.220.122 - - [17/Jan/2022:00:31:49 -0600] "GET / HTTP/1.1" 403 699 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.116 Safari/537.36"

```
-  Hom many uniq IP addresses accessed the website ? 
```console
~/Desktop/test/test_ggs$ sed -e 's/\([0-9]\+\.[0-9]\+\.[0-9]\+\.[0-9]\+\).*$/\1/' test.txt 
114.119.138.117
141.8.142.92
50.93.32.73
95.163.255.40
54.236.1.13
95.163.255.10
95.163.255.30
95.163.255.31
95.163.255.10
85.208.98.30
95.163.255.41
54.236.1.11
157.55.39.28
54.236.1.13
95.163.255.41
87.250.224.184
85.208.98.23
95.163.255.41
54.236.1.13
54.236.1.11
207.46.13.213
95.163.255.51
95.163.255.51
95.163.255.21
95.163.255.30
54.236.1.11
157.55.39.45
114.119.138.13
54.236.1.11
173.252.79.22
173.252.79.12
54.236.1.11
54.236.1.11
54.236.1.13
54.236.1.11
64.9.255.11
64.9.255.11
54.236.1.13
178.63.51.106
54.236.1.13
54.236.1.13
106.11.159.111
87.250.224.101
141.8.142.92
87.250.224.184
68.67.155.230
54.236.1.13
54.236.1.11
31.13.127.5
31.13.127.36
157.55.39.45
157.55.39.45
54.236.1.11
54.236.1.11
54.236.1.11
54.236.1.11
31.13.127.6
54.236.1.13
157.55.39.28
31.13.127.1
68.67.155.230
157.55.39.75
54.236.1.13
54.236.1.13
54.236.1.11
31.13.127.8
31.13.103.1
54.236.1.11
114.119.138.117
157.55.39.114
54.236.1.11
54.236.1.11
54.236.1.13
54.236.1.11
31.13.103.118
207.46.13.129
157.55.39.114
54.236.1.11
213.180.203.22
207.46.13.213
54.236.1.13
216.244.66.235
54.236.1.13
31.13.103.116
31.13.115.120
54.236.1.11
114.119.138.111
69.63.189.2
69.63.189.117
31.13.103.111
5.255.253.109
54.236.1.13
54.236.1.11
157.90.181.150
54.236.1.11
54.236.1.11
157.55.39.114
54.236.1.11
157.90.181.150
54.236.1.13
157.90.181.150
185.191.171.17
35.240.117.238
54.236.1.13
157.90.181.150
54.236.1.13
54.236.1.13
157.90.181.150
185.191.171.35
157.55.39.28
31.13.103.2
54.236.1.11
54.236.1.11
87.250.224.187
54.236.1.13
54.236.1.11
54.236.1.13
157.55.39.28
95.163.255.11
54.236.1.11
54.236.1.11
95.108.213.60
95.163.255.40
95.163.255.41
95.163.255.31
207.46.13.213
95.163.255.41
35.211.201.14
35.211.201.14
35.211.201.14
54.236.1.13
54.236.1.11
95.163.255.40
54.236.1.13
157.55.39.75
69.89.26.54
54.236.1.11
157.55.39.114
54.236.1.13
54.236.1.13
114.119.138.117
54.236.1.13
34.90.7.164
69.89.26.54
216.244.66.235
54.236.1.13
182.108.21.155
34.90.7.164
54.236.1.13
54.236.1.13
54.236.1.13
54.236.1.11
54.236.1.11
157.55.39.28
54.236.1.13
34.90.168.133
34.90.168.133
54.236.1.11
54.236.1.11
207.46.13.213
54.236.1.11
5.45.207.120
54.236.1.13
54.236.1.13
131.220.6.152
34.90.168.133
54.236.1.13
8.211.2.156
54.236.1.11
54.236.1.13
54.236.1.13
157.55.39.75
54.236.1.11
54.236.1.11
85.208.98.196
198.199.104.179
54.236.1.11
54.236.1.11
54.236.1.11
207.46.13.213
207.46.13.213
66.249.75.12
85.208.98.199
54.236.1.13
54.236.1.13
54.236.1.11
125.71.65.77
54.236.1.11
54.236.1.11
54.236.1.11
95.108.213.13
54.236.1.11
54.236.1.11
54.236.1.11
54.236.1.13
18.237.220.122
54.236.1.13
54.236.1.13
18.237.220.122
18.237.220.122

```

-  IP address with most requests.

```console
~/Desktop/test/test_ggs$ cat test.txt  | awk '{print $1}' | sort | uniq -c | sort -n
1 106.11.159.111
      1 114.119.138.111
      1 114.119.138.13
      1 125.71.65.77
      1 131.220.6.152
      1 173.252.79.12
      1 173.252.79.22
      1 178.63.51.106
      1 182.108.21.155
      1 185.191.171.17
      1 185.191.171.35
      1 198.199.104.179
      1 207.46.13.129
      1 213.180.203.22
      1 31.13.103.1
      1 31.13.103.111
      1 31.13.103.116
      1 31.13.103.118
      1 31.13.103.2
      1 31.13.115.120
      1 31.13.127.1
      1 31.13.127.36
      1 31.13.127.5
      1 31.13.127.6
      1 31.13.127.8
      1 35.240.117.238
      1 50.93.32.73
      1 5.255.253.109
      1 5.45.207.120
      1 66.249.75.12
      1 69.63.189.117
      1 69.63.189.2
      1 8.211.2.156
      1 85.208.98.196
      1 85.208.98.199
      1 85.208.98.23
      1 85.208.98.30
      1 87.250.224.101
      1 87.250.224.187
      1 95.108.213.13
      1 95.108.213.60
      1 95.163.255.11
      1 95.163.255.21
      2 141.8.142.92
      2 216.244.66.235
      2 34.90.7.164
      2 64.9.255.11
      2 68.67.155.230
      2 69.89.26.54
      2 87.250.224.184
      2 95.163.255.10
      2 95.163.255.30
      2 95.163.255.31
      2 95.163.255.51
      3 114.119.138.117
      3 157.55.39.45
      3 157.55.39.75
      3 18.237.220.122
      3 34.90.168.133
      3 35.211.201.14
      3 95.163.255.40
      4 157.55.39.114
      5 157.55.39.28
      5 157.90.181.150
      5 95.163.255.41
      6 207.46.13.213
     41 54.236.1.13
     48 54.236.1.11
```

-  Top 3 IP addresses by amount of POST requests.
 
Nothing

-  Which IP addresses received 403 error ? 
```console
~/Desktop/test/test_ggs$ grep '403' test.txt | cut -d: -f1 test.txt 
114.119.138.117 - - [16/Jan/2022]
141.8.142.92 - - [16/Jan/2022]
50.93.32.73 - - [16/Jan/2022]
95.163.255.40 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
95.163.255.10 - - [16/Jan/2022]
95.163.255.30 - - [16/Jan/2022]
95.163.255.31 - - [16/Jan/2022]
95.163.255.10 - - [16/Jan/2022]
85.208.98.30 - - [16/Jan/2022]
95.163.255.41 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
157.55.39.28 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
95.163.255.41 - - [16/Jan/2022]
87.250.224.184 - - [16/Jan/2022]
85.208.98.23 - - [16/Jan/2022]
95.163.255.41 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
207.46.13.213 - - [16/Jan/2022]
95.163.255.51 - - [16/Jan/2022]
95.163.255.51 - - [16/Jan/2022]
95.163.255.21 - - [16/Jan/2022]
95.163.255.30 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
157.55.39.45 - - [16/Jan/2022]
114.119.138.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
173.252.79.22 - - [16/Jan/2022]
173.252.79.12 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
64.9.255.11 - - [16/Jan/2022]
64.9.255.11 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
178.63.51.106 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
106.11.159.111 - - [16/Jan/2022]
87.250.224.101 - - [16/Jan/2022]
141.8.142.92 - - [16/Jan/2022]
87.250.224.184 - - [16/Jan/2022]
68.67.155.230 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
31.13.127.5 - - [16/Jan/2022]
31.13.127.36 - - [16/Jan/2020]
157.55.39.45 - - [16/Jan/2022]
157.55.39.45 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
31.13.127.6 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
157.55.39.28 - - [16/Jan/2022]
31.13.127.1 - - [16/Jan/2022]
68.67.155.230 - - [16/Jan/2022]
157.55.39.75 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
31.13.127.8 - - [16/Jan/2022]
31.13.103.1 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
114.119.138.117 - - [16/Jan/2022]
157.55.39.114 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
31.13.103.118 - - [16/Jan/2022]
207.46.13.129 - - [16/Jan/2022]
157.55.39.114 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
213.180.203.22 - - [16/Jan/2022]
207.46.13.213 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
216.244.66.235 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
31.13.103.116 - - [16/Jan/2022]
31.13.115.120 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
114.119.138.111 - - [16/Jan/2022]
69.63.189.2 - - [16/Jan/2022]
69.63.189.117 - - [16/Jan/2022]
31.13.103.111 - - [16/Jan/2022]
5.255.253.109 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
157.90.181.150 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
157.55.39.114 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
157.90.181.150 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
157.90.181.150 - - [16/Jan/2022]
185.191.171.17 - - [16/Jan/2022]
35.240.117.238 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
157.90.181.150 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
157.90.181.150 - - [16/Jan/2022]
185.191.171.35 - - [16/Jan/2022]
157.55.39.28 - - [16/Jan/2022]
31.13.103.2 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
87.250.224.187 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
157.55.39.28 - - [16/Jan/2022]
95.163.255.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
95.108.213.60 - - [16/Jan/2022]
95.163.255.40 - - [16/Jan/2022]
95.163.255.41 - - [16/Jan/2022]
95.163.255.31 - - [16/Jan/2022]
207.46.13.213 - - [16/Jan/2022]
95.163.255.41 - - [16/Jan/2022]
35.211.201.14 - - [16/Jan/2022]
35.211.201.14 - - [16/Jan/2022]
35.211.201.14 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
95.163.255.40 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
157.55.39.75 - - [16/Jan/2022]
69.89.26.54 - - [16/Jan/2022]
54.236.1.11 - - [16/Jan/2022]
157.55.39.114 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
114.119.138.117 - - [16/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
34.90.7.164 - - [16/Jan/2022]
69.89.26.54 - - [16/Jan/2022]
216.244.66.235 - - [16/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
182.108.21.155 - - [17/Jan/2022]
34.90.7.164 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.13 - - [16/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
157.55.39.28 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
34.90.168.133 - - [17/Jan/2022]
34.90.168.133 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
207.46.13.213 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
5.45.207.120 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
131.220.6.152 - - [17/Jan/2022]
34.90.168.133 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
8.211.2.156 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
157.55.39.75 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
85.208.98.196 - - [17/Jan/2022]
198.199.104.179 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
207.46.13.213 - - [17/Jan/2022]
207.46.13.213 - - [17/Jan/2022]
66.249.75.12 - - [17/Jan/2022]
85.208.98.199 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
125.71.65.77 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
95.108.213.13 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.11 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
18.237.220.122 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
54.236.1.13 - - [17/Jan/2022]
18.237.220.122 - - [17/Jan/2022]
18.237.220.122 - - [17/Jan/2022]


- Task with * . Write script to show which pages Google checked from the website 

## Replace

Replace IP address with most reuests on 127.0.0.1 in test.txt file 
