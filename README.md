blocksver
=========

blocksver - gives you a nice view of the latest blocks versions and which
bip9 softfork is likely to activate soon.

You must have bitcoind 0.13.1 or later and bitcoin-cli installed.  
When run for the first time the script will retrieve all the latest blocks data and cache it.  
After the cache has been built it will run almost instantly, depending on how many
blocks have been mined since the last run.  
An example of the output produced:

```
Best height: 437962 - 6 new blocks
Best hash: 0000000000000000036cf0a27673ea08b007cec0ccdb4e8ab751526d8506f9f5
Network hashrate: 1823 Ph/s
Next diff-change at block 439488 - in 1526 blocks ~10.6 days 2016-11-19
Next halving at block 630000 - in 192038 blocks ~3.7 years 2020-07-04

ID      BIT  START       TIMEOUT     STATUS
csv       0  2016-05-01  2017-05-01  active
segwit    1  2016-11-15  2017-11-15  defined

A block can signal support for a softfork using the bits 0-28, only if the
bit is within the time ranges above, and if bits 31-30-29 are set to 0-0-1.
Signalling can start at the first diff change after the START time.
Lock-in threshold is 1916/2016 blocks (95.04%)

Version of all blocks since the last difficulty adjustment:

VERSION       28  24  20  16  12   8   4   0  BLOCKS  SHARE
               |   |   |   |   |   |   |   |
0x20000000  ..*.............................     474   96.54%
0x30000000  ..*o............................      10    2.04%
0x00000004  .............................*..       6    1.22%
0x08000004  ....*........................*..       1    0.20%
                                                 491  100.00%
ID       BIT   BLOCKS  SHARE
none     none     481  97.96%
unknown    28      10   2.04%
```
