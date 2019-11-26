### Time
```python 
# show date string > '2019-10-01'
datetime.date.today().isoformat()
# show datetime string (utc) > '2019-10-01T14:41:47.055933'
datetime.datetime.today().isoformat()
```

### Random

```python
# random string that can forever never be same
import time
s = ('%06x' % int(time.time()*10000000)).upper()
```
### String
String formatting
```python
{.2f}
{:=>30}
```

[home](/index)