### recurrsive glob

get all filename in directory that satisifies given re
```python
from pathlib import Path
f_list = []
for filename in Path('./imgs').glob('**/*.png'):
    f_list.append(str(filename))
```
[home](/index/)