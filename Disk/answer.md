###磁盘访问 练习
####问题1：执行FIFO调度策略
#####-a 0
Block:   0  Seek:  0  Rotate:165  Transfer: 30  Total: 195
TOTALS      Seek:  0  Rotate:165  Transfer: 30  Total: 195
#####-a 6
Block:   6  Seek:  0  Rotate:345  Transfer: 30  Total: 375
TOTALS      Seek:  0  Rotate:345  Transfer: 30  Total: 375
#####-a 30
Block:  30  Seek: 80  Rotate:265  Transfer: 30  Total: 375
TOTALS      Seek: 80  Rotate:265  Transfer: 30  Total: 375
#####-a 7,30,8
Block:   7  Seek:  0  Rotate: 15  Transfer: 30  Total:  45
Block:  30  Seek: 80  Rotate:220  Transfer: 30  Total: 330
Block:   8  Seek: 80  Rotate:310  Transfer: 30  Total: 420
TOTALS      Seek:160  Rotate:545  Transfer: 90  Total: 795
#####-a 10,11,12,13,24,1
Block:  10  Seek:  0  Rotate:105  Transfer: 30  Total: 135
Block:  11  Seek:  0  Rotate:  0  Transfer: 30  Total:  30
Block:  12  Seek: 40  Rotate:320  Transfer: 30  Total: 390
Block:  13  Seek:  0  Rotate:  0  Transfer: 30  Total:  30
Block:  24  Seek: 40  Rotate:260  Transfer: 30  Total: 330
Block:   1  Seek: 80  Rotate:280  Transfer: 30  Total: 390
TOTALS      Seek:160  Rotate:965  Transfer:180  Total:1305

####问题2：执行SSTF调度策略
#####-a 10,11,12,13,24,1
Block:  10  Seek:  0  Rotate:105  Transfer: 30  Total: 135
Block:  11  Seek:  0  Rotate:  0  Transfer: 30  Total:  30
Block:   1  Seek:  0  Rotate: 30  Transfer: 30  Total:  60
Block:  12  Seek: 40  Rotate:260  Transfer: 30  Total: 330
Block:  13  Seek:  0  Rotate:  0  Transfer: 30  Total:  30
Block:  24  Seek: 40  Rotate:260  Transfer: 30  Total: 330
TOTALS      Seek: 80  Rotate:655  Transfer:180  Total: 915
####问题3：执行SCAN，C-SCAN磁盘调度策略
#####-a 10,11,12,13,24,1 -p SCAN
Block:   1  Seek:  0  Rotate:195  Transfer: 30  Total: 225
Block:  24  Seek: 80  Rotate:220  Transfer: 30  Total: 330
Block:  13  Seek: 40  Rotate:320  Transfer: 30  Total: 390
Block:  12  Seek:  0  Rotate:300  Transfer: 30  Total: 330
Block:  11  Seek: 40  Rotate:260  Transfer: 30  Total: 330
Block:  10  Seek:  0  Rotate:300  Transfer: 30  Total: 330
TOTALS      Seek:160  Rotate:1595  Transfer:180  Total:1935
#####-a 10,11,12,13,24,1 -p CSCAN
Block:   1  Seek:  0  Rotate:195  Transfer: 30  Total: 225
Block:  24  Seek: 80  Rotate:220  Transfer: 30  Total: 330
Block:  13  Seek: 40  Rotate:320  Transfer: 30  Total: 390
Block:  12  Seek:  0  Rotate:300  Transfer: 30  Total: 330
Block:  11  Seek: 40  Rotate:260  Transfer: 30  Total: 330
Block:  10  Seek:  0  Rotate:300  Transfer: 30  Total: 330
TOTALS      Seek:160  Rotate:1595  Transfer:180  Total:1935