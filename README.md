NanoLog
Low Latency C++17 Logging Library..
Supports typical logger features namely multiple log levels, log file rolling and asynchronous writing to file.

Design highlights
Zero copying of string literals.
Lazy conversion of integers and doubles to ascii.
No heap memory allocation for log lines representable in less than ~256 bytes.

Guaranteed and Non Guaranteed logging
Nanolog supports Guaranteed logging i.e. log messages are never dropped even at extreme logging rates.
Nanolog also supports Non Guaranteed logging. Uses a ring buffer to hold log lines. In case of extreme logging rate when the ring gets full (i.e. the consumer thread cannot pop items fast enough), the previous log line in the slot will be dropped. Does not block producer even if the ring buffer is full.
