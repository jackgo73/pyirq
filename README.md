# pyirq

format /proc/interrupts content

## usage

```
# python pyirq.py
INTs / 1 second(s) / top 3 cpus / top 5 ints - Tue Oct 20 15:15:48 2020
INT#         INCR   TOPCPU#0  TOPCPU#1  TOPCPU#2  NAME
 LOC          572    6( 18%)  10( 10%)   0( 07%)  Local timer interrupts
 IWI           16    0( 25%)  10( 12%)  15( 12%)  IRQ work interrupts
 TLB           10    2( 10%)   8( 10%)  10( 10%)  TLB shootdowns
  26            7    0(100%)   1( 00%)   2( 00%)  PCI-MSI-edge virtio3-input.0
  27            6   29(100%)   0( 00%)   1( 00%)  PCI-MSI-edge virtio1-req.0
INTs / 1 second(s) / top 3 cpus / top 5 ints - Tue Oct 20 15:15:49 2020
INT#         INCR   TOPCPU#0  TOPCPU#1  TOPCPU#2  NAME
 LOC          504    6( 20%)  10( 10%)   0( 07%)  Local timer interrupts
 IWI            9   25( 44%)   0( 22%)  18( 22%)  IRQ work interrupts
  42            1   15(100%)   0( 00%)   1( 00%)  PCI-MSI-edge virtio3-output.7
  49            1   22(100%)   0( 00%)   1( 00%)  PCI-MSI-edge virtio3-input.11
INTs / 1 second(s) / top 3 cpus / top 5 ints - Tue Oct 20 15:15:50 2020
INT#         INCR   TOPCPU#0  TOPCPU#1  TOPCPU#2  NAME
 LOC          566    6( 18%)  10( 09%)   8( 05%)  Local timer interrupts
 IWI           10   25( 40%)   8( 20%)  18( 20%)  IRQ work interrupts
  64            3    0(100%)   1( 00%)   2( 00%)  PCI-MSI-edge virtio5-req.0
  42            1   15(100%)   0( 00%)   1( 00%)  PCI-MSI-edge virtio3-output.7
  68            1    0(100%)   1( 00%)   2( 00%)  PCI-MSI-edge virtio5-req.4
```

press 5

```
INTs / 1 second(s) / top 5 cpus / top 5 ints - Tue Oct 20 15:16:17 2020
INT#         INCR   TOPCPU#0  TOPCPU#1  TOPCPU#2  TOPCPU#3  TOPCPU#4  NAME
 LOC          600   10( 17%)  14( 09%)  20( 09%)  22( 08%)   2( 05%)  Local timer interrupts
 IWI           13   22( 46%)  25( 30%)  18( 15%)  20( 07%)   0( 00%)  IRQ work interrupts
 RES            4    0( 25%)   1( 25%)   4( 25%)  26( 25%)   2( 00%)  Rescheduling interrupts
  42            3   15(100%)   0( 00%)   1( 00%)   2( 00%)   3( 00%)  PCI-MSI-edge virtio3-output.7
  64            3    0(100%)   1( 00%)   2( 00%)   3( 00%)   4( 00%)  PCI-MSI-edge virtio5-req.0
INTs / 1 second(s) / top 5 cpus / top 5 ints - Tue Oct 20 15:16:18 2020
INT#         INCR   TOPCPU#0  TOPCPU#1  TOPCPU#2  TOPCPU#3  TOPCPU#4  NAME
 LOC          745   10( 17%)  20( 11%)  14( 07%)  22( 07%)  25( 07%)  Local timer interrupts
 IWI           18   22( 38%)  25( 22%)  20( 16%)  18( 11%)  30( 11%)  IRQ work interrupts
  68            5    0(100%)   1( 00%)   2( 00%)   3( 00%)   4( 00%)  PCI-MSI-edge virtio5-req.4
  27            4   29(100%)   0( 00%)   1( 00%)   2( 00%)   3( 00%)  PCI-MSI-edge virtio1-req.0
  42            1   15(100%)   0( 00%)   1( 00%)   2( 00%)   3( 00%)  PCI-MSI-edge virtio3-output.7
INTs / 1 second(s) / top 5 cpus / top 5 ints - Tue Oct 20 15:16:19 2020
INT#         INCR   TOPCPU#0  TOPCPU#1  TOPCPU#2  TOPCPU#3  TOPCPU#4  NAME
 LOC          613   10( 16%)  22( 09%)  14( 09%)  30( 07%)  20( 07%)  Local timer interrupts
 IWI           20   22( 35%)  30( 30%)  15( 10%)  18( 10%)   0( 05%)  IRQ work interrupts
  27            2   29(100%)   0( 00%)   1( 00%)   2( 00%)   3( 00%)  PCI-MSI-edge virtio1-req.0
  42            1   15(100%)   0( 00%)   1( 00%)   2( 00%)   3( 00%)  PCI-MSI-edge virtio3-output.7
  49            1   22(100%)   0( 00%)   1( 00%)   2( 00%)   3( 00%)  PCI-MSI-edge virtio3-input.11
```

press 1

```
INTs / 1 second(s) / top 1 cpus / top 5 ints - Tue Oct 20 15:17:13 2020
INT#         INCR   TOPCPU#0  NAME
 LOC          549   18( 25%)  Local timer interrupts
 IWI           16   28( 25%)  IRQ work interrupts
  29            6    2(100%)  PCI-MSI-edge virtio3-input.1
  34            3    7(100%)  PCI-MSI-edge virtio3-output.3
  42            2   15(100%)  PCI-MSI-edge virtio3-output.7
INTs / 1 second(s) / top 1 cpus / top 5 ints - Tue Oct 20 15:17:14 2020
INT#         INCR   TOPCPU#0  NAME
 LOC          560   18( 21%)  Local timer interrupts
 IWI            6    3( 33%)  IRQ work interrupts
  42            1   15(100%)  PCI-MSI-edge virtio3-output.7
  43            1   16(100%)  PCI-MSI-edge virtio3-input.8
  49            1   22(100%)  PCI-MSI-edge virtio3-input.11
```

exit when press keys are not in  `[0, ... , 9]`


other usage

```
# python pyirq.py --help
Usage: pyirq.py [options]

Options:
  -h, --help            show this help message and exit
  -t TIME, --time=TIME  update interval in seconds
  -f INTR_FILE, --intr_file=INTR_FILE
                        read a file instead of /proc/interrupts
  -k TOPK, --topk=TOPK  top k interrupts
  -d, --debug           debug mode
  -v, --version         get version
```

