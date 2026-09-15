## Guidelines
Follow these rules while creating your practice note:

- Run and record output for **at least 6 commands**
- Include **2 process commands** (`ps`, `top`, `pgrep`, etc.)
- Include **2 service commands** (`systemctl status`, `systemctl list-units`, etc.)
- Include **2 log commands** (`journalctl -u <service>`, `tail -n 50`, etc.)
- Pick **one service on your system** (example: `ssh`, `cron`, `docker`) and inspect it
- Keep it **simple and actionable**



# Process checks
## `ps`

```
[pgregoretti] ~
 ● ps
  PID TTY           TIME CMD
 2486 ttys000    0:00.22 -zsh
 ```

## `top`

```
Processes: 426 total, 3 running, 423 sleeping, 2682 threads                                                                 23:36:36
Load Avg: 1.68, 2.09, 2.03  CPU usage: 5.17% user, 4.47% sys, 90.35% idle  SharedLibs: 315M resident, 84M data, 55M linkedit.
MemRegions: 0 total, 0B resident, 0B private, 710M shared. PhysMem: 7541M used (1305M wired, 3357M compressor), 91M unused.
VM: 191T vsize, 6144M framework vsize, 162356(12) swapins, 260580(0) swapouts. Networks: packets: 1667040/1988M in, 299528/91M out.
Disks: 6609625/139G read, 2077089/53G written.

PID    COMMAND      %CPU TIME     #TH   #WQ  #PORT MEM    PURG   CMPRS  PGRP  PPID  STATE    BOOSTS          %CPU_ME %CPU_OTHRS UID
36652  Intelligence 25.5 00:00.87 5/1   4/1  52+   10M+   768K+  3216K- 36652 1     running   0[0]           0.06419 2.41186    501
0      kernel_task  7.1  28:33.04 566/9 0    0     23M    0B     0B     0     0     running   0[0]           0.00000 0.00000    0
2429   iTerm2       6.0  01:25.60 7     4    395   95M+   12M    31M-   2429  1     sleeping *0[324]         0.07134 0.00000    501
986    BiomeAgent   5.6  00:31.64 5     4/1  226+  8433K+ 0B     2112K- 986   1     sleeping  0[4288]        2.27727 0.04181    501
```



# Service checks
## `systemctl status`

```


```

## `systemctl list-units`

# Log checks
## `journalctl -u <service>`

## `tail -n 50`

# Mini troubleshooting steps
## `ssh`