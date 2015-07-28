# pytimeout

Python module to enable timeout on python code.

Based on http://stackoverflow.com/questions/8464391/what-should-i-do-if-socket-setdefaulttimeout-is-not-working
Márton Miháltz <mmihaltz@gmail.com>

Example:

```
from pytimeout import Timeout
from time import sleep

try:
    with Timeout(3):
        print('This may take some time...')
        sleep(1800) # statements that may time out here
except Timeout.Timeout:
    print('Oops, timed out')
```
