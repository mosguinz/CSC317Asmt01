---
export_on_save:
    html: true
puppeteer:
    format: "Letter"
    timeout: 3000
chrome:
    printBackground: true
---

# Assignment 01

## 1. What is the command to determine the kernel version of your OS? Please write the command and its output.

```sh
ubuntu@primary:~$ uname -v
#63-Ubuntu SMP Thu Nov 24 13:48:31 UTC 2022
```

## 2. What is the command to determine the current user logged in? Please write the command and its output.

```sh
ubuntu@primary:~$ whoami
ubuntu
```

## 3. What is the Linux command or commands to list all user accounts on a Linux system? ONLY user account names should be shown!

```sh
ubuntu@primary:~$ awk -F: '{print $1}' /etc/passwd
root
daemon
bin
sys
sync
games
man
lp
mail
news
uucp
proxy
www-data
backup
list
irc
gnats
nobody
systemd-network
systemd-resolve
messagebus
systemd-timesync
syslog
_apt
tss
uuidd
tcpdump
sshd
pollinate
landscape
fwupd-refresh
ubuntu
lxd
```

## 4. Using your answer from the previous question, what would be the command or commands to show the the list of users as a comma separated list.

i. You may need to use the | (pipe command) to link two commands together.

```sh
ubuntu@primary:~$ awk -v ORS=',' -F: '{print $1}' /etc/passwd
root,daemon,bin,sys,sync,games,man,lp,mail,news,uucp,proxy,www-data,backup,list,irc,gnats,nobody,systemd-network,systemd-resolve,messagebus,systemd-timesync,syslog,_apt,tss,uuidd,tcpdump,sshd,pollinate,landscape,fwupd-refresh,ubuntu,lxd,
```

## 5. What is the command or commands that will show you the last 15 lines of the /var/log/kern.log file? Please write the commands and copy the output.
a. If your system does not have a kern.log, simply print which ever file in your
system stores system logs.
b. Note, WSL2 may not have a kern.log file at all.

```sh
ubuntu@primary:~$ head -15 /var/log/kern.log
Feb  9 04:43:15 primary kernel: [    0.000000] Booting Linux on physical CPU 0x0000000000 [0x410fd083]
Feb  9 04:43:15 primary kernel: [    0.000000] Linux version 5.15.0-57-generic (buildd@bos02-arm64-057) (gcc (Ubuntu 11.3.0-1ubuntu1~22.04) 11.3.0, GNU ld (GNU Binutils for Ubuntu) 2.38) #63-Ubuntu SMP Thu Nov 24 13:48:31 UTC 2022 (Ubuntu 5.15.0-57.63-generic 5.15.74)
Feb  9 04:43:15 primary kernel: [    0.000000] efi: EFI v2.70 by EDK II
Feb  9 04:43:15 primary kernel: [    0.000000] efi: SMBIOS 3.0=0x7f700000 MEMATTR=0x7cf05698 ACPI 2.0=0x7bf70018 MOKvar=0x7ceef000 MEMRESERVE=0x7c371118
Feb  9 04:43:15 primary kernel: [    0.000000] secureboot: Secure boot disabled
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: Early table checksum verification disabled
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: RSDP 0x000000007BF70018 000024 (v02 BOCHS )
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: XSDT 0x000000007BF7FE98 000064 (v01 BOCHS  BXPC     00000001      01000013)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: FACP 0x000000007BF7FA98 00010C (v05 BOCHS  BXPC     00000001 BXPC 00000001)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: DSDT 0x000000007BF77518 00141A (v02 BOCHS  BXPC     00000001 BXPC 00000001)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: APIC 0x000000007BF7FC18 0000A8 (v03 BOCHS  BXPC     00000001 BXPC 00000001)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: PPTT 0x000000007BF7FD18 000060 (v02 BOCHS  BXPC     00000001 BXPC 00000001)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: GTDT 0x000000007BF7D898 000060 (v02 BOCHS  BXPC     00000001 BXPC 00000001)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: MCFG 0x000000007BF7FE18 00003C (v01 BOCHS  BXPC     00000001 BXPC 00000001)
Feb  9 04:43:15 primary kernel: [    0.000000] ACPI: SPCR 0x000000007BF7FF98 000050 (v02 BOCHS  BXPC     00000001 BXPC 00000001)
```

## 6. What is the command or commands that will show you all the login attempts for your username? Please write the commands and copy the output.
## 7. Using the dmesg command, show only the messages relating to warnings and errors. Also ensure the output is using a human readable time format. To verify that only error and warning messages are being show what option of dmesg would you use? Show both commands that were used.
## 8. What command would you use to display free disk space? List the command and its output.
## 9. What is the command or commands that would list the contents of the /var/log directory in alphanumeric order? List the command and its output.
## 10. What is the command or commands that would list all the empty files or folders in your user’s home directory?
## 11. What is the command or commands used to list the files in /var/log in order of their size? List the command and its output.
## 12. What is the command or commands used to list the top 10 file who use the most disk space? What is this command(s) and show its output?
## 13.  What is the command that will show you the last 15 commands you have typed? List the command and its output.
## 14.  What is the difference between the commands less and more?
