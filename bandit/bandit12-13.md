# Bandit Level 12 → Level 13

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit13.html)

The password for the next level is stored in the file data.txt, which is a hexdump of a file that
has been repeatedly compressed. For this level it may be useful to create a directory under /tmp
in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command
“mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Solution

```shell
ssh bandit12@bandit.labs.overthewire.org -p 2220  # (with password 'GROozWPO8QyN0mGrjUkID0WCYkZiQxrN')
cd $(mktemp -d) && cp ~/data.txt .
file data.txt  # data.txt: ASCII text
xxd -r data.txt data1 && file data1  # data1.gz: gzip compressed data, was "data2.bin", last modified: Sat Sep 26 21:52:56 2026, max compression, from Unix, original size modulo 2^32 582
gunzip -k -c data1 > data2 && file data2  # data2.bin: bzip2 compressed data, block size = 900k
bunzip2 -k -c data2 > data3 && file data3  # data3: gzip compressed data, was "data4.bin", last modified: Sat Sep 26 21:52:56 2026, max compression, from Unix, original size modulo 2^32 20480
gunzip -k -c data3 > data4 && file data4  # data4: POSIX tar archive (GNU)
tar -xf data4 && file data5.bin  # data5.bin: POSIX tar archive (GNU)
tar -xf data5.bin && file data6.bin  # data6.bin: bzip2 compressed data, block size = 900k
bunzip2 -k -c data6.bin > data7 && file data7  # data7: POSIX tar archive (GNU)
tar -xf data7 && file data8.bin  # data8.bin: gzip compressed data, was "data9.bin", last modified: Sat Sep 26 21:52:56 2026, max compression, from Unix, original size modulo 2^32 49
gunzip -k -c data8.bin > data9 && file data9  # data9: ASCII text
cat data9
```

One step command:
```shell
cd $(mktemp -d) && cp ~/data.txt . && \
xxd -r data.txt data1 && \
gunzip -k -c data1 > data2 && \
bunzip2 -k -c data2 > data3 && \
gunzip -k -c data3 > data4 && \
tar -xf data4 && \
tar -xf data5.bin && \
bunzip2 -k -c data6.bin > data7 && \
tar -xf data7 && \
gunzip -k -c data8.bin > data9 && \
cat data9
```

## Result

```text
The password is qQYQiHOBPR8zR61qxYqX45quvihF2uzk
```

We've got password `qQYQiHOBPR8zR61qxYqX45quvihF2uzk`!
