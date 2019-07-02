# greaseLib

A library for creating low latency, low CPU usage logging subsystems.

Features:
- Tries to be as zero-copy as possible when creating amalgamted log
- Low overhead when creating multiple sinks
- No blocking ever on log APIs
- 3 primary meta data for each log entry: tag, origin, level
- Support for custom log routing (`logMeta`)
- Support for a fast, Unix socket log sink using UNIX datagram
- Support for std syslog socket

Documentation:

The source. Perhaps we will have time to add some eventually.

But see `standalone_test_logsink.c` to get started.


## Build Instructions:
1. Build the dependencies inside `deps` folder
  ```
   cd greaseLib\deps
   sh install-deps.sh
   ```
2. Build the grease lib or application (`make grease_echo` or `make standalone_test_logsink`) with makefile
  ```
  cd greaseLib
  make 
  ```
  
## Test / Example
`standalone_test_logsink` is the sample implementation and test code for greaseLib. Execute by providing library paths, default ` LD_LIBRARY_PATH=deps/build/lib ./standalone_test_logsink`
